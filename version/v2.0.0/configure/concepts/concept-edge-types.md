# Concept Edge Types

See [.](./ "mention") for a definition of Concept and general overview.

A Concept Edge Type defines a kind of relationship between Concepts, such as 'Is A.' It specifies which Concept Class the parent and child Concepts belong to. Typically, concept edge types are used to model hierarchical relationships between concepts.  For instance, a concept edge type of 'Is A' can be used to model how different structure types relate to each other. A building is a structure, and residential building is a building. Therefore, a residential building is also a structure.

In most cases, set the parent and child to the same Concept Class. This lets Concepts in the same taxonomy be related to each other.

{% hint style="info" %}
After creation the values of the concept edge type taxonomy must be loaded into the system through the _Import_ [_Business Data_ importer](../../curate/import-business-data.md).\
\
This is how Concepts are added to the registry.
{% endhint %}

### Creating a concept edge type

1. Navigate to Concept Edge Types.
2. Select _Create._
3. Fill out the form and click submit.

<figure><img src="../../../../.gitbook/assets/image (78).png" alt=""><figcaption></figcaption></figure>

| Form Field          | Description                                                                                                                                                                                                                                                                                                                                                                 |
| ------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Code                | <p>Unique ID of the concept edge type.<br><br>This code is globally unique.</p>                                                                                                                                                                                                                                                                                             |
| Label               | Label for the concept edge type.                                                                                                                                                                                                                                                                                                                                            |
| Description         | Optional description of the concept edge type.                                                                                                                                                                                                                                                                                                                              |
| Parent Type         | Parent concept class in the edge relationship.                                                                                                                                                                                                                                                                                                                              |
| Child Type          | Child concept class in the edge relationship.                                                                                                                                                                                                                                                                                                                               |
| Discrete Graph Type | <p>The type of relationship between two concept classes. There is currently only one option.<br>- Taxonomy <br><br>A taxonomy concept edge type is fundamentally a directed acyclic graph (DAG). Defining a concept edge type's discrete graph type as taxonomy specifies that the relationship between the two concept classes is modeled as a DAG of taxonomic data.</p> |
