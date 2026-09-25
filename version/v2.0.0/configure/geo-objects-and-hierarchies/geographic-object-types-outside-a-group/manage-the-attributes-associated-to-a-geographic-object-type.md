# Managing the attributes of a Geo-Object Type

{% hint style="info" %}
Registry Administrators can manage the attributes of the Geo-Object Types under the curation mandate of their organization
{% endhint %}

Every Geo-Object Type has default attributes, such as its code and label. You can add custom attributes to store more information about each Geo-Object.

## Adding an attribute

1.  Navigate to the **Geo-Objects and Hierarchies** page from the sidebar.

    <figure><img src="../../../../../.gitbook/assets/image (84).png" alt=""><figcaption></figcaption></figure>
2.  Click the three-dot menu next to the Geo-Object Type and select **Edit**.

    <figure><img src="../../../../../.gitbook/assets/image (82).png" alt=""><figcaption></figcaption></figure>
3.  In the **Attributes** section, click **+ Add**.

    <figure><img src="../../../../../.gitbook/assets/image (88).png" alt=""><figcaption></figcaption></figure>
4.  The **Add a new attribute** form opens. Select the data type and fill out the form:

    | Field | Description | Required |
    | ----- | ----------- | -------- |
    | Data Type | <p>The type of values the attribute holds: <strong>Text</strong>, <strong>Localized Text</strong> (a value for each installed locale), <strong>Integer</strong>, <strong>Decimal</strong>, <strong>Date</strong> or <strong>Boolean</strong>. The data type is enforced for every value stored in the attribute.</p><p><em>Example: The number of beds in a health facility should be an Integer, so values are stored as whole numbers.</em></p> | Required |
    | Code | <p>The unique identifier of the attribute. It can't contain spaces and can't be changed later.</p><p><em>Example: NUMBER_OF_BEDS</em></p> | Required |
    | Label | The display label, with one field per installed locale. The default locale is required. | Required |
    | Description (Abstract) | A description, with one field per installed locale. | |
    | Length (Decimal only) | The total number of digits in the number. The default is 32. | Required |
    | Decimal (Decimal only) | The number of digits to the right of the decimal point. The default is 8. | Required |

    <figure><img src="../../../../../.gitbook/assets/image (1) (2).png" alt=""><figcaption></figcaption></figure>
5.  Click **Submit**. The attribute is saved right away.
6.  To add another attribute, repeat steps 3 to 5.

{% hint style="info" %}
Term and Classification attributes can't be added from this form. A **classification** attribute is added when you choose a Concept Set while [creating the Geo-Object Type](add-a-geographic-object-type.md).
{% endhint %}

## Editing or removing an attribute

In the **Attributes** section, each custom attribute has two icons:

* The pencil icon (**Edit**) opens the attribute so you can change its label and description. Its code and data type can't be changed.
* The trash icon (**Remove**) deletes the attribute after you confirm by clicking **Delete**.

Default attributes can't be edited or removed.
