# Create a custom implementation for importing data from FHIR to Geoprism Registry

{% hint style="warning" %}
All custom implementations for importing data from a FHIR instance must implement the _net.geoprism.registry.etl.fhir.FhirResourceProcessor_ interface.
{% endhint %}

An import implementation turns FHIR `Location` and `Organization` resources into Geo-Objects. The easiest way to write one is to extend `AbstractFhirResourceProcessor` and implement how to find each resource's Geo-Object Type (`getType`), its identifier (`getIdentifier`), and how to fill in the Geo-Object (`populate`). You can also override `getGeometry` to read the geometry.

This example is based on the basic resource processor built into Geoprism Registry.

```java
package com.terraframe.demo;

import java.util.Date;
import java.util.Optional;

import org.commongeoregistry.adapter.dataaccess.LocalizedValue;
import org.commongeoregistry.adapter.dataaccess.ValueOverTimeDTO;
import org.hl7.fhir.r4.model.CodeableConcept;
import org.hl7.fhir.r4.model.Coding;
import org.hl7.fhir.r4.model.Identifier;
import org.hl7.fhir.r4.model.Location;
import org.hl7.fhir.r4.model.Organization;

import com.runwaysdk.dataaccess.ProgrammingErrorException;

import net.geoprism.registry.etl.fhir.AbstractFhirResourceProcessor;
import net.geoprism.registry.etl.fhir.FhirResourceProcessor;
import net.geoprism.registry.model.ServerGeoObjectIF;

public class DemoFhirResourceProcessor extends AbstractFhirResourceProcessor implements FhirResourceProcessor
{
  @Override
  public String getLabel()
  {
    return "Demo Resource processor";
  }

  @Override
  protected void populate(ServerGeoObjectIF geoObject, Location location, Date lastUpdated)
  {
    if (lastUpdated == null)
    {
      lastUpdated = new Date();
    }

    LocalizedValue value = LocalizedValue.createEmptyLocalizedValue();
    value.setValue(LocalizedValue.DEFAULT_LOCALE, location.getName());

    geoObject.setDisplayLabel(value, lastUpdated, ValueOverTimeDTO.INFINITY_END_DATE);
    geoObject.setExists(true, lastUpdated, ValueOverTimeDTO.INFINITY_END_DATE);
  }

  @Override
  protected String getType(Organization organization)
  {
    Coding coding = organization.getTypeFirstRep().getCodingFirstRep();

    if (coding != null)
    {
      String code = coding.getCode();

      if (code != null)
      {
        return code;
      }
    }

    throw new ProgrammingErrorException("Unable to derive the GPR GeoObject-Type for the organization [" + organization.getId() + "]");
  }

  @Override
  protected String getType(Location location)
  {
    String system = getSystem().getSystem();
    Optional<CodeableConcept> type = location.getType().stream().filter(t -> t.getCodingFirstRep().getSystem().equals(system)).findFirst();

    if (type.isPresent())
    {
      String code = type.get().getCodingFirstRep().getCode();

      if (code != null)
      {
        return code;
      }
    }

    throw new ProgrammingErrorException("Unable to derive the GPR GeoObject-Type for the location [" + location.getId() + "]");
  }

  @Override
  protected Identifier getIdentifier(Organization organization)
  {
    return organization.getIdentifier().stream().filter(i -> i.getSystem().equals(this.getSystem().getSystem())).findFirst().orElse(null);
  }

  @Override
  protected Identifier getIdentifier(Location location)
  {
    return location.getIdentifier().stream().filter(i -> i.getSystem().equals(this.getSystem().getSystem())).findFirst().orElse(null);
  }

}
```
