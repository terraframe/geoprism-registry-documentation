# Apache Jena External System



1. Go to the **Settings** module from the sidebar.\
   ![](<../../../../.gitbook/assets/image (28).png>)
2.  Scroll down to the 'External Systems' section and click on the **+** button to open the Registration modal.

    <figure><img src="../../../../.gitbook/assets/image (71).png" alt=""><figcaption></figcaption></figure>
3.  Select Jena from the _Type_ dropdown and fill out the other fields.<br>

    <figure><img src="../../../../.gitbook/assets/image (67).png" alt=""><figcaption></figcaption></figure>

| Field name          | Description                                                                                                                 | Required? |
| ------------------- | --------------------------------------------------------------------------------------------------------------------------- | --------- |
| Type                | The type of external system.                                                                                                | Yes       |
| Organization        | The organization the user belongs to. An external system will only be available to data and users within this organization. | Yes       |
| ID                  | The identifier for this external system.                                                                                    | Yes       |
| Label               | The label of the external system.                                                                                           | Yes       |
| Description         | A description of the external system.                                                                                       | No        |
| URL                 | The URL of the Jena instance (ex: [https://example.com:8182](https://example.com:8182))                                     | Yes       |
| Authentication Type | <ul><li>None</li><li>IAM</li></ul>                                                                                          | Yes       |

### Synchronization

Geoprism Registry supports using an Apache Jena external system synchronization to push data to an Apache Jena instance.&#x20;

* See [apache-jena-synchronization.md](../synchronize-an-external-system/apache-jena-synchronization.md "mention")
