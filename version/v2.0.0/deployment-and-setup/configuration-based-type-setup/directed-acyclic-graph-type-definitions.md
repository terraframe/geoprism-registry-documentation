# Directed acyclic graph type definitions

Put `<dag>` elements inside an `<organization>` element. In the schema, directed acyclic graph and undirected graph types share one type definition, named `graph`, with the same attributes shown below.

{% hint style="info" %}
This file only creates the graph type. To load the relationships between Geo-Objects, use [Import Edge Data](../../curate/import-edge-data.md) or the [API](../../external-system-integration/available-apis.md).
{% endhint %}

## XSD definition <a href="#xsd-definition.2" id="xsd-definition.2"></a>

```
<xs:complexType name="dag">
    <xs:attribute name="code" type="xs:string" use="required" />
    <xs:attribute name="label" type="xs:string" use="required" />
    <xs:attribute name="description" type="xs:string" use="optional" />
  </xs:complexType>
```

Example:

```
<dag
    code="FLOWS_INTO"
    label="Flows Into (MOH)"
    description=" This DAG links bodies of water which flow into other bodies of water"/>  
```
