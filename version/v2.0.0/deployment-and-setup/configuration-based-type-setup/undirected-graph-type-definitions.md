# Undirected graph type definitions

Put `<undirected-graph>` elements inside an `<organization>` element. In the schema, directed acyclic graph and undirected graph types share one type definition, named `graph`, with the same attributes shown below.

{% hint style="info" %}
This file only creates the graph type. To load the relationships between Geo-Objects, use [Import Edge Data](../../curate/import-edge-data.md) or the [API](../../external-system-integration/available-apis.md).
{% endhint %}

## XSD definition <a href="#xsd-definition.3" id="xsd-definition.3"></a>

```
<xs:complexType name="undirected-graph">
    <xs:attribute name="code" type="xs:string" use="required" />
    <xs:attribute name="label" type="xs:string" use="required" />
    <xs:attribute name="description" type="xs:string" use="optional" />
  </xs:complexType>
```

Example:

```
<undirected-graph
    code="ADJECENT_TO"
    label="Adjecent To (MOH)"
    description="Links locations which are adjecent to each other"/>  
```

Some example files can be accessed here:

{% file src="../../../../.gitbook/assets/tolkien-moh.xml" %}

{% file src="../../../../.gitbook/assets/tolkien-moha.xml" %}
