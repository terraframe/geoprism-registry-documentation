# 4.2. Register and synchronize an external system

Registering an external system allows to specify a persistent configuration for integrating with external systems. The external system registration is where synchronizations can be triggered (Apache Jena and FHIR only), modified, and generally referenced to understand how the integration is defined. Its primary function is to enable pushing content to an external system.

Registering an external system can only be done by a Registry Administrator or System Administrator. If a Registry Administrator creates the external system it will only be available to the organization that Registry Administrator is a member of. A System Administrator must assign the external system to an organization.

Setting up an external system synchronization enables a user to push data to that external system. Synchronization configurations require an external system to be registered and the external identifiers to be set through the data import process.

GeoPrism Registry currently supports integrations with the following systems:

* Apache Jena
* [Fast Healthcare Interoperability Resources®](https://www.hl7.org/fhir/) (FHIR)

The following sections provide more details on synchronizing with each system.
