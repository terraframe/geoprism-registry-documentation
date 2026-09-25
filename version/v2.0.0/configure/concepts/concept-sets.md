# Concept Sets

See [.](./ "mention") for a definition of Concept and general overview.

A Concept Set defines the allowed values for a Geo-Object Type attribute, drawn from your imported Concepts. Each Concept Set is defined by a set of concept classes and concept edge types.

There are two types of concept sets:

* Enumeration
* Taxonomy

Enumerations define a flat list of data. This is typically how classification options would be defined to restrict the options in a Geo-Object Type attribute.&#x20;

Taxonomies define a hierarchical set of data for when classifications of information are nested in a larger tree of taxonomies. Larger taxonomies may define different levels of data classifications (e.g. residential is on one level with single family and multi-family residential being below that). This enables the ability to select a part of a taxonomy hierarchy that is most relevant to an attribute of a Geo-Object Type while keeping the over all taxonomic data in one place.

Example:&#x20;

If a taxonomy edge type and the imported concept edges define the types of human built physical structures (e.g. building, dam, etc...), a concept set can package them together. That concept set can then be assigned to a Geo-Object Type and used during import to specify that the values of a Geo-Object attribute must be one of those physical structure options. A Geo-Object attribute value of "Dam" will be allowed because it's a type of built physical structure as defined by the taxonomy.

#### Where concept sets are used

A concept set can be specified on a Geo-Object Type when [creating one new](../geo-objects-and-hierarchies/geographic-object-types-outside-a-group/) and used during import to apply a constraint to an attribute on the data.

{% hint style="warning" %}
Pre-requisite: The concept edge type values must be [imported](../../curate/import-business-data.md) first before adding a concept set to a new Geo-Object Type and before importing Geo-Object data to that type in the system.
{% endhint %}

<figure><img src="../../../../.gitbook/assets/image (79).png" alt=""><figcaption></figcaption></figure>

| Form Field          | Description                                                                                                                                                                                                                                                                                                                          |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Code                | <p>Unique ID of the concept set.<br><br>This code is globally unique.</p>                                                                                                                                                                                                                                                            |
| Label               | Label for the concept set.                                                                                                                                                                                                                                                                                                           |
| Description         | Optional description of the concept set.                                                                                                                                                                                                                                                                                             |
| Concept Class       | The concept class to use for this concept set.                                                                                                                                                                                                                                                                                       |
| Concept Edge Type   | The concept edge type to use for this concept set.                                                                                                                                                                                                                                                                                   |
| Discrete Graph Type | <p>The type of taxonomic structure to use for this concept set.</p><ul><li>Enumeration</li><li>Taxonomy<br></li></ul><p>Selecting enumeration specifies a flat list of options.</p><p></p><p>Selecting taxonomy allows you to specify a part of a multi-branched taxonomy by selecting the root node of a larger taxonomy tree. </p> |
| Root Term           | The root node selector to specify the root node of a multi-branched taxonomy. That root node and every option below it will be a valid option.                                                                                                                                                                                       |
