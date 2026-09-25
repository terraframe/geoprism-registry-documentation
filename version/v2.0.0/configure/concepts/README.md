# Concepts

A **Concept** is a single, agreed-upon term that describes a kind of thing. Concepts give everyone the same vocabulary, so the same idea is always recorded the same way instead of as free text like "river," "River," or "riv."

Concepts are grouped into **Concept Sets**. A Concept Set can be as simple as a list of allowed values (for example, _Open_, _Closed_, _Under Construction_) or organized into a hierarchy (for example, _Stream_ is a kind of _Waterway_).

Once your Concepts are imported, you can use them to classify Geo-Objects.&#x20;

**How the pieces fit together**

Setting up Concepts involves three things you create in Geoprism Registry, plus the Concepts themselves:

* A **Concept Class** is a template that says what information each Concept has, such as a name, code, or definition.
* A **Concept Edge Type** defines how Concepts can be related, such as "is a" (_Dam_ is a _Structure_).
* The **Concepts** are loaded with the [Import Business Data](../../curate/import-business-data.md) page, and the relationships between them are loaded with the [Import Edge Data](../../curate/import-edge-data.md) page.
* A **Concept Set** picks which Concepts are allowed as a Geo-Object Type's classification, either as a flat list or as a branch of a taxonomy. You choose the Concept Set when you create the Geo-Object Type, and it can't be changed later.

All three are managed on the **Concept Classes** page in the sidebar, which has a section for each: **Concept Classes**, **Concept Edge Types** and **Concept Sets**.

**Setup order**

1. Create a Concept Class.
2. Create a Concept Edge Type that uses that class.
3. Import your Concepts on the Import Business Data page, choosing **Concept Object** and your Concept Class.
4. Import the relationships between your Concepts on the Import Edge Data page, choosing your Concept Edge Type.
5. Create a Concept Set.
6. Create a Geo-Object Type and select the Concept Set. This adds a **classification** attribute to the type.
7. When you import Geo-Object data, map a column in your file to the **classification** field.



See the [concept-classes.md](concept-classes.md "mention"), [concept-edge-types.md](concept-edge-types.md "mention"), and [concept-sets.md](concept-sets.md "mention") for more detail.

