# Rapid domain setup

GeoPrism Registry supports automatically building Geo-Object Types, Hierarchies, directed acyclic graphs, and undirected graphs using configurations defined in XML. This is useful for quickly setting up a GeoPrism Registry instance.

## Geo-Object Type definitions <a href="#geo-object-type-definitions" id="geo-object-type-definitions"></a>

### XSD Definition

```
// <xs:complexType name="type">
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
  </xs:complexType>
```

### Attribute XSD Definition <a href="#attribute-xsd-definition" id="attribute-xsd-definition"></a>

```
// <!-- Common Attributes of all attributes -->
  <xs:attributeGroup name="attribute">
    <!-- name: The name of the attribute -->
    <xs:attribute name="code" type="xs:string" use="required" />
    <!-- label:The display label of the attribute -->
    <xs:attribute name="label" type="xs:string" />
    <!-- description: A description of the purpose of attribute -->
    <xs:attribute name="description" type="xs:string" />
  </xs:attributeGroup>
  <xs:complexType name="text">
    <xs:attributeGroup ref="attribute" />
  </xs:complexType>
  <xs:complexType name="term">
    <xs:sequence minOccurs="0" maxOccurs="unbounded">
      <xs:element name="option">
        <xs:complexType>
          <xs:attribute name="code" type="xs:string" use="required" />
          <!-- label:The display label of the attribute -->
          <xs:attribute name="label" type="xs:string" />
          <!-- description: A description of the purpose of attribute -->
          <xs:attribute name="description" type="xs:string" />
        </xs:complexType>
      </xs:element>
    </xs:sequence>
    <xs:attributeGroup ref="attribute" />
  </xs:complexType>
  <xs:complexType name="classification">
    <xs:attributeGroup ref="attributeClassification" />
  </xs:complexType>
  <xs:attributeGroup name="attributeClassification">
    <xs:attributeGroup ref="attribute" />
    <xs:attribute name="root" type="xs:string" use="required" />
    <xs:attribute name="classificationType" type="xs:string" use="required" />
  </xs:attributeGroup>
  <xs:attributeGroup name="attributeDec">
    <xs:attributeGroup ref="attribute" />
    <xs:attribute name="precision" type="xs:integer" />
    <xs:attribute name="scale" type="xs:integer" />
  </xs:attributeGroup>
  <!-- Represents a Boolean object in the database -->
  <xs:complexType name="boolean">
    <xs:attributeGroup ref="attribute" />
  </xs:complexType>
  <!-- Represents a Double object in the database -->
  <xs:complexType name="integer">
    <xs:attributeGroup ref="attribute" />
  </xs:complexType>
  <!-- Represents a Decimal object in the database -->
  <xs:complexType name="decimal">
    <xs:attributeGroup ref="attributeDec" />
  </xs:complexType>
  <!-- Represents a Date object in the database -->
  <xs:complexType name="date">
    <xs:attributeGroup ref="attribute" />
  </xs:complexType>

```

#### Example

```
// <type
    code="Health_facility"
    label="Health facility (MOH)"
    description="Public health facilities under the management of the Ministry of Health"
    visibility="PUBLIC"
    geometryType="POINT"
    isGeometryEditable="true">
    <attributes>
      <term
        code="COOR_ACU"
        label="Coordinates accuracy">
        <option
          code="COA1"
          label="Unknown" />
        <option
          code="COA2"
          label="Low" />
        <option
          code="COA3"
          label="Moderate" />
        <option
          code="COA4"
          label="High" />
      </term>
      <term
        code="SOUR_COOR"
        label="Coordinates source">
        <option
          code="SCO1"
          label="Unknown" />
        <option
          code="SCO2"
          label="Low" />
        <option
          code="SCO3"
          label="MOH (GPS)" />
        <option
          code="COA4"
          label="UN (google Map)" />
      </term>
      <term
        code="HF_OWN"
        label="Health facility Ownership">
        <option
          code="HFO1"
          label="Unknown" />
        <option
          code="HFO2"
          label="Government" />
        <option
          code="HFO3"
          label="Private" />
      </term>
      <text
        code="HD_NA_EN"
        label="Health facility head name"
        description="Full name of the health facility head in English" />
      <text
        code="HD_PS_EN"
        label="Health facility head position"
        description="Position of the health facility head in English" />
      <text
        code="D_NBR_G"
        label="Health facility phone number"
        description="General phone number of the health facility" />
      <term
        code="HF_T"
        label="Health facility type">
        <option
          code="HFT1"
          label="Unknown" />
        <option
          code="HFT2"
          label="National Hospital" />
        <option
          code="HFT3"
          label="Referral Hospital" />
        <option
          code="HFT4"
          label="Health Centre" />
        <option
          code="HFT5"
          label="Health Post" />
      </term>
      <text
        code="HF_OWN_G"
        label="Name governmental agency (ownership)"
        description="Name of the governmental agency managing the health facility" />
    </attributes>
    <group-item
      code="Referral_hospital"
      label="Referral Hospital (MOH)"
      description="Health facility were general care diagnostic services, limited surgical procedure and access to specialist consultation for patients referred from health centers are being provided" />
    <group-item
      code="National_hospital"
      label="National Hospital (MOH)"
      description="Health facility providing the same services as a referral hospital as well as a range of more highly specialized services" />
    <group-item
      code="Health_post"
      label="Health Post (MOH)"
      description="Health facility were only primary health care are being provided" />
    <group-item
      code="Health_centre"
      label="Health Centre (MOH)"
      description="Health facility were enhanced level of care is being provided" />
  </type>
```

## Hierarchy Type Definitions <a href="#hierarchy-type-definitions" id="hierarchy-type-definitions"></a>

### XSD Definition <a href="#xsd-definition.1" id="xsd-definition.1"></a>

```
// <xs:complexType name="hierarchy">
    <xs:sequence>
      <xs:choice minOccurs="0" maxOccurs="unbounded">
        <xs:element name="child" type="node" minOccurs="1" />
      </xs:choice>
    </xs:sequence>  
    <xs:attribute name="code" type="xs:string" use="required" />
    <xs:attribute name="label" type="xs:string" use="required" />
    <xs:attribute name="description" type="xs:string" use="optional" />
    <xs:attribute name="progress" type="xs:string" use="optional" />
    <xs:attribute name="acknowledgement" type="xs:string" use="optional" />
    <xs:attribute name="disclaimer" type="xs:string" use="optional" />
    <xs:attribute name="accessConstraints" type="xs:string" use="optional" />
    <xs:attribute name="useConstraints" type="xs:string" use="optional" />
    <xs:attribute name="extends" type="xs:string" use="optional" />
  </xs:complexType>
```

#### Example

```
// <hierarchy
    code="Health_geo"
    label="Health geography hierarchy (MOH)"
    description=" This hierarchy allows to link each health facility with the Shire in which it is located"
    progress="Final"
    disclaimer="This hierarchy is being distributed without warranty of any kind, either expressed or implied. The responsibility for the interpretation and use of the dataset lies with the user. In no event shall the Ministry of Health be liable for damages arising from its use"
    accessConstraints="The access to this hiearchy is limited  to the users of the Common Geo-Registry tool for demonstrations purposes only"
    useConstraints="The use of this hierarchy is limited  to the to the users of the Common Geo-Registry tool for demonstrations purposes only"
    acknowledgement="Please acknowledge the Department of Planning, Ministry of Health of the Middle Earth when using this hierarchy"
    extends="ADM_H">
    <child code="SHR">
      <child code="Health_facility" />
    </child>
  </hierarchy>

```

## Directed Acyclic Graph Type Definitions <a href="#directed-acyclic-graph-type-definitions" id="directed-acyclic-graph-type-definitions"></a>

### XSD Definition <a href="#xsd-definition.2" id="xsd-definition.2"></a>

```
// <xs:complexType name="dag">
    <xs:attribute name="code" type="xs:string" use="required" />
    <xs:attribute name="label" type="xs:string" use="required" />
    <xs:attribute name="description" type="xs:string" use="optional" />
  </xs:complexType>
```

#### Example

```
// <dag
    code="FLOWS_INTO"
    label="Flows Into (MOH)"
    description=" This DAG links bodies of water which flow into other bodies of water"/>  
```

### Undirected Graph Type Definitions <a href="#undirected-graph-type-definitions" id="undirected-graph-type-definitions"></a>

### XSD Definition <a href="#xsd-definition.3" id="xsd-definition.3"></a>

```
// <xs:complexType name="undirected-graph">
    <xs:attribute name="code" type="xs:string" use="required" />
    <xs:attribute name="label" type="xs:string" use="required" />
    <xs:attribute name="description" type="xs:string" use="optional" />
  </xs:complexType>
```

#### Example

```
// <undirected-graph
    code="ADJECENT_TO"
    label="Adjecent To (MOH)"
    description="Links locations which are adjecent to each other"/>  
```

{% file src="../../../.gitbook/assets/tolkien-moh.xml" %}

{% file src="../../../.gitbook/assets/tolkien-moha.xml" %}
