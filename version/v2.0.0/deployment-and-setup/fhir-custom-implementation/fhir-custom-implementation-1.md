# Create a custom implementation for exporting data to FHIR

{% hint style="warning" %}
All custom implementations for exporting data to a FHIR instance must implement the _net.geoprism.registry.etl.fhir.FhirDataPopulator_ interface.
{% endhint %}

An export implementation turns each row of a list version into FHIR `Location` and `Organization` resources. The easiest way to write one is to extend `AbstractFhirDataPopulator`, which handles the basic resources and provides helpers for hierarchy extensions (`addHierarchyExtension`) and `partOf` references (`setPartOf`).

| Method | Called |
| ------ | ------ |
| `getLabel()` | To show the implementation's name in the **Implementation** list of a synchronization configuration. |
| `configure(FhirConnection context, ListTypeVersion version, boolean resolveIds)` | Once, before the export, with the connection to the FHIR server and the list version being exported. |
| `populate(Business row, Facility facility)` | For each row of the list, to fill in the facility's `Location` and `Organization`. |
| `createExtraResources(Business row, Bundle bundle, Facility facility)` | For each row, to add any other resources to the bundle. |
| `finish(Bundle bundle)` | Once, after all rows have been processed. |

This example publishes locations and organizations using the IHE mCSD profiles. It's based on the mCSD export implementation built into Geoprism Registry.

```java
package com.terraframe.demo;

import java.util.LinkedList;
import java.util.List;

import org.commongeoregistry.adapter.constants.GeometryType;
import org.hl7.fhir.r4.model.Bundle;
import org.hl7.fhir.r4.model.CodeableConcept;
import org.hl7.fhir.r4.model.Coding;
import org.hl7.fhir.r4.model.Location;
import org.hl7.fhir.r4.model.Organization;

import com.google.gson.JsonArray;
import com.google.gson.JsonObject;
import com.runwaysdk.Pair;
import com.runwaysdk.business.Business;

import net.geoprism.registry.ListType;
import net.geoprism.registry.etl.fhir.AbstractFhirDataPopulator;
import net.geoprism.registry.etl.fhir.Facility;
import net.geoprism.registry.etl.fhir.FhirConnection;
import net.geoprism.registry.etl.fhir.FhirDataPopulator;
import net.geoprism.registry.ListTypeVersion;
import net.geoprism.registry.model.ServerGeoObjectType;
import net.geoprism.registry.model.ServerHierarchyType;

public class DemoFhirDataPopulator extends AbstractFhirDataPopulator implements FhirDataPopulator
{
  private List<ServerHierarchyType> hierarchies;

  public DemoFhirDataPopulator()
  {
    super();

    this.hierarchies = new LinkedList<ServerHierarchyType>();
  }

  @Override
  public String getLabel()
  {
    return "Demo Export Implementation";
  }

  @Override
  public void configure(FhirConnection context, ListTypeVersion version, boolean resolveIds)
  {
    super.configure(context, version, resolveIds);

    ListType list = version.getListType();

    JsonArray hierarchies = list.getHierarchiesAsJson();

    for (int i = 0; i < hierarchies.size(); i++)
    {
      JsonObject hierarchy = hierarchies.get(i).getAsJsonObject();

      String hCode = hierarchy.get("code").getAsString();

      List<Pair<String, Integer>> pCodes = list.getParentCodes(hierarchy);

      if (pCodes.size() > 0)
      {
        this.hierarchies.add(ServerHierarchyType.get(hCode));
      }
    }
  }

  @Override
  public void populate(Business row, Facility facility)
  {
    super.populate(row, facility);

    ServerGeoObjectType type = this.getList().getServerGeoObjectType();
    String label = type.getLabel().getValue();
    String system = this.getContext().getSystem();

    CodeableConcept concept = new CodeableConcept().setText(label).addCoding(new Coding(system, type.getCode(), label));

    Location location = facility.getLocation();
    location.addType(concept);
    location.getMeta().addProfile("http://ihe.net/fhir/StructureDefinition/IHE.mCSD.Location");

    Organization organization = facility.getOrganization();
    organization.addType(concept);
    organization.getMeta().addProfile("http://ihe.net/fhir/StructureDefinition/IHE.mCSD.Organization");

    if (type.getGeometryType().equals(GeometryType.MULTIPOINT))
    {
      location.getMeta().addProfile("http://ihe.net/fhir/StructureDefinition/IHE.mCSD.FacilityLocation");
      location.addType(new CodeableConcept().addCoding(new Coding("urn:ietf:rfc:3986", "urn:ihe:iti:mcsd:2019:facility", "Facility")));
      location.setPhysicalType(new CodeableConcept().setText("Building").addCoding(new Coding("http://terminology.hl7.org/CodeSystem/location-physical-type", "bu", "Building")));

      organization.getMeta().addProfile("http://ihe.net/fhir/StructureDefinition/IHE.mCSD.FacilityOrganization");
      organization.addType(new CodeableConcept().addCoding(new Coding("urn:ietf:rfc:3986", "urn:ihe:iti:mcsd:2019:facility", "Facility")));
    }
    else
    {
      location.getMeta().addProfile("http://ihe.net/fhir/StructureDefinition/IHE.mCSD.JurisdictionLocation");
      location.addType(new CodeableConcept().addCoding(new Coding("urn:ietf:rfc:3986", "urn:ihe:iti:mcsd:2019:jurisdiction", "Jurisdiction")));
      location.setPhysicalType(new CodeableConcept().setText("Jurisdiction").addCoding(new Coding("http://terminology.hl7.org/CodeSystem/location-physical-type", "jdn", "Jurisdiction")));

      organization.getMeta().addProfile("http://ihe.net/fhir/StructureDefinition/IHE.mCSD.JurisdictionsOrganization");
      organization.addType(new CodeableConcept().addCoding(new Coding("urn:ietf:rfc:3986", "urn:ihe:iti:mcsd:2019:jurisdiction", "Jurisdiction")));
    }

    if (this.hierarchies.size() > 1)
    {
      for (ServerHierarchyType hierarchy : this.hierarchies)
      {
        this.addHierarchyExtension(row, facility, hierarchy);
      }
    }
    else if (this.hierarchies.size() == 1)
    {
      this.setPartOf(row, facility, this.hierarchies.get(0));
    }
  }

  @Override
  public void createExtraResources(Business row, Bundle bundle, Facility facility)
  {
  }

  @Override
  public void finish(Bundle bundle)
  {
  }
}
```
