# Apache Jena Synchronization

{% hint style="info" %}
Synchronizations can only be created by administrators.
{% endhint %}

Apache Jena Synchronizations perform an update of the external system's data, rather than a full delete and replace of the destination's Jena database.&#x20;



1.  Navigate to the _External System Synchronizations_ section of the _Settings_ page.<br>

    <figure><img src="../../../../.gitbook/assets/image (113).png" alt=""><figcaption></figcaption></figure>


2.  Click the _Register Synchronization_ button to open the management section.<br>

    <figure><img src="../../../../.gitbook/assets/image (114).png" alt=""><figcaption></figcaption></figure>


3.  Click _Create_ to open the _Synchronization Configuration_ modal.

    <figure><img src="../../../../.gitbook/assets/image (112).png" alt=""><figcaption></figcaption></figure>

| Field name              | Description                                                                                                                                                                                                                                                                                                                 | Required? |
| ----------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------- |
| Label                   | The label of the synchronization profile.                                                                                                                                                                                                                                                                                   | Yes       |
| Organization            | The organization the user belongs to. A synchronization profile will only be available to data and users within this organization.                                                                                                                                                                                          | Yes       |
| External System         | <p>The registered external system configuration that will be used to configure this synchronization. This must be registered before creating a synchronization. </p><p></p><p>See <a data-mention href="../register-an-external-system/">register-an-external-system</a></p>                                                | Yes       |
| Spatial Knowledge Graph | <p>The published spatial knowledge graphs from the system. The published graph that is selected will be used for pushing data to the external system.</p><p></p><p>See <a data-mention href="../../explore/spatial-knowledge-graphs-skg/">spatial-knowledge-graphs-skg</a></p>                                              | Yes       |
| Namespace               | <p>The base URI that begins the identifier of every resource in the published graph (e.g., <code>https://data.example.gov/gpr/</code>). This is the root descriptor of all the graph data.<br><br>Use a domain your organization controls, and avoid changing it after publishing, since that changes every identifier.</p> | Yes       |
| Graph                   | The name of the graph in the triple store that this synchronization populates. Named graphs keep each published SKG separate, so it can be queried, updated, or removed on its own.                                                                                                                                         | Yes       |

4.  Fill out the form and click **Submit** to save the configuration.<br>

    <figure><img src="../../../../.gitbook/assets/image (119).png" alt=""><figcaption></figcaption></figure>
5.  Click the _View_ button to view the options for running the synchronization. <br>

    <figure><img src="../../../../.gitbook/assets/image (120).png" alt=""><figcaption></figcaption></figure>


6. Click **Publish** to push the selected SKG to Jena.

