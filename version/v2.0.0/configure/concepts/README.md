# Concepts

A **Concept** is a single, agreed-upon term that describes a kind of thing. Concepts give everyone the same vocabulary, so the same idea is always recorded the same way instead of as free text like "river," "River," or "riv."

Concepts are grouped into **Concept Sets**. A Concept Set can be as simple as a list of allowed values (for example, _Open_, _Closed_, _Under Construction_) or organized into a hierarchy (for example, _Stream_ is a kind of _Waterway_).

Once a Concept exists, you can use it to classify Geo-Object attributes.&#x20;

**How the pieces fit together**

Setting up Concepts involves three things you create in Geoprism Registry, plus the Concepts themselves:

* A **Concept Class** is a template that says what information each Concept has, such as a name, code, or definition.
* A **Concept Edge Type** defines how Concepts can be related, such as "is a" (_Dam_ is a _Structure_).
* The **Concepts** and their relationships are loaded using the Business Data importer.
* A **Concept Set** picks which Concepts are allowed for a Geo-Object Type attribute, either as a flat list or as a branch of a taxonomy. These are assigned to a Geo-Object Type at the time of Geo-Object Type creation.

**Setup order**

1. Create a Concept Class.
2. Create a Concept Edge Type that uses that class.
3. Import your Concepts with the Business Data importer.
4. Create a Concept Set.
5. Use the Concept Set on a Geo-Object Type attribute.



See the [concept-classes.md](concept-classes.md "mention"), [concept-edge-types.md](concept-edge-types.md "mention"), and [concept-sets.md](concept-sets.md "mention") for more detail.

