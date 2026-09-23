# Concept Edge Types

Concept edge types define how concept classes can relate to each other. Typically, concept edge types are used to model hierarchical relationships between concepts.  For instance, a concept edge type of 'Is A' can be used to model how different structure types relate to each other. A building is a structure, and residential building is a building. Therefore, a residential building is also a structure.

Most use cases will create an edge where the parent and child concept classes are the same. This specifies that a concept edge type that has the same concept class set for the parent and child options will allow relationships between nodes in the same taxonomy tree.

NOTE: After creation the values of the concept edge type taxonomy must be loaded into the system through the _Import_ [_Business Data_ importer](../../curate/import-business-data.md).

### Creating a concept edge type

1. Navigate to Concept Edge Types.
2. Select _Create._
3. Fill out the form and click submit.

<figure><img src="../../../../.gitbook/assets/image (78).png" alt=""><figcaption></figcaption></figure>

| Form Field          | Description                                                                                                                                                                                                                                                                                                                                                                |
| ------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Code                | <p>Unique ID of the concept edge type.<br><br>This code is globally unique.</p>                                                                                                                                                                                                                                                                                            |
| Label               | Label for the concept edge type.                                                                                                                                                                                                                                                                                                                                           |
| Description         | Optional description of the concept edge type.                                                                                                                                                                                                                                                                                                                             |
| Parent Type         | Parent concept class in the edge relationship.                                                                                                                                                                                                                                                                                                                             |
| Child Type          | Child concept class in the edge relationship.                                                                                                                                                                                                                                                                                                                              |
| Discrete Graph Type | <p>The type of relationship between two concept classes. There is currently only one option.<br>- Taxonomy <br><br>A taxonomy concept edge type is fundamentally a directed acyclic graph (DAG). Defining a concept edge types discrete graph type as taxonomy specifies that the relationship between the two concept classes are modeled as a DAG of taxonomic data.</p> |
