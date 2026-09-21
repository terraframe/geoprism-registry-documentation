# Apache Jena

## Registration

The process for registering an Apache Jena instance in GeoPrism Registry is as follows:

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

### 4.2.1.2. Synchronization

GeoPrism Registry supports using a Jena external system synchronization to push data to a Jena instance. The purpose of the external system synchronization is to define the Spatial Knowledge Graphs, the types that are included in them, and the time period of the data that is sent to the Jena instance.&#x20;

The following steps are to be followed to enable the synchronization:

TODO
