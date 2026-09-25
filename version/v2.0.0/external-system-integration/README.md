# External system integration

Geoprism Registry can share data with other systems in two ways:

* **Push data to another system** by registering it as an external system and setting up a synchronization. Geoprism Registry currently supports:
  * **Apache Jena**, which receives published [Spatial Knowledge Graphs](../explore/spatial-knowledge-graphs-skg/README.md) as RDF.
  * **FHIR** (Fast Healthcare Interoperability Resources), which can send data to a FHIR server, or pull data from one with a custom implementation.
* **Let another system pull data** from Geoprism Registry through its [REST API](available-apis.md).

## Setting up a synchronization

1.  [Register the external system](register-an-external-system/README.md) in **Settings**.
2.  [Create a synchronization configuration](synchronize-an-external-system/README.md) that says what data to send.
3.  Run the synchronization whenever you want to send the latest data.
