# Synchronize an External System

A synchronization sends data from Geoprism Registry to a registered external system. Each synchronization configuration saves what to send and where, so you can run it again whenever you want to send the latest data.

{% hint style="info" %}
Registry Administrators and System Administrators can manage synchronizations. The external system must be [registered](../register-an-external-system/README.md) first.
{% endhint %}

## Managing synchronizations

1.  Go to the **Settings** page from the sidebar.
2.  In the **External System Synchronizations** section, click **Register Synchronization**.
3.  The **Synchronization Configurations** page lists each configuration. Click **Create** to add one, or use **View**, **Edit** and **Delete** on an existing one.

Clicking **View** opens the configuration. Click **Run now** to start a synchronization. Each run appears under **Jobs**, where you can see its progress and any errors.

For the steps for each type of system, see:

* [apache-jena-synchronization.md](apache-jena-synchronization.md "mention")
* [fhir-synchronization.md](fhir-synchronization.md "mention")

## Other ways to share data

Synchronizations push data to other systems. Other systems can also pull data from Geoprism Registry:

* [available-apis.md](../available-apis.md "mention")
* [labeled-property-graphs.md](../../explore/labeled-property-graphs.md "mention"), an older way to download a graph of your data
