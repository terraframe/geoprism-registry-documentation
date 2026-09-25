# Create an organization

{% hint style="info" %}
Only System Administrators can create and edit organizations.
{% endhint %}

1.  Go to the **Settings** page from the sidebar.

    ![](<../../../../.gitbook/assets/image (28).png>)
2.  In the **Organizations** section, click the plus icon (**Create Organization**) at the bottom of the table.

    ![](<../../../../.gitbook/assets/image (10) (3).png>)
3.  Fill out the **Organization** form:

    <figure><img src="../../../../.gitbook/assets/image (19).png" alt=""><figcaption></figcaption></figure>

    | Field | Description | Required |
    | ----- | ----------- | -------- |
    | Unique ID | The unique identifier of the organization. It can't be changed later. | Required |
    | Organization Name | The name, with one field per installed locale. | Required |
    | Contact Information | How to contact the organization, with one field per installed locale. | |
    | Enabled | Whether the organization is active. | |
4.  Click **Submit**. The organization appears in the **Organizations** table.

    ![](<../../../../.gitbook/assets/image (6).png>)

## Editing an organization

Click the pencil icon next to the organization in the **Organizations** table, change the fields and click **Submit**. The Unique ID can't be changed.

## Arranging organizations in a hierarchy

Organizations can have a parent organization, shown in the **Parent** column of the table. For example, provincial health offices could sit under a Ministry of Health.

* Click the **Manage Hierarchy** icon above the table to open the organization tree. Drag an organization onto another one to make it a child, and confirm the move. To make an organization top-level again, choose **Remove from parent**. Click **Close** when you're done.
* Click the **Upload Hierarchy** icon to import an organization hierarchy from a JSON file.
