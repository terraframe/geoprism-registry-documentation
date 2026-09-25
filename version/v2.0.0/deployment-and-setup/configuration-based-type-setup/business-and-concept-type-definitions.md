# Business and Concept type definitions

These elements go inside an `<organization>` element, like `<type>` and `<hierarchy>`. Business Types and Concept Classes use the same [attribute elements](configuration-based-type-setup-1.md#attribute-xsd-definition) as Geo-Object Types.

## XSD definition

```xml
<!-- Used by both <business-type> and <concept-class> -->
<xs:complexType name="business-type">
  <xs:sequence>
    <xs:choice minOccurs="0" maxOccurs="unbounded">
      <xs:element name="attributes" type="attributes" minOccurs="0" />
    </xs:choice>
  </xs:sequence>
  <xs:attribute name="code" type="xs:string" use="required" />
  <xs:attribute name="label" type="xs:string" use="required" />
  <xs:attribute name="description" type="xs:string" use="optional" />
  <xs:attribute name="labelAttribute" type="xs:string" use="optional" />
</xs:complexType>

<xs:complexType name="business-edge">
  <xs:attribute name="code" type="xs:string" use="required" />
  <xs:attribute name="label" type="xs:string" use="required" />
  <xs:attribute name="description" type="xs:string" use="optional" />
  <xs:attribute name="parentTypeCode" type="xs:string" use="optional" />
  <xs:attribute name="childTypeCode" type="xs:string" use="optional" />
</xs:complexType>

<xs:complexType name="concept-edge">
  <xs:attribute name="code" type="xs:string" use="required" />
  <xs:attribute name="label" type="xs:string" use="required" />
  <xs:attribute name="description" type="xs:string" use="optional" />
  <xs:attribute name="parentTypeCode" type="xs:string" use="optional" />
  <xs:attribute name="childTypeCode" type="xs:string" use="optional" />
  <xs:attribute name="discreteType" type="xs:string" use="optional" />
</xs:complexType>

<xs:complexType name="concept-set">
  <xs:attribute name="code" type="xs:string" use="required" />
  <xs:attribute name="label" type="xs:string" use="required" />
  <xs:attribute name="description" type="xs:string" use="optional" />
  <xs:attribute name="conceptClass" type="xs:string" use="optional" />
  <xs:attribute name="conceptEdgeType" type="xs:string" use="optional" />
  <xs:attribute name="discreteType" type="xs:string" use="optional" />
</xs:complexType>
```

| Element | Creates | Notes |
| ------- | ------- | ----- |
| `<business-type>` | A [Business Type](../../configure/business-types/README.md) | `labelAttribute` is the code of the attribute used as each business object's label. |
| `<concept-class>` | A [Concept Class](../../configure/concepts/concept-classes.md) | Uses the same structure as `<business-type>`. |
| `<business-edge>` | A [Business Edge Type](../../configure/business-types/business-edge-types.md) | `parentTypeCode` and `childTypeCode` are the codes of the Business Types at each end. |
| `<concept-edge>` | A [Concept Edge Type](../../configure/concepts/concept-edge-types.md) | `parentTypeCode` and `childTypeCode` are Concept Class codes. `discreteType` is required in practice; use `TAXONOMY`. |
| `<concept-set>` | A [Concept Set](../../configure/concepts/concept-sets.md) | `conceptClass` and `conceptEdgeType` are codes. `discreteType` is required in practice: `ENUMERATION` or `TAXONOMY`. For a taxonomy, the importer also reads a `rootTerm` attribute with the code of the root Concept, although it isn't in the schema. |

Define Concept Classes and Concept Edge Types before the Concept Sets that use them, and Concept Sets before the Geo-Object Types that use them.

## Example

```xml
<organization code="USACE">
  <concept-class code="StructureType" label="Structure type">
    <attributes>
      <text code="DEFINITION" label="Definition" />
    </attributes>
  </concept-class>
  <concept-edge code="IS_A" label="Is a" parentTypeCode="StructureType" childTypeCode="StructureType" discreteType="TAXONOMY" />
  <concept-set code="STRUCTURE_TYPES" label="Structure types" conceptClass="StructureType" conceptEdgeType="IS_A" discreteType="TAXONOMY" rootTerm="Structure" />

  <business-type code="Staff" label="Staff" labelAttribute="NAME">
    <attributes>
      <text code="NAME" label="Name" />
    </attributes>
  </business-type>
</organization>
```
