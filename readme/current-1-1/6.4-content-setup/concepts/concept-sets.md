# Concept Sets

Concept sets define a set of concept classes and edges that together define a formally defined constraint that can be used on data in the system.&#x20;

There are two types of concept sets:

* Enumeration
* Taxonomy

Enumerations define a flat list of data. This is typically how classification options would be defined to restrict the options in a Geo-Object Type attribute.&#x20;

Taxonomies define a hierarchical set of data for when classifications of information are nested in a larger tree of taxonomies. Larger taxonomies may define different levels of data classifications (e.g. residential is on one level with single family and multi-family residential being below that). This enables the ability to select a part of a taxonomy hierarchy that is most relevant to an attribute of a Geo-Object Type while keeping the over all taxonomic data in one place.

Example:&#x20;

If a taxonomy edge type defines the types of human built physical structures (e.g. building, dam, etc...), a concept set can use that to specify that the values of a Geo-Object attribute must be one of those physical structure options. A Geo-Object attribute value of "Dam" will be allowed because it's a type of built physical structure as defined by the taxonomy.

#### Where concept sets be used

A concept set can be specified on a Geo-Object Type when [creating one new](../geo-objects-and-hierarchies/6.4.2-geographic-object-types-outside-a-group/).&#x20;

<mark style="color:$danger;">Pre-requisite: The concept edge type values must be</mark>[ <mark style="color:$danger;">imported</mark> ](../../curate/import-business-data.md)<mark style="color:$danger;">first before adding a concept set to a new Geo-Object Type and before importing Geo-Object data to that type in the system.</mark>

<figure><img src="../../../../.gitbook/assets/image (79).png" alt=""><figcaption></figcaption></figure>

| Form Field          | Description                                                                                                                                                                                                                                                                                                                          |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Code                | <p>Unique ID of the concept set.<br><br>This code is globally unique.</p>                                                                                                                                                                                                                                                            |
| Label               | Label for the concept set.                                                                                                                                                                                                                                                                                                           |
| Description         | Optional description of the concept set.                                                                                                                                                                                                                                                                                             |
| Concept Class       | The concept class to use for this concept set.                                                                                                                                                                                                                                                                                       |
| Concept Edge Type   | The concept edge type to use for this concept set.                                                                                                                                                                                                                                                                                   |
| Discrete Graph Type | <p>The type of taxonomic structure to use for this concept set.</p><ul><li>Enumeration</li><li>Taxonomy<br></li></ul><p>Selecting enumeration specifies a flat list of options.</p><p></p><p>Selecting taxonomy allows you to specify a part of a multi-branched taxonomy by selecting the root node of a larger taxonomy tree. </p> |
| Root Term           | The root node selector to specify the root node of a multi-branched taxonomy. Every option below the selected node will be a valid option.                                                                                                                                                                                           |
