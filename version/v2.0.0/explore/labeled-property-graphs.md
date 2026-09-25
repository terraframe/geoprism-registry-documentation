# Labeled Property Graphs

A **Labeled Property Graph** (LPG) definition describes a set of registry data that you can publish and download as an RDF graph. It's useful when you need a simple graph export of your data.

{% hint style="info" %}
LPG downloads are an older way to share data with external systems. For new integrations, use [Spatial Knowledge Graphs](spatial-knowledge-graphs-skg/README.md) with an [external system synchronization](../external-system-integration/synchronize-an-external-system/README.md) instead.
{% endhint %}

{% hint style="info" %}
If you don't see **Labeled Property Graphs** in the sidebar, the feature may not be enabled for your installation.
{% endhint %}

## Creating an LPG definition

1.  Navigate to the **Labeled Property Graphs** page from the sidebar.
2.  Click **Create**.
3.  Choose how the graph is dated. This can't be changed later.

    | Option | Description |
    | ------ | ----------- |
    | Single date | One graph of the data as it was on the **Valid For** date. |
    | Frequency-based | A graph for each period at a regular **Frequency** (**Annual**, **Biannual**, **Quarter** or **Monthly**), beginning on the **Start date**. |
    | Period-based | A graph for each period you define. Click **New** to add a period with a **Start Date** and **End Date**. |
4.  Fill out the rest of the form:

    | Field | Description | Required |
    | ----- | ----------- | -------- |
    | Code | The unique identifier of the LPG definition. It can't be changed later. | Required |
    | Title | The display title, with one field per installed locale. | Required |
    | Description (Abstract) | A description, with one field per installed locale. | Required |
    | Strategy Type | <p>How the data in the graph is selected. It can't be changed later.</p><ul><li><strong>Hierarchy Tree:</strong> for data modeled as a hierarchy on the Geo-Objects and Hierarchies page. The graph contains a Geo-Object and everything below it in a hierarchy.</li><li><strong>Graph:</strong> for data modeled with graph and edge types. The graph contains the types you choose.</li></ul> | Required |
5.  Fill out the fields for the strategy you chose:

    | Field | Strategy | Description |
    | ----- | -------- | ----------- |
    | Hierarchy | Hierarchy Tree | The hierarchy to follow. |
    | Root Geo Object | Hierarchy Tree | The Geo-Object Type, then the Geo-Object, at the top of the graph. The graph includes this Geo-Object and everything below it in the hierarchy. |
    | Organization | Graph | The organization whose access to data the graph uses. The graph can include that organization's data and data shared with it by other organizations. |
    | Geo-Object Types | Graph | The Geo-Object Types to include. |
    | Edge Types | Graph | The edge types to include. |
    | Business Types | Graph | The Business Types to include. |
    | Edges with Business Types | Graph | The edges involving Business Types to include. |
6.  Click **Submit**.

## Publishing a version

The LPG definition lists an entry for each date or period. Each entry can have several published versions.

1.  Click the LPG definition in the list to open it.
2.  Under the date or period you want, click **Publish New Version** and confirm.

A version saves the state of the data for that date or period, as it was recorded when you published the version. Because Geoprism Registry tracks changes over time, you can publish again later to capture any corrections or new data for the same period, and each version keeps its **Date Generated**.

To see older versions of an entry, click **See previous versions**. To delete a version, click **Delete** next to it and confirm.

For a Frequency-based definition, click **Update List Periods** to update the list of periods.

## Downloading a version as RDF

1.  Next to a published version, click **Export RDF** and choose how to include geometries:
    * **With Geometries**
    * **With Simplified Geometries**, which are geometrically simplified to make the file smaller
    * **Without Geometries**
2.  The export runs as a job, and the [Scheduled Jobs](../curate/scheduled-jobs/view-scheduled-jobs.md) page opens.
3.  When the export is ready, click **Download RDF Export**. The download is removed 15 days after it was generated.

## Other options

* **Configuration** on an open LPG definition shows the settings it was created with.
* The trash icon next to an LPG definition in the list deletes it after you confirm.
