# Adding a Geo-Object Type to a group

{% hint style="info" %}
Registry Administrators can add Geo-Object Types to groups under the curation mandate of their organization
{% endhint %}

1.  Navigate to the **Geo-Objects and Hierarchies** page from the sidebar.
2.  Click the three-dot menu next to the group and select **Add sub type**.

    <figure><img src="../../../../../.gitbook/assets/image (82).png" alt=""><figcaption></figcaption></figure>
3.  The **Add Geo-Object Type** form opens. Some fields are copied from the group and can't be changed. Fill out the form:

    | Field | Description | Required |
    | ----- | ----------- | -------- |
    | Code | The unique human-readable identifier of the Geo-Object Type. It can't be changed later. | Required |
    | Label (Default Locale) | The display label for the Geo-Object Type. It's used when the default locale is selected in the language toggle, or when another language is selected but has no label. | Required |
    | Label (other installed locales) | A display label for each other locale installed in the system. | |
    | Description (Abstract) | A description of the Geo-Object Type, with one field per installed locale. | |
    | Visibility | Copied from the group. It can't be changed. | |
    | Geometry Type | Copied from the group. It can't be changed. | |
    | Enable geometry editing | Whether Geo-Object geometries can be edited with Geoprism Registry's web-based editing tools. Selected by default. | |
    | Organization | The organization that manages the group. It can't be changed. | |

    A Geo-Object Type in a group has all the group's attributes, including its classification if the group has a Concept Set. You can also add attributes of its own.

    <figure><img src="../../../../../.gitbook/assets/image (87).png" alt=""><figcaption></figcaption></figure>
4.  Click **Ok**. The new Geo-Object Type appears under the group.

    <figure><img src="../../../../../.gitbook/assets/image (83).png" alt=""><figcaption></figcaption></figure>
