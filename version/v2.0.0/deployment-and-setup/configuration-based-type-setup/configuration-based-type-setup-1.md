# Geo-Object type definitions

A `<type>` element defines a Geo-Object Type or a group. It goes inside an `<organization>` element.

## XSD definition

```xml
<xs:complexType name="type">
  <xs:sequence>
    <xs:choice minOccurs="0" maxOccurs="unbounded">
      <xs:element name="attributes" type="attributes" minOccurs="0" />
      <xs:element name="group-item" type="group-item" minOccurs="0" maxOccurs="unbounded" />
    </xs:choice>
  </xs:sequence>
  <xs:attribute name="code" type="xs:string" use="required" />
  <xs:attribute name="label" type="xs:string" use="required" />
  <xs:attribute name="description" type="xs:string" use="optional" />
  <xs:attribute name="visibility" type="visibility" use="optional" />
  <xs:attribute name="geometryType" type="geometryType" use="required" />
  <xs:attribute name="isGeometryEditable" type="xs:boolean" />
  <xs:attribute name="isGroup" type="xs:boolean" />
  <xs:attribute name="conceptSet" type="xs:string" use="optional" />
  <xs:attribute name="startDate" type="xs:string" use="optional" />
  <xs:attribute name="endDate" type="xs:string" use="optional" />
  <xs:attribute name="rootTerm" type="xs:string" use="optional" />
</xs:complexType>

<xs:complexType name="group-item">
  <xs:attribute name="code" type="xs:string" use="required" />
  <xs:attribute name="label" type="xs:string" use="required" />
  <xs:attribute name="description" type="xs:string" use="optional" />
</xs:complexType>

<xs:simpleType name="visibility">
  <xs:restriction base="xs:string">
    <xs:enumeration value="PRIVATE" />
    <xs:enumeration value="PUBLIC" />
  </xs:restriction>
</xs:simpleType>

<xs:simpleType name="geometryType">
  <xs:restriction base="xs:string">
    <xs:enumeration value="POINT" />
    <xs:enumeration value="LINE" />
    <xs:enumeration value="POLYGON" />
    <xs:enumeration value="MIXED" />
  </xs:restriction>
</xs:simpleType>
```

| Attribute | Description |
| --------- | ----------- |
| `code`, `label`, `description` | The type's code, label and description. |
| `visibility` | `PUBLIC` or `PRIVATE`. |
| `geometryType` | `POINT`, `LINE`, `POLYGON` or `MIXED`. |
| `isGeometryEditable` | Whether geometries can be edited with the web-based editing tools. |
| `isGroup` | `true` to create a group. Each `<group-item>` inside it creates a Geo-Object Type in the group. |
| `conceptSet`, `startDate`, `endDate`, `rootTerm` | Adds a classification to the type, using the Concept Set with this code. See [Concept Sets](../../configure/concepts/concept-sets.md). |

## Attribute XSD definition <a href="#attribute-xsd-definition" id="attribute-xsd-definition"></a>

Put attributes inside an `<attributes>` element. The same attribute elements are used for Business Types and Concept Classes.

```xml
<xs:complexType name="attributes">
  <xs:choice minOccurs="0" maxOccurs="unbounded">
    <xs:element name="text" type="text" />
    <xs:element name="boolean" type="boolean" />
    <xs:element name="integer" type="integer" />
    <xs:element name="decimal" type="decimal" />
    <xs:element name="date" type="date" />
    <xs:element name="term" type="term" />
  </xs:choice>
</xs:complexType>

<!-- Common attributes of all attributes -->
<xs:attributeGroup name="attribute">
  <xs:attribute name="code" type="xs:string" use="required" />
  <xs:attribute name="label" type="xs:string" />
  <xs:attribute name="description" type="xs:string" />
</xs:attributeGroup>

<xs:attributeGroup name="attributeDec">
  <xs:attributeGroup ref="attribute" />
  <xs:attribute name="precision" type="xs:integer" />
  <xs:attribute name="scale" type="xs:integer" />
</xs:attributeGroup>

<xs:complexType name="text">
  <xs:attributeGroup ref="attribute" />
</xs:complexType>
<xs:complexType name="boolean">
  <xs:attributeGroup ref="attribute" />
</xs:complexType>
<xs:complexType name="integer">
  <xs:attributeGroup ref="attribute" />
</xs:complexType>
<xs:complexType name="decimal">
  <xs:attributeGroup ref="attributeDec" />
</xs:complexType>
<xs:complexType name="date">
  <xs:attributeGroup ref="attribute" />
</xs:complexType>
```

{% hint style="warning" %}
The schema still includes a `term` attribute type with `option` elements, but term attributes aren't imported in this version. Use a Concept Set classification instead.
{% endhint %}

## Example

```xml
<type
    code="Health_facility"
    label="Health facility (MOH)"
    description="Public health facilities under the management of the Ministry of Health"
    visibility="PUBLIC"
    geometryType="POINT"
    isGeometryEditable="true"
    isGroup="true">
  <attributes>
    <text code="PHONE" label="Phone number" />
    <integer code="NUMBER_OF_BEDS" label="Number of beds" />
    <decimal code="ANNUAL_BUDGET" label="Annual budget" precision="12" scale="2" />
    <date code="OPENING_DATE" label="Opening date" />
    <boolean code="HAS_ELECTRICITY" label="Has electricity" />
  </attributes>
  <group-item code="National_hospital" label="National hospital (MOH)" />
  <group-item code="Health_centre" label="Health centre (MOH)" />
  <group-item code="Health_post" label="Health post (MOH)" />
</type>
```
