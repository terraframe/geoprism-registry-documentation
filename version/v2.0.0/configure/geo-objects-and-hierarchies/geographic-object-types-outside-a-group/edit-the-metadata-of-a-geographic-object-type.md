# Editing a Geo-Object Type

{% hint style="info" %}
Registry Administrators can edit the metadata of Geo-Object Types under the curation mandate of their organization
{% endhint %}

1.  Navigate to the **Geo-Objects and Hierarchies** page from the sidebar.

    <figure><img src="../../../../../.gitbook/assets/image (84).png" alt=""><figcaption></figcaption></figure>
2.  Click the three-dot menu next to the Geo-Object Type and select **Edit**.

    <figure><img src="../../../../../.gitbook/assets/image (82).png" alt=""><figcaption></figcaption></figure>
3.  The Geo-Object Type opens for editing, with **Identity**, **Configuration**, **Ownership** and **Attributes** sections. Change the fields you need:

    | Field | Description | Can be changed |
    | ----- | ----------- | -------------- |
    | Code | The unique identifier. | No |
    | Label | The display label, with one field per installed locale. The default locale is required. | Yes |
    | Description (Abstract) | A description, with one field per installed locale. | Yes |
    | Visibility | Select **Private** to make the type visible only to people in its organization. | Yes, except for a type in a group, which uses the group's visibility |
    | Group Membership | Shows whether the type is a group. | No |
    | Group | For a type in a group, the code of the group it belongs to. | No |
    | Geo-Object Editing | **Enable geometry editing** sets whether Geo-Object geometries can be edited with the web-based editing tools. | Yes |
    | Geometry Type | The geometry that Geo-Objects of this type must have. | No |
    | Organization | The organization that manages the type. | No |

    The Concept Set chosen when the type was created isn't shown here and can't be changed. To add or change attributes, see [manage-the-attributes-associated-to-a-geographic-object-type.md](manage-the-attributes-associated-to-a-geographic-object-type.md "mention").

4.  Click **Submit**.
