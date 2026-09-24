# 3.7. FHIR custom implementation

{% hint style="warning" %}
This documentation covers advanced system configuration.
{% endhint %}

{% hint style="info" %}
These transformations are what is used when importing or exporting data through an External Synchronization from or to a FHIR instance.
{% endhint %}

The data coming in and out of a Fast Healthcare Interoperability Resources (FHIR) instance is transformed through the use of the Java Service IOC architecture. A developer can add a new transformation by creating a JAR file that registers its classes as implementations of the FHIR interfaces. The following sections describe a step-by-step process to create a new FHIR implementation in the system.
