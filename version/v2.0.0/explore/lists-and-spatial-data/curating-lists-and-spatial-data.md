# Curating Lists and Spatial Data

Geoprism Registry helps you find and fix problems in your data in two ways:

* **Run Curation** checks a working version of a list for Geo-Objects without a geometry.
* **Curation tasks** are created when a [historical event](../../curate/historical-events/README.md) means other Geo-Objects may need changes. For example, when a district is split, the health facilities in it may need to be reassigned to the new district.

You can also sort a column in an open list to find Geo-Objects with empty values for an attribute.

## Checking for missing geometries

{% hint style="info" %}
The System Administrator, Registry Administrators and Registry Maintainers can run curation.
{% endhint %}

The check covers only the date or period of that list, not all the data in the registry.

1.  Navigate to the **Lists and Spatial Data** page from the sidebar. On the left, click the Geo-Object Type under its organization, then click the title of the set.

    <figure><img src="../../../../.gitbook/assets/image (34) (1).png" alt=""><figcaption></figcaption></figure>
2.  Open the **List** of the working version for the date or period you want to check.

    <figure><img src="../../../../.gitbook/assets/image (1) (1) (2) (1) (1).png" alt=""><figcaption></figcaption></figure>
3.  Click **Run Curation**.

    <figure><img src="../../../../.gitbook/assets/image (18) (4).png" alt=""><figcaption></figcaption></figure>
4.  The **Curation report** opens. It shows who started the check, when, and how many Geo-Objects have been checked. Each problem is listed with its **Problem Type** (**No Geometry**) and the Geo-Object's **Code**. If there are no problems, the report says **No validation issues found**.

    <figure><img src="../../../../.gitbook/assets/image (4) (1).png" alt=""><figcaption></figcaption></figure>

    <figure><img src="../../../../.gitbook/assets/image (16) (2).png" alt=""><figcaption></figcaption></figure>
5.  To fix a problem, click **Resolve**. The Geo-Object opens in the [Explorer](../explorer/README.md), where you can [add its geometry](../explorer/editing-a-geo-object.md). Then select **Resolved** in the report.

The latest report stays available until you run curation again. Click the **Last curation** link next to **Run Curation** to open it.

![](<../../../../.gitbook/assets/image (10) (1).png>)

## Curation tasks from historical events

{% hint style="warning" %}
In Geoprism Registry 2.0, the curation task list isn't linked from the sidebar. This section describes how tasks work, and will be updated once it's confirmed how to open them.
{% endhint %}

Tasks are listed under **Open Tasks** and **Completed Tasks**. An open task tells you about a historical event that may affect Geo-Objects you curate. For example, when Santa Rosa Shire is merged into Bacong Shire, you may need to reassign the hospitals in Santa Rosa Shire to Bacong Shire from the date of the merge.

<figure><img src="../../../../.gitbook/assets/image (17) (4).png" alt=""><figcaption></figcaption></figure>

To address a task:

1.  To learn more about the event, find it on the [Historical Events](../../curate/historical-events/README.md) page.
2.  Make the changes. If there are many, [import a spreadsheet](../../curate/import-geospatial-data/import-a-spreadsheet.md) with the new parent information. If there are only a few, [edit each Geo-Object](editing-lists-and-spatial-data.md).
3.  Mark the task as complete. It moves to **Completed Tasks**. If you marked it complete by mistake, you can mark it as open again.

    <figure><img src="../../../../.gitbook/assets/image (6) (3).png" alt=""><figcaption></figcaption></figure>
