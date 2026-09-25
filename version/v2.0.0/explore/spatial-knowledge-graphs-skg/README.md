# Spatial Knowledge Graphs (SKG)

A **Spatial Knowledge Graph** (SKG) is a published, versioned graph of your Geo-Objects, business objects and the edges between them, as they were on a chosen date. It's generated as [Resource Description Framework (RDF)](https://www.w3.org/RDF/) triples, a standard format that other systems can store and query.

SKGs are the way to share registry data with external systems. They replace [Labeled Property Graph](../labeled-property-graphs.md) downloads.

## How it works

* **Configuration.** On the **Publish SKG** page, you create an SKG configuration. It sets which types to include (Geo-Object Types, hierarchies, graph types, Business Types and Business Edge Types), the **Valid For** date whose values are published, and the period of validity recorded on the data.
* **Versions.** Each time you click **Publish updates**, Geoprism Registry creates a new version of the SKG. The first version contains all the selected data, and each later version contains the changes since the previous one.
* **Delivery.** External systems receive the published versions through a synchronization. The [Apache Jena synchronization](../../external-system-integration/synchronize-an-external-system/apache-jena-synchronization.md) pushes a published SKG to an Apache Jena triple store.

{% hint style="warning" %}
Publishing deletes all [rollback checkpoints](../../curate/rollback-data.md). Imports made before a publish can no longer be rolled back.
{% endhint %}

## Next steps

* [create-and-publish-a-spatial-knowledge-graph-skg.md](create-and-publish-a-spatial-knowledge-graph-skg.md "mention")
* [Synchronize an External System](../../external-system-integration/synchronize-an-external-system/README.md)
