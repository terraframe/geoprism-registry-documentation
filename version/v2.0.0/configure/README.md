# Configure

The **Configure** part of the sidebar is where you define the structure of your data before you load it. Registry Administrators set this up for their organization.

| Page | What it's for |
| ---- | ------------- |
| [Concepts](concepts/README.md) | Controlled vocabularies and taxonomies used to classify Geo-Objects. |
| [Geo-Objects and Hierarchies](geo-objects-and-hierarchies/README.md) | The kinds of geographic objects you manage, their attributes, and the hierarchies that relate them. |
| [Business Types](business-types/README.md) | Kinds of data that aren't geospatial, and how they relate to each other and to Geo-Objects. |
| [Source Authorities](source-authorities/README.md) | The organizations responsible for your data. |
| [Data Sources](data-sources/README.md) | Where your data comes from, recorded with each import. |

## A typical setup order

1.  Add the [Source Authorities](source-authorities/README.md) and [Data Sources](data-sources/README.md) your data comes from.
2.  If you'll classify Geo-Objects, set up [Concepts](concepts/README.md) first, because a Geo-Object Type's Concept Set can only be chosen when the type is created.
3.  Create your [Geo-Object Types](geo-objects-and-hierarchies/geographic-object-types-outside-a-group/README.md) and [hierarchies](geo-objects-and-hierarchies/hierarchies/README.md).
4.  Create any [Business Types](business-types/README.md) and Business Edge Types you need.
5.  Load your data. See [Curate](../curate/README.md).

{% hint style="info" %}
Organizations are set up by a System Administrator. See [Organization management](../deployment-and-setup/organization-management/README.md).
{% endhint %}
