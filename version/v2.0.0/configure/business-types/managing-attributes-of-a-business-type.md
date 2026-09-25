# Managing attributes of a Business Type

{% hint style="info" %}
Registry Administrators can manage the Business Types of their organization.
{% endhint %}

Attributes define the information stored for each business object. Every Business Type has default attributes, such as its code, and you can add custom attributes.

## Adding an attribute

1.  Navigate to the **Business Types** page from the sidebar.

    <figure><img src="../../../../.gitbook/assets/image (98).png" alt=""><figcaption></figcaption></figure>
2.  Click the three-dot menu next to the Business Type and select **Edit**.

    <figure><img src="../../../../.gitbook/assets/image (100).png" alt=""><figcaption></figcaption></figure>
3.  In the **Attributes** section, click **+ Add**.

    <figure><img src="../../../../.gitbook/assets/image (88).png" alt=""><figcaption></figcaption></figure>
4.  The **Add a new attribute** form opens. Select the data type and fill out the form:

    | Field | Description | Required |
    | ----- | ----------- | -------- |
    | Data Type | <p>The type of values the attribute holds: <strong>Text</strong>, <strong>Localized Text</strong> (a value for each installed locale), <strong>Integer</strong>, <strong>Decimal</strong>, <strong>Date</strong> or <strong>Boolean</strong>. The data type is enforced for every value stored in the attribute.</p><p><em>Example: The number of staff at a facility should be an Integer, so values are stored as whole numbers.</em></p> | Required |
    | Code | <p>The unique identifier of the attribute. It can't contain spaces and can't be changed later.</p><p><em>Example: NUMBER_OF_STAFF</em></p> | Required |
    | Label | The display label, with one field per installed locale. The default locale is required. | Required |
    | Description (Abstract) | A description, with one field per installed locale. | |
    | Length (Decimal only) | The total number of digits in the number. The default is 32. | Required |
    | Decimal (Decimal only) | The number of digits to the right of the decimal point. The default is 8. | Required |
    | Is change over time | Select this to keep a history of the attribute's values over time. Each imported value is stored with the start and end dates of its import. It can only be set when the attribute is created. | |

    <figure><img src="../../../../.gitbook/assets/image (1) (2).png" alt=""><figcaption></figcaption></figure>
5.  Click **Submit**. The attribute is saved right away.
6.  To add another attribute, repeat steps 3 to 5.

## Editing or removing an attribute

In the **Attributes** section, each custom attribute has two icons:

* The pencil icon (**Edit**) opens the attribute so you can change its label and description. Its code and data type can't be changed.
* The trash icon (**Remove**) deletes the attribute after you confirm by clicking **Delete**.

Default attributes can't be edited or removed.
