# Import a Shapefile

{% hint style="info" %}
Registry Administrators and Registry Maintainers can import the lists and spatial data of the Geo-Object Types under the curation mandate of their organization
{% endhint %}

Spatial data is imported into Geoprism Registry through shapefiles.

To be able to smoothly import shapefiles into Geoprism Registry, these basic requirements must be followed:

* The spatial data must be in [shapefile](https://support.esri.com/en/white-paper/279) format.
* As a shapefile consists of multiple files that collectively make up a shapefile, these files must be compressed into a zipped (.zip) file before importing.
* The shapefile must include data only for a single Geo-Object Type.
* The shapefile must be unprojected ([World Geodetic System 1984; EPSG:4326](https://epsg.io/4326)). Otherwise, Geoprism Registry will give an error message and the import will not take place.

Shapefiles are imported as follows:

1. Navigate to the _Import_ _Geospatial Data page in the sidebar._

<figure><img src="../../../../.gitbook/assets/image (108).png" alt=""><figcaption></figcaption></figure>

2. Click on the **Import Shapefile** tab.

<figure><img src="../../../../.gitbook/assets/image (8) (2).png" alt=""><figcaption></figcaption></figure>

3. Fill out the following fields for the shapefile you would like to import:

| Field              | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              | Required |
| ------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | -------- |
| Hierarchy          | The hierarchy the Geo-Object Type for which you are importing a shapefile belongs to. The dropdown list of hierarchies will depend on the hierarchies created for the organization you are a part of.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | Required |
| Geo-Object Type    | The Geo-Object Type of the shapefile you would like to import. The dropdown list of Geo-Object Types will depend on the hierarchy selected in the _Hierarchy_ field.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | Required |
| Import Strategy    | <p>The import strategy for the shapefile being imported:</p><ul><li><em>New and update:</em> This will import the Geo-Objects in the shapefile that are not yet in Geoprism Registry as well as overwrite the attributes of Geo-Objects from the shapefile that are already in Geoprism Registry.</li><li><em>New only:</em> This will import only the Geo-Objects from the shapefile that are not yet in Geoprism Registry. If the imported file contains Geo-Objects that are already in Geoprism Registry (same unique identifier and/or label depending on what is selected during matching) then the import will fail to avoid creating duplicates.</li><li><em>Update only:</em> This will overwrite the attributes of the Geo-Objects from the list that are already in Geoprism Registry. If the imported file contains Geo-Objects that are not yet in Geoprism Registry, these will not be imported.</li></ul> | Required |
| Start Date         | The start of the date of validity of the Geo-Objects in the shapefile. All the Geo-Objects in the shapefile being imported, whether new or for update, should have the same start date of validity.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | Required |
| End Date           | The end of the date of validity of the Geo-Objects in the shapefile. All the Geo-Objects in the shapefile being imported, whether new or for update, should have the same end date of validity. If the shapefile is still valid on the date it is being imported in Geoprism Registry, click the **Set as most current** button.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         | Required |
| Import blank cells | Selecting this option ensures that if there are empty cells in the list being imported, they are imported as empty attribute values (overwrite). This option gives more control to ensure that updates will either only update cells with values or to overwrite existing values with _null_ values.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |          |

<figure><img src="https://lh3.googleusercontent.com/yGMQl8P3jzfSorz_rFV_EOfJ6MJDzLG629sT6eAUgrKr-TlkSBud_ygqeIqIMUY2TybEAkFSuNelEnHjqcNT4x7LeB7Lbq3FSssRnYwBXUXJ_wMyxZX6rE8yjqBLAqfmEoan71rNmwjYSvJ8nAhmKNyMhnE7PEZkGFCDEnUXRRYP67FmTu7LfpfTRw" alt=""><figcaption></figcaption></figure>

4. Click the **Choose file** button and select the shapfile you'd like to download.
5.  The _Attribute Matching_ window opens containing the attributes for the Geo-Object Type. The number of attributes that appears depends on the number of attributes created for the Geo-Object Type for which the shapefile is being imported. In the dropdown option for each field, choose the attribute from the shapefile being imported that matches the created attribute of the Geo-Object Type. Click the **Next** button.<br>

    <figure><img src="../../../../.gitbook/assets/Screenshot from 2026-09-23 15-39-55.png" alt=""><figcaption></figcaption></figure>

    \
    _Note:_ When the shapefile is formatted correctly and completely, you should be able to match all of its attributes to the Geo-Object Type for which it is being imported. Otherwise, some of the attributes will be left blank.<br>
6.  The Alternative ID Mapping window opens providing an opportunity to add (optional) a mapping to additional ID columns from the shapefile so that can be included in the import.<br>

    <figure><img src="../../../../.gitbook/assets/Screenshot from 2026-09-23 15-41-53.png" alt=""><figcaption></figcaption></figure>
7.  The _Hierarchy Matching_ window opens listing the Geo-Object Types above (parent) the Geo-Object Type for which the shapefile is being imported. The number of Geo-Object Types listed depends on the position in the hierarchy of the Geo-Object Type for which the shapefile is being imported. Fill out the following fields for each parent Geo-Object Type:

    | Field                     | Description                                                                                                                                                   |
    | ------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- |
    | Source file parent column | The attribute from the shapefile being imported that corresponds to the parent Geo-Object Type (unique identifier or name)                                    |
    | Match Strategy            | <p>The strategy on how the selected attribute will be matched:</p><ul><li>Using the code, label, and synonyms</li><li>Using the code only (fastest)</li></ul> |

    _Note:_ The hierarchy matching is optional. This could be completed if you have added the hierarchy information to the shapefile you are importing.

    <figure><img src="https://lh6.googleusercontent.com/N8qd9fvp_OhLXR3EpTF6tRW7o9f-JAP16_E_CUsy_AIO9E9Etd1rmbCYrO1Q_PbwubfpBu_MkO5GXc7WOWVhPhC-v7yQ0PppEuHk4QIR-EvxqQ0iWgNgeqFe3cbbhBOaaG6r1NMUAJx02TpITkjGwT-Dg3Q5uKo9sJBvCw7knkW6zaCuAb-Ewzp-Xw" alt=""><figcaption></figcaption></figure>
8. Click **Submit**.
9.  The import will start processing. Click the **Go to jobs** button to view the progress. This will direct you to the _Scheduled Jobs_ page.&#x20;

    <figure><img src="https://lh4.googleusercontent.com/MFgb0ZyHkIoTrPb5pyh-sud87sA2SyWGSTIWjAnavPCoF9KR9ljzm9zE4W6T-r8BngyxwKL3jVwwmC_xZp9EyOUe8_nXvdZxbLy7Wenq7nmWGUY_ERYsnsrcdwbEeBu0W4wz0EUoqE7nz_VcPKIqMSKJtyiN6nIxEly8B-XpM2j31IYntNW-69ocWw" alt=""><figcaption></figcaption></figure>

