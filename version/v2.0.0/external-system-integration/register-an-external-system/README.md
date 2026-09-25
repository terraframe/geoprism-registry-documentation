# Register an External System

Registering an external system saves the connection details Geoprism Registry uses to send data to it. Synchronizations then use the registered system to send data.

{% hint style="info" %}
Registry Administrators and System Administrators can register external systems. A system registered by a Registry Administrator is only available to their organization. A System Administrator chooses the organization when registering one.
{% endhint %}

Geoprism Registry currently supports:

* [apache-jena-external-system.md](apache-jena-external-system.md "mention")
* [fhir-external-system.md](fhir-external-system.md "mention"): [Fast Healthcare Interoperability Resources®](https://www.hl7.org/fhir/)

## Managing registered systems

Registered systems are listed in the **External Systems** section of the **Settings** page, with their type, label and description.

* Click the plus icon at the bottom of the list to register a new system.
* Click the pencil icon to edit a system. Its type, organization and ID can't be changed.
* Click the trash icon to remove a system.
