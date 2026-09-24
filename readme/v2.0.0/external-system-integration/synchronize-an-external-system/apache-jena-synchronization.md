# Apache Jena Synchronization

{% hint style="info" %}
Synchronizations must be registered by administrators.
{% endhint %}

1.  Navigate to the _External System Synchronizations_ section of the _Settings_ page.<br>

    <figure><img src="../../../../.gitbook/assets/image (113).png" alt=""><figcaption></figcaption></figure>


2.  Click the _Register Synchronization_ button to open the management section.<br>

    <figure><img src="../../../../.gitbook/assets/image (114).png" alt=""><figcaption></figcaption></figure>


3.  Click _Create_ to open the _Synchronization Configuration_ modal.

    <figure><img src="../../../../.gitbook/assets/image (112).png" alt=""><figcaption></figcaption></figure>

| Field name              | Description                                                                                                                                                                                                                    | Required? |
| ----------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | --------- |
| Label                   | The label of the external system.                                                                                                                                                                                              |           |
| Organization            | The organization the user belongs to. An external system will only be available to data and users within this organization.                                                                                                    | Yes       |
| External System         | The external system configuration that will be used to configure this synchronization. This must be registered before creating a synchronization. See [register-an-external-system](../register-an-external-system/ "mention") | Yes       |
| Spatial Knowledge Graph |                                                                                                                                                                                                                                | Yes       |
| Namespace               |                                                                                                                                                                                                                                | Yes       |
| Graph                   |                                                                                                                                                                                                                                | Yes       |

4. Fill out the form and click _Submit._
