# FHIR External System

By storing both a standard Geoprism Registry identifier and external system identifier, Geoprism Registry can maintain a mapping between object instances in the two systems. The external identifiers are set in the system through the data import process.



1. Go to the **Settings** module from the sidebar.\
   ![](<../../../../.gitbook/assets/image (28).png>)
2.  Scroll down to the _External Systems_ section and click on the **+** button to open the _Registration_ modal.

    <figure><img src="../../../../.gitbook/assets/image (62).png" alt=""><figcaption></figcaption></figure>
3.  Select 'FHIR' from the _Type_ dropdown and fill out the other fields (descriptions in the table below).

    | Field name   | Description                                                                                                                 | Required? |
    | ------------ | --------------------------------------------------------------------------------------------------------------------------- | --------- |
    | Type         | The type of external system.                                                                                                | Yes       |
    | Organization | The organization the user belongs to. An external system will only be available to data and users within this organization. | Yes       |
    | ID           | The identifier for this external system.                                                                                    | Yes       |
    | Label        | The label of the external system.                                                                                           | Yes       |
    | Description  | A description of the external system.                                                                                       | No        |
    | URL          | The URL for the FHIR system.                                                                                                | Yes       |
    | System       | The FHIR system to use when exporting or importing                                                                          | Yes       |

<figure><img src="../../../../.gitbook/assets/Screenshot 2022-11-01 130337.jpg" alt=""><figcaption></figcaption></figure>

### Compatibility

Integration with FHIR requires use of FHIR OAuth security integration. Not all versions of [HAPI FHIR](https://hapifhir.io/) are known to be capable of integrating with Geoprism Registry via OAuth. The following table shows whether or not the steps in this document have been found to work with the listed version of HAPI FHIR.

| HAPPI FHIR version | Integration via OAuth possible? |
| ------------------ | ------------------------------- |
| 5.3.0              | Yes                             |

### Synchronization

Geoprism Registry supports using an Apache Jena external system synchronization to push data to an Apache Jena instance.&#x20;

* See [fhir-synchronization.md](../synchronize-an-external-system/fhir-synchronization.md "mention")
