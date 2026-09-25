# Concept Edge Types

See [.](./ "mention") for a definition of Concept and general overview.

A Concept Edge Type defines a kind of relationship between Concepts, such as 'Is A.' It specifies which Concept Class the parent and child Concepts belong to. Typically, concept edge types are used to model hierarchical relationships between concepts.  For instance, a concept edge type of 'Is A' can be used to model how different structure types relate to each other. A building is a structure, and residential building is a building. Therefore, a residential building is also a structure.

In most cases, set the parent and child to the same Concept Class. This lets Concepts in the same taxonomy be related to each other.

{% hint style="info" %}
After you create a Concept Edge Type, load the relationships between your Concepts on the [Import Edge Data](../../curate/import-edge-data.md) page.\
\
The Concepts themselves must already be in the registry. Import them first on the [Import Business Data](../../curate/import-business-data.md) page, choosing **Concept Object**.
{% endhint %}

{% hint style="info" %}
Registry Administrators can create Concept Edge Types for their organization. Only a System Administrator can edit or delete them.
{% endhint %}

## Creating a Concept Edge Type

1.  Navigate to the **Concept Classes** page from the sidebar. The page has three sections, **Concept Classes**, **Concept Edge Types** and **Concept Sets**, which you choose at the top of the list. Select **Concept Edge Types**.
2.  Click **Create** under your organization.
3.  Fill out the form:

    <figure><img src="../../../../.gitbook/assets/image (78).png" alt=""><figcaption></figcaption></figure>

    | Field | Description | Required |
    | ----- | ----------- | -------- |
    | Code | The unique identifier of the Concept Edge Type. It can't be changed later. | Required |
    | Label | The display label, with one field per installed locale. | Required |
    | Description (Abstract) | A description, with one field per installed locale. | |
    | Parent Type | The Concept Class of the parent Concept in each relationship. It can't be changed later. | Required |
    | Child Type | The Concept Class of the child Concept in each relationship. It can't be changed later. | Required |
    | Discrete Graph Type | <p>The kind of relationship. There's currently one option, <strong>Taxonomy</strong>. A taxonomy is a directed acyclic graph (DAG): each Concept can have parents and children, but a Concept can never be its own ancestor. It can't be changed later.</p> | Required |
4.  Click **Submit**.

## Editing or deleting a Concept Edge Type

Click the three-dot menu next to the Concept Edge Type:

* **Edit** lets you change its label and description, then click **Submit**.
* **Delete** removes it after you confirm.
* **Import History** lists the imports into it.
