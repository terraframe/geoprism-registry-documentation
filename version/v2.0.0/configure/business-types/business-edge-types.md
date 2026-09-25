# Business Edge Types

A **Business Edge Type** defines a kind of relationship that business objects can have with other business objects or with Geo-Objects. For example, a Business Edge Type could link Staff records to the Health Facility Geo-Objects they work at.

{% hint style="info" %}
Registry Administrators can create Business Edge Types for their organization. Only a System Administrator can edit or delete them.
{% endhint %}

## Creating a Business Edge Type

1.  Navigate to the **Business Types** page from the sidebar and select **Business Edge Types** at the top of the list.
2.  Click **Create** under your organization.
3.  Fill out the form:

    | Field | Description | Required |
    | ----- | ----------- | -------- |
    | Code | The unique human-readable identifier of the edge type. It can't be changed later. | Required |
    | Label | The display label, with one field per installed locale. | Required |
    | Description | A description, with one field per installed locale. | |
    | Parent Type | The type at the parent end of each edge: a Business Type, or **Geo-Object**. It can't be changed later. | Required |
    | Child Type | The type at the child end of each edge: a Business Type, or **Geo-Object**. It can't be changed later. | Required |
4.  Click **Submit**.

After you create a Business Edge Type, load its relationships on the [Import Edge Data](../../curate/import-edge-data.md) page.

## Editing or deleting a Business Edge Type

Click the three-dot menu next to the Business Edge Type:

* **Edit** lets you change its label and description, then click **Submit**. Its code, parent type and child type can't be changed.
* **Delete** removes it after you confirm by clicking **Delete**.
* **Import History** lists the imports into it.
