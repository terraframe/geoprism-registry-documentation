# Concept Classes

See [.](./ "mention") for a definition of Concept and general overview.

A Concept Class defines the attribution structure for concepts contained within a Concept Set, including enumerations and taxonomies. This acts as a template that defines what information each Concept in a Concept Set has. Every Concept has a name, but a Concept Class could also add a definition, a code, or a source.

By itself, a Concept Class is not linked to any other data in the system. It must be assigned to a Concept Edge Type and Concept Set before that Concept Set can be used to classify a Geo-Object Type.

{% hint style="info" %}
Registry Administrators can manage the Concept Classes of their organization.
{% endhint %}

## Creating a Concept Class

1.  Navigate to the **Concept Classes** page from the sidebar. The page has three sections, **Concept Classes**, **Concept Edge Types** and **Concept Sets**, which you choose at the top of the list. Make sure **Concept Classes** is selected.
2.  Click **Add** under your organization.
3.  Fill out the form:

    <figure><img src="../../../../.gitbook/assets/image (72).png" alt=""><figcaption></figcaption></figure>

    | Field | Description | Required |
    | ----- | ----------- | -------- |
    | Code | The unique identifier of the Concept Class. It can't be changed later. | Required |
    | Label | The display label, with one field per installed locale. The default locale is required. | Required |
    | Description (Abstract) | A description, with one field per installed locale. | |
    | Organization | The organization that manages the Concept Class. It's filled in with the organization you clicked **Add** under, and can't be changed. | |
4.  Click **Ok**. The new Concept Class opens.

## Adding attributes

Every Concept Class has default attributes, such as the code and name of each Concept. To store more information about each Concept, such as a definition or a source, add custom attributes:

1.  Click the three-dot menu next to the Concept Class and select **Edit**.
2.  In the **Attributes** section, click **+ Add**, fill out the **Add a new attribute** form and click **Submit**. The form is the same as for Business Types, including **Is change over time**. See [managing-attributes-of-a-business-type.md](../business-types/managing-attributes-of-a-business-type.md "mention").

<figure><img src="../../../../.gitbook/assets/image (81).png" alt=""><figcaption></figcaption></figure>

## Other options

The three-dot menu next to a Concept Class also has:

* **View Data**, which opens a table of the Concepts in that class.
* **Import History**, which lists the imports into that class.
* **Delete**, which deletes the Concept Class after you confirm.

To load Concepts into a Concept Class, see [Import Business Data](../../curate/import-business-data.md).
