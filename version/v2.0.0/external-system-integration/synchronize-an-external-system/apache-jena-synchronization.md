# Apache Jena Synchronization

{% hint style="info" %}
Registry Administrators and System Administrators can create synchronizations. You need a registered [Apache Jena external system](../register-an-external-system/apache-jena-external-system.md) and a published [Spatial Knowledge Graph](../../explore/spatial-knowledge-graphs-skg/README.md).
{% endhint %}

An Apache Jena synchronization sends a published Spatial Knowledge Graph to a Jena triple store. Each run updates the data in the external system, rather than deleting and replacing the whole Jena database.

1.  Go to the **Settings** page. Find the **External System Synchronizations** section.

    <figure><img src="../../../../.gitbook/assets/image (113).png" alt=""><figcaption></figcaption></figure>
2.  Click **Register Synchronization** to open the **Synchronization Configurations** page.

    <figure><img src="../../../../.gitbook/assets/image (114).png" alt=""><figcaption></figcaption></figure>
3.  Click **Create** to open the **Synchronization Configuration** form, and fill it out:

    <figure><img src="../../../../.gitbook/assets/image (112).png" alt=""><figcaption></figcaption></figure>

    | Field name | Description | Required? |
    | ---------- | ----------- | --------- |
    | Label | The label of the synchronization profile. | Yes |
    | Organization | The organization the user belongs to. A synchronization profile will only be available to data and users within this organization. | Yes |
    | External System | <p>The registered external system configuration that will be used to configure this synchronization. This must be registered before creating a synchronization. </p><p></p><p>See <a data-mention href="../register-an-external-system/">register-an-external-system</a></p> | Yes |
    | Spatial Knowledge Graph | <p>The published spatial knowledge graphs from the system. The published graph that is selected will be used for pushing data to the external system.</p><p></p><p>See <a data-mention href="../../explore/spatial-knowledge-graphs-skg/">spatial-knowledge-graphs-skg</a></p> | Yes |
    | Namespace | <p>The base URI that begins the identifier of every resource in the published graph (e.g., <code>https://data.example.gov/gpr/</code>). This is the root descriptor of all the graph data.<br><br>Use a domain your organization controls, and avoid changing it after publishing, since that changes every identifier.</p> | Yes |
    | Graph | The name of the graph in the triple store that this synchronization populates. Named graphs keep each published SKG separate, so it can be queried, updated, or removed on its own. | Yes |
4.  Click **Submit** to save the configuration.

    <figure><img src="../../../../.gitbook/assets/image (119).png" alt=""><figcaption></figcaption></figure>
5.  Click **View** next to the configuration.
6.  Click **Run now** to push the selected SKG to Jena. Its progress appears under **Jobs**.

    <figure><img src="../../../../.gitbook/assets/image (120).png" alt=""><figcaption></figcaption></figure>
