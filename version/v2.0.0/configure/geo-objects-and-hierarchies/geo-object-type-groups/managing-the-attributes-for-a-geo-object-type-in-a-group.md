# Managing the attributes for a Geo-Object Type in a group

{% hint style="info" %}
Registry Administrators can manage the attributes of groups under the curation mandate of their organization
{% endhint %}

Attributes you add to a group apply to every Geo-Object Type in the group. To add an attribute to just one Geo-Object Type in the group, edit that Geo-Object Type instead.

1.  Navigate to the **Geo-Objects and Hierarchies** page from the sidebar.
2.  Click the three-dot menu next to the group and select **Edit**.

    <figure><img src="../../../../../.gitbook/assets/image (82).png" alt=""><figcaption></figcaption></figure>
3.  In the **Attributes** section, click **+ Add**.

    <figure><img src="../../../../../.gitbook/assets/image (8) (1) (1).png" alt=""><figcaption></figcaption></figure>
4.  The **Add a new attribute** form opens. Select the data type and fill out the form:

    | Field | Description | Required |
    | ----- | ----------- | -------- |
    | Data Type | <p>The type of values the attribute holds: <strong>Text</strong>, <strong>Localized Text</strong> (a value for each installed locale), <strong>Integer</strong>, <strong>Decimal</strong>, <strong>Date</strong> or <strong>Boolean</strong>. The data type is enforced for every value stored in the attribute.</p><p><em>Example: The number of beds in a health facility should be an Integer, so values are stored as whole numbers.</em></p> | Required |
    | Code | <p>The unique identifier of the attribute. It can't contain spaces and can't be changed later.</p><p><em>Example: NUMBER_OF_BEDS</em></p> | Required |
    | Label | The display label, with one field per installed locale. The default locale is required. | Required |
    | Description (Abstract) | A description, with one field per installed locale. | |
    | Length (Decimal only) | The total number of digits in the number. The default is 32. | Required |
    | Decimal (Decimal only) | The number of digits to the right of the decimal point. The default is 8. | Required |

    <figure><img src="https://lh5.googleusercontent.com/FVXOBtSvWqQdrzn7g-wLHDFXjnO5G0DrOX9FNHbxvrSw2mTVFgX2Xid3WXr2Ey3-oSwk3aXvi5RL2zgSU1dlXkXRrAp42koraX4wp81OsmDlzUYQSyuAWKu8itY1EeeQkp0p9vxCpKG1X6QSfRRXO9jTQqvs40XGtBH6w-ur1S4AeYHscGyZzGMl" alt=""><figcaption></figcaption></figure>

5.  Click **Submit**. The attribute is saved right away.
6.  To add another attribute, repeat steps 3 to 5.

To edit or remove an attribute, see [Editing or removing an attribute](../geographic-object-types-outside-a-group/manage-the-attributes-associated-to-a-geographic-object-type.md#editing-or-removing-an-attribute).
