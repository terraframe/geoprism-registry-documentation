# Add a Data Source

{% hint style="info" %}
Every Data Source must name a Source Authority. If the organization responsible for the data isn't listed yet, [add a Source Authority](../source-authorities/add-a-source-authority.md) first.
{% endhint %}

1.  Navigate to the **Data Sources** page from the sidebar.

    <figure><img src="../../../../.gitbook/assets/image (105).png" alt=""><figcaption></figcaption></figure>
2.  Click **Add Data Source** and fill out the form:

    <figure><img src="../../../../.gitbook/assets/image (106).png" alt=""><figcaption></figcaption></figure>

    | Field | Description | Required |
    | ----- | ----------- | -------- |
    | Code | The unique human-readable identifier of the Data Source. It can't be changed later. | Required |
    | Label | The display label, with one field per installed locale. The default locale is used when another language is selected but has no label. | Required |
    | Description (Abstract) | A description, with one field per installed locale. | |
    | URI | A link to the source of the data, such as a dataset's web page or download address. | |
    | Governance Level | <p>How the data is governed:</p><ul><li>Authoritative</li><li>Official</li><li>Community Curated</li><li>Research</li><li>Derived</li><li>Experimental</li><li>Ad Hoc</li></ul> | |
    | Metadata Profile | <p>The metadata standard the source uses to describe its data:</p><ul><li>DCAT</li><li>GeoDCAT</li><li>ISO19115</li><li>STAC</li><li>SensorML</li><li>FHIR</li><li>Data Cite</li><li>Custom</li><li>Ad Hoc</li><li>None</li></ul> | |
    | Source Authority | The [Source Authority](../source-authorities/README.md) responsible for this data. | Required |
3.  Click **Submit**.
