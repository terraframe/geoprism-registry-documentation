# Introduction

<div align="left"><figure><img src="../../.gitbook/assets/Screenshot 2022-11-01 143354.jpg" alt="" width="331"><figcaption></figcaption></figure></div>

Geoprism Registry (GPR) is a translation layer that helps organizations bring time-aware data into AI while maintaining high quality, common geographies, common IDs, and provenance. Language models have no reliable built-in knowledge of which places exist, how they relate, or how they have changed. Geoprism Registry supplies that knowledge as structured, versioned data that AI systems and other applications can query and trace back to its source.&#x20;

At its core, GPR is an open source platform for maintaining an authoritative registry of geographic objects, such as administrative areas, settlements, health facilities, and schools. It records their hierarchies, geometries, attributes, and history, so historical data is always interpreted against the geography that was valid at the time. You define the structure of your data with Geo-Object Types, hierarchies, Concepts, and Business Types. You then load, correct, and maintain the data as it changes, explore it on maps and in lists, and publish it for other systems through the API. Geoprism Registry is released under the LGPL open source license.

Geoprism Registry can act as a common geo-registry (CGR): a single, reliable source of geographic data that any information system can use. See [gpr-as-a-cgr.md](gpr-as-a-cgr.md "mention") for background on the CGR concept.

## What you can do with Geoprism Registry

* **Model your data.** Define Geo-Object Types and the hierarchies that link them, classify Geo-Objects with Concepts, and add non-geospatial data with Business Types. See [Configure](configure/).
* **Load and maintain data.** Import spreadsheets, shapefiles and relationships, review changes through change requests, record historical events such as mergers and splits, and roll back imports if needed. See [Curate](curate/).
* **Explore and share data.** View Geo-Objects on a map, publish lists and spatial data for a date or period, and publish Spatial Knowledge Graphs for other systems. See [Explore](explore/).
* **Connect other systems.** Share data with external systems such as Apache Jena and FHIR, or use the APIs. See [External system integration](external-system-integration/).

## How this documentation is organized

| Section                                                         | For                                | What it covers                                                             |
| --------------------------------------------------------------- | ---------------------------------- | -------------------------------------------------------------------------- |
| [Deployment and setup](deployment-and-setup/)                   | System Administrators              | Installing Geoprism Registry, organizations, languages, email and branding |
| [External system integration](external-system-integration/)     | System and Registry Administrators | APIs, and connecting and synchronizing external systems                    |
| [Key Components](geoprism-registry-key-components/)             | Everyone                           | The concepts behind Geoprism Registry's content and roles                  |
| [Access and Permissions](geoprism-registry-tutorial/)           | Everyone                           | Logging in, managing users and passwords                                   |
| [Configure](configure/), [Curate](curate/), [Explore](explore/) | Registry users                     | How to use each part of the app, in the same order as the sidebar          |
