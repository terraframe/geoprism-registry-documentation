# Apache Jena Synchronization

{% hint style="info" %}
Synchronizations can only be created by administrators.
{% endhint %}

1.  Navigate to the _External System Synchronizations_ section of the _Settings_ page.<br>

    <figure><img src="../../../../.gitbook/assets/image (113).png" alt=""><figcaption></figcaption></figure>


2.  Click the _Register Synchronization_ button to open the management section.<br>

    <figure><img src="../../../../.gitbook/assets/image (114).png" alt=""><figcaption></figcaption></figure>


3.  Click _Create_ to open the _Synchronization Configuration_ modal.

    <figure><img src="../../../../.gitbook/assets/image (112).png" alt=""><figcaption></figcaption></figure>

| Field name              | Description                                                                                                                                                                                                                                                                         | Required? |
| ----------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------- |
| Label                   | The label of the external system.                                                                                                                                                                                                                                                   |           |
| Organization            | The organization the user belongs to. An external system will only be available to data and users within this organization.                                                                                                                                                         | Yes       |
| External System         | <p>The external system configuration that will be used to configure this synchronization. This must be registered before creating a synchronization. </p><p></p><p>See <a data-mention href="../register-an-external-system/">register-an-external-system</a></p>                   | Yes       |
| Spatial Knowledge Graph | <p>The published spatial knowledge graphs from the system. The published graph that is selected will be used for pushing data to the external system.</p><p></p><p>See <a data-mention href="../../explore/spatial-knowledge-graphs-skg.md">spatial-knowledge-graphs-skg.md</a></p> | Yes       |
| Namespace               | The namespace applied as an RDF prefix to the graph generated for synchronization.                                                                                                                                                                                                  | Yes       |
| Graph                   | The graph name applied as an RDF prefix to the graph generated for synchronization.                                                                                                                                                                                                 | Yes       |

4. Fill out the form and click _Submit._
