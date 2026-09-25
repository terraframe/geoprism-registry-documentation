# Adding a Geo-Object Type

{% hint style="info" %}
Registry Administrators can create the Geo-Object Types under the curation mandate of their organization
{% endhint %}

1.  Navigate to the **Geo-Objects and Hierarchies** page from the sidebar and make sure **Geo-Object Types** is selected at the top of the list.

    <figure><img src="../../../../../.gitbook/assets/image (84).png" alt=""><figcaption></figcaption></figure>
2.  Click **Add Geo-Object Type** under your organization.

    <figure><img src="../../../../../.gitbook/assets/image (6) (1) (2).png" alt=""><figcaption></figcaption></figure>
3.  Fill out the form:

    | Field | Description | Required |
    | ----- | ----------- | -------- |
    | Code | The unique human-readable identifier. It tells Geo-Object Types apart if two have the same label. It can't be changed later. | Required |
    | Label (Default Locale) | The display label for the Geo-Object Type. It's used when the default locale is selected in the language toggle, or when another language is selected but has no label. | Required |
    | Label (other installed locales) | A display label for each other locale installed in the system. | |
    | Description (Abstract) | A description of the Geo-Object Type, with one field per installed locale. | |
    | Group Membership | Shows whether this is a group. It can't be changed here. To create a group, click **Add Group** instead. See [Geo-Object Type Groups](../geo-object-type-groups/README.md). | |
    | Visibility | Select **Private** to make the Geo-Object Type visible only to people in its organization. Public types can be viewed (read only) by all organizations. | |
    | Geometry Type | The geometry that all Geo-Objects of this type must have: **Point**, **Line**, **Polygon** or **Mixed Geometries**. It can't be changed later. | Required |
    | Enable geometry editing | Whether Geo-Object geometries can be edited with Geoprism Registry's web-based editing tools. Selected by default. | |
    | Organization | The organization that manages the Geo-Object Type. It's filled in with the organization you clicked **Add Geo-Object Type** under, and can't be changed. | |
    | Concept Set | <p>Optional. The Concept Set used to classify Geo-Objects of this type. Selecting one adds a <strong>classification</strong> attribute to the type. When you import Geo-Object data, you map a column in your file to this attribute, and its values must be Concepts in the Concept Set.<br><br><mark style="color:$warning;">IMPORTANT: The Concept Set can't be added, changed or removed after the Geo-Object Type is created.</mark></p> | |
    | Start Date / End Date | The period of validity for the Concept Set on this type. Only shown when you choose a Concept Set. | Required with a Concept Set |
    | Root Term | For a taxonomy Concept Set, the Concept whose branch of the taxonomy provides the allowed values. | |

    <figure><img src="../../../../../.gitbook/assets/image (86).png" alt=""><figcaption></figcaption></figure>
4.  Click **Ok**. The new Geo-Object Type opens, and you can [add its attributes](manage-the-attributes-associated-to-a-geographic-object-type.md).

    <figure><img src="https://lh4.googleusercontent.com/o7M8ZVCNZHZN0UP2jV0KSgFsivunPL8tNkNAZjqb8SEO13cudcNkDBP_HpLBOEU53fZoUebtppPUcjXzxHoVHPgsRjWMsgjkO6HqcCKsOq2-nysbkHcoWZj78yXTvqVtaIGSy2a9VZiXjeSsy1-399d6otzENPg_iEEPvlTI8vn3fF7sTiLzukJ7" alt=""><figcaption></figcaption></figure>
