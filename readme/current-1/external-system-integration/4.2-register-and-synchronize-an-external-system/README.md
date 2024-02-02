# 4.2. Register and synchronize an external system

Registering an external system allows to specify a persistent configuration for integrating with external systems. The external system registration is where synchronizations can be triggered (DHIS2 and FHIR only), modified, and generally referenced to understand how the integration is defined. Its primary function is for GeoPrism Registry to share its content with an external system. By storing both a standard GeoPrism Registry identifier and external system identifier, GeoPrism Registry can maintain a mapping between object instances in the two systems. The external identifiers are set in the system through the data import process.

Registering an external system can only be done by a Registry Administrator or System Administrator. If a Registry Administrator creates the external system it will only be available to the organization that Registry Administrator is a member of. A System Administrator must assign the external system to an organization.

Setting up an external system synchronization enables a user to push data to that external system. Synchronization configurations require an external system to be registered and the external identifiers to be set through the data import process.

GeoPrism Registry currently supports integrations with the following systems:

* [District Health Information System](https://dhis2.org/) 2 (DHIS2)
* [Reveal](https://revealprecision.com/)
* [Fast Healthcare Interoperability Resources®](https://www.hl7.org/fhir/) (FHIR)

The following sections provide more details on synchronizing with each system.
