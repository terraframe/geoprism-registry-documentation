# Spatial Knowledge Graphs (SKG)

A Spatial Knowledge Graph (SKG) is a published snapshot of your Geo-Objects, business objects, and edges, in a standard format other systems can query.

The **Publish SKG** page enables configuring, saving, managing, and publishing spatial knowledge graphs to be used by external systems. A published spatial knowledge graph defines which types it includes and the time period its data covers.

#### Generated Format

A published SKG generates [Resource Description Framework (RDF)](https://www.w3.org/RDF/) triples.



Each time you publish, Geoprism Registry creates a new version of the SKG containing the changes since the previous version. External systems receive these versions through a synchronization.

* See [create-and-publish-a-spatial-knowledge-graph-skg.md](create-and-publish-a-spatial-knowledge-graph-skg.md "mention") to create and publish an SKG.
* See [synchronize-an-external-system](../../external-system-integration/synchronize-an-external-system/ "mention") for how a published SKG is sent to an external system.

