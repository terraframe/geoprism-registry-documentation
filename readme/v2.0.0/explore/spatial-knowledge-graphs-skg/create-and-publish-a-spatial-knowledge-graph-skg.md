# Create and Publish a Spatial Knowledge Graph (SKG)

1.  Navigate to the Publish SKG page from the navigation sidebar.<br>

    <figure><img src="../../../../.gitbook/assets/image (115).png" alt=""><figcaption></figcaption></figure>


2.  Click _Create_ to open a form for configuring a new SKG.<br>

    <figure><img src="../../../../.gitbook/assets/image (116).png" alt=""><figcaption></figcaption></figure>


3. Fill out the form being careful to select all the types needed for the SKG that will be created.

| Field                        | Description                                                                                                                                                                                                                                                                                |
| ---------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Label                        | The label describing the published SKG.                                                                                                                                                                                                                                                    |
| Valid For                    | <p>The date for which the published SKG is valid.<br><br>Example: An SKG with data specific to and updated for a  2025 analysis might be set to December 31, 2025.</p>                                                                                                                     |
| Start of period of validity  | The date defining the oldest data to include in the SKG. Geoprism Registry tracks change over time on Geo-Objects attributes, business objects, and edges. Those attribute level change over time dates are used to determine the validity of the data included in the published SKG.      |
| End of period of validity    | The date defining the most recent data to include in the SKG. Geoprism Registry tracks change over time on Geo-Objects attributes, business objects, and edges. Those attribute level change over time dates are used to determine the validity of the data included in the published SKG. |
| Geo-Object Types             | The Geo-Object Types to include in the published SKG.                                                                                                                                                                                                                                      |
| Hierarchy Types              | The hierarchy types to include in the published SKG.                                                                                                                                                                                                                                       |
| Directed Acyclic Graph Types | The directed acyclic graph types to include in the published SKG.                                                                                                                                                                                                                          |
| Undirected Graph Types       | The undirected graph types to include in the published SKG.                                                                                                                                                                                                                                |
| Business Types               | The business types to include in the published SKG.                                                                                                                                                                                                                                        |
| Business Edge Types          | The business edge types to include in the published SKG.                                                                                                                                                                                                                                   |

4.  Click _Submit. A summary of the publish configuration._<br>

    <figure><img src="../../../../.gitbook/assets/image (117).png" alt=""><figcaption></figcaption></figure>


5.  Push the _Publish Updates_ button to publish the first version of the SKG.<br>

    <figure><img src="../../../../.gitbook/assets/image (118).png" alt=""><figcaption></figcaption></figure>



#### Publishing SKG Updates

Once a spatial knowledge graph (SKG) configuration is created it can be updated when needed. This enables control over the state of the data in the published graph so that external systems can recieve a version of the published graph that fits that systems needs.&#x20;

1. Navigate to an existing published SKG.
2. Push the _Publish Updates_ button to publish a new version of the SKG.
   1. If there has been no changes to the data relevant for the publish configuration a message will indicate that there are no new events to publish. <br>



