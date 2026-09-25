# Configuration-based type setup

Geoprism Registry can create types from an XML file instead of the user interface. This is useful for setting up a new instance quickly, or copying types from one instance to another. The file can define:

* [Geo-Object Types](configuration-based-type-setup-1.md), including groups and their attributes
* [Hierarchies](hierarchy-type-definitions.md)
* [Directed acyclic graph types](directed-acyclic-graph-type-definitions.md) and [undirected graph types](undirected-graph-type-definitions.md)
* [Business Types, Business Edge Types, Concept Classes, Concept Edge Types and Concept Sets](business-and-concept-type-definitions.md)

{% hint style="warning" %}
Importing type definitions can only be done by a System Administrator.
{% endhint %}

## File structure

The root element is `<CGR>`. It contains one `<organization>` element for each organization, whose `code` is the organization's Unique ID. The types go inside the organization that will manage them:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<CGR>
  <organization code="MOH">
    <type code="Health_facility" label="Health facility (MOH)" geometryType="POINT" />
    <hierarchy code="HEALTH_FACILITY_HIERARCHY" label="Health facility hierarchy (MOH)">
      <child code="Health_facility" />
    </hierarchy>
  </organization>
</CGR>
```

When you import a file, you choose one organization, and only the types inside that organization's element are imported.

The structure of each element is described with XSD (XML Schema Definition) on the pages in this section. Geoprism Registry doesn't check the file against the schema when it's imported, so check your file carefully before you import it.

For complete examples, see the files attached to [undirected-graph-type-definitions.md](undirected-graph-type-definitions.md "mention"). To start from an existing instance, export its types. See [configuration-based-type-setup.md](configuration-based-type-setup.md "mention").
