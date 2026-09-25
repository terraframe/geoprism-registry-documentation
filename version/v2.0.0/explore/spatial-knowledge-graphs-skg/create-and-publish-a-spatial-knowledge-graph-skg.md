# Create and Publish a Spatial Knowledge Graph (SKG)

Publishing an SKG is a two-part process. First you create a configuration that says which types to include and which dates to use. Then you publish versions of it. External systems receive each version through an [external system synchronization](../../external-system-integration/synchronize-an-external-system/README.md).

## Creating an SKG configuration

1.  Navigate to the **Publish SKG** page from the sidebar.

    <figure><img src="../../../../.gitbook/assets/image (115).png" alt=""><figcaption></figcaption></figure>
2.  Click **Create** to open the **Configuration** form.

    <figure><img src="../../../../.gitbook/assets/image (116).png" alt=""><figcaption></figcaption></figure>
3.  Fill out the form. Select every type the SKG needs: an edge is only included when its edge type and the types at both of its ends are all selected.

    | Field | Description | Required |
    | ----- | ----------- | -------- |
    | Label | The label of the SKG. | Required |
    | Valid For | The date whose attribute values are published. Geoprism Registry tracks changes over time, so each Geo-Object and business object is published with the values it had on this date. <p><em>Example: For a 2025 analysis, set Valid For to December 31, 2025.</em></p> | Required |
    | Start of period of validity | The start of the period of validity recorded on the published data. | Required |
    | End of period of validity | The end of the period of validity recorded on the published data. In the current version, this second date field is also labelled **Start of period of validity**. | Required |
    | Geo-Object Types | The Geo-Object Types to include. If a Geo-Object Type has a Concept Set, its Concepts are published automatically. | |
    | Hierarchy Types | The hierarchies to include. | |
    | Directed Acyclic Graph Types | The directed acyclic graph types to include. | |
    | Undirected Graph Types | The undirected graph types to include. | |
    | Business Types | The Business Types to include. | |
    | Business Edge Types | The Business Edge Types to include. | |
4.  Click **Submit**. The SKG's configuration summary opens.

    <figure><img src="../../../../.gitbook/assets/image (117).png" alt=""><figcaption></figcaption></figure>
5.  Click **Publish updates** to publish the first version of the SKG.

    <figure><img src="../../../../.gitbook/assets/image (118).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
Publishing deletes all [rollback checkpoints](../../curate/rollback-data.md). Imports made before a publish can no longer be rolled back.
{% endhint %}

## Publishing updates

After the first version, you control when external systems receive new data by publishing new versions.

1.  On the **Publish SKG** page, click the SKG in the list.
2.  Click **Publish updates**.

Each new version contains only the changes to the selected types since the previous version. If nothing has changed, a message says there are no new events to publish.

The **Versions** table lists each version with its **Number**, **UID** and **Date**.

## Deleting an SKG

Click the trash icon next to the SKG in the list and confirm by clicking **Delete**.
