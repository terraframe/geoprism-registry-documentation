# 3.7.3. Create a custom implementation for importing data from FHIR to GeoPrism Registry

{% hint style="warning" %}
All custom implementations for importing data from a FHIR instance must implement the _net.geoprism.registry.etl.fhir.FhirResourceProcessor_ interface.
{% endhint %}

```
package com.terraframe.demo;

import java.util.Date;
import java.util.Optional;

import org.commongeoregistry.adapter.dataaccess.LocalizedValue;
import org.hl7.fhir.r4.model.CodeableConcept;
import org.hl7.fhir.r4.model.Coding;
import org.hl7.fhir.r4.model.Identifier;
import org.hl7.fhir.r4.model.Location;
import org.hl7.fhir.r4.model.Organization;

import com.runwaysdk.dataaccess.ProgrammingErrorException;
import com.runwaysdk.dataaccess.graph.attributes.ValueOverTime;

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

    geoObject.setDisplayLabel(value, lastUpdated, ValueOverTime.INFINITY_END_DATE);
    geoObject.setExists(true, lastUpdated, ValueOverTime.INFINITY_END_DATE);
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
