# Apache Jena External System

An Apache Jena external system tells Geoprism Registry where to send data from a published Spatial Knowledge Graph. Geoprism Registry loads the graph into a named graph in a triple store at the URL you register (see [Apache Jena Synchronization](https://docs.geoprismregistry.com/version/v2.0.0/external-system-integration/synchronize-an-external-system/apache-jena-synchronization)) using the W3C SPARQL 1.1 Graph Store HTTP Protocol and SPARQL 1.1 Update.

Despite the name, this external system type isn’t limited to Apache Jena. Geoprism Registry supports two triple stores:

* **Apache Jena Fuseki**
* **Amazon Neptune**, including AWS IAM authentication

Other triple stores that implement SPARQL 1.1 may work if they expose query, update, and graph store endpoints at `/sparql`, `/update`, and `/data` relative to the URL you register.



1.  Go to the **Settings** page from the sidebar.

    ![](<../../../../.gitbook/assets/image (28).png>)
2.  In the **External Systems** section, click the plus icon to open the **External System** form.

    <figure><img src="../../../../.gitbook/assets/image (71).png" alt=""><figcaption></figcaption></figure>
3.  Select **Jena** as the **Type** and fill out the form:

    <figure><img src="../../../../.gitbook/assets/image (67).png" alt=""><figcaption></figcaption></figure>

    | Field               | Description                                                                                                                 | Required |
    | ------------------- | --------------------------------------------------------------------------------------------------------------------------- | -------- |
    | Type                | The type of external system. It can't be changed later.                                                                     | Required |
    | Organization        | The organization the external system is available to. It can't be changed later.                                            | Required |
    | ID                  | The identifier of the external system. It can't be changed later.                                                           | Required |
    | Label               | The display label, with one field per installed locale.                                                                     | Required |
    | Description         | A description, with one field per installed locale.                                                                         |          |
    | URL                 | The URL of the Jena instance, including the port, for example `https://example.com:8182`. Don't include the `/sparql` path. | Required |
    | Authentication Type | <ul><li>None</li><li>IAM</li></ul>                                                                                          | Yes      |
4. Click **Submit**.

## Synchronization

To send a published Spatial Knowledge Graph to the Jena instance, see [apache-jena-synchronization.md](../synchronize-an-external-system/apache-jena-synchronization.md "mention").
