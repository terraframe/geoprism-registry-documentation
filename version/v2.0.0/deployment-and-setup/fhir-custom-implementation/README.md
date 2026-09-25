# FHIR custom implementation

{% hint style="warning" %}
This documentation covers advanced system configuration, for Java developers.
{% endhint %}

When Geoprism Registry exchanges data with a Fast Healthcare Interoperability Resources (FHIR) server through a [FHIR synchronization](../../external-system-integration/synchronize-an-external-system/fhir-synchronization.md), the data is transformed by an **implementation**:

* An **export implementation** (`FhirDataPopulator`) turns list data into FHIR resources.
* An **import implementation** (`FhirResourceProcessor`) turns FHIR resources into Geo-Objects.

Geoprism Registry includes these implementations, which you can choose in a synchronization configuration without writing any code:

| Implementation | Type | Class |
| -------------- | ---- | ----- |
| Basic Export Implementation | Export | `net.geoprism.registry.etl.fhir.BasicFhirDataPopulator` |
| mCSD Export Implementation | Export | `net.geoprism.registry.etl.fhir.MCSDFhirDataPopulator` |
| Basic Resource processor | Import | `net.geoprism.registry.etl.fhir.BasicFhirResourceProcessor` |

If these don't fit your data, a developer can write a custom implementation. Implementations are found with the Java `ServiceLoader`, so you add one by building a JAR that registers its classes. The steps are:

1.  [maven-project-setup.md](maven-project-setup.md "mention")
2.  [fhir-custom-implementation-1.md](fhir-custom-implementation-1.md "mention"), [fhir-custom-implementation-2.md](fhir-custom-implementation-2.md "mention"), or both
3.  [fhir-custom-implementation-3.md](fhir-custom-implementation-3.md "mention")
4.  [fhir-custom-implementation-4.md](fhir-custom-implementation-4.md "mention")
