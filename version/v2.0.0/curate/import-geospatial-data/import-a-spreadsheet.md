# Import a Spreadsheet

{% hint style="info" %}
Registry Administrators and Registry Maintainers can import the lists and spatial data of the Geo-Object Types under the curation mandate of their organization
{% endhint %}

To import Geo-Object data into Geoprism Registry, we have to take into account the Geo-Object Types, attributes, and hierarchies that have been defined. The data to be imported needs to be formatted so the fields/columns can be mapped onto the attributes of the relevant Geo-Object Type, and where available, hierarchy information can be matched with the correct hierarchy.

## Importing a spreadsheet&#x20;

To be able to smoothly import a list to Geoprism Registry, the following basic requirements must be followed:

* The spreadsheet must be in XLSX format
* The spreadsheet must contain the values for all the attributes that have been defined in the data dictionary as well as the parents for the hierarchies the Geo-Object Type is a part of
* A header must exist on the first row that contains the unique label for each attribute
* Each column must be set to the appropriate data type
* The data should be in the first worksheet of the XLSX file; all other worksheets will be ignored by the system
* There should be no formulas in the spreadsheet as these are not supported
* Geographic coordinates included in the spreadsheet must be unprojected ([World Geodetic System 1984; EPSG:4326](https://epsg.io/4326)) and stored in separated columns (latitude and longitude)

{% hint style="warning" %}
If the spreadsheet has multiple tabs only the first tab will be used for the import
{% endhint %}

Importing a spreadsheet happens as follows:

1.  Navigate to the _Import_ _Geospatial Data page in the sidebar._<br>

    <figure><img src="../../../../.gitbook/assets/image (110).png" alt=""><figcaption></figcaption></figure>
2.  Ensure the _Import Spreadsheet_ tab is selected.

    <figure><img src="../../../../.gitbook/assets/image (7) (1) (2).png" alt=""><figcaption></figcaption></figure>
3.  Fill out the following fields for the list you would like to import:

    | Field             | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | Required |
    | ----------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------- |
    | Hierarchy         | The hierarchy the Geo-Object Type for which you are importing a list belongs to. The dropdown list of hierarchies will depend on the hierarchies created for the organization you are a part of. If the Geo-Object type is part of several hierarchies then the data elements in the XLSX file containing this information will have to be imported separately for each hierarchy                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  | Required |
    | Geo-Object Type   | The Geo-Object Type for which you are importing content into Geoprism Registry. The dropdown will contain the list of Geo-Object Types over which the user has the curation mandate and which are part of the hierarchy that has been selected                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | Required |
    | Import Strategy   | <p>The import strategy for the list being imported:</p><ul><li><em>New and update:</em> This will import the Geo-Objects and associated attributes in the spreadsheetthat are not yet in Geoprism Registry as well as overwrite the attributes of the Geo-Objects from the list that are already in Geoprism Registry.</li><li><em>New only:</em> This will import only the Geo-Objects from the spreadsheet that are not yet in Geoprism Registry. If the file contains Geo-Objects that were already in Geoprism Registry (same unique identifier and/or label depending on the selected matching method) then the import will fail to avoid creating duplicates.</li><li><em>Update only:</em> This will overwrite the attributes of the Geo-Objects from the spreadsheet that are already in Geoprism Registry. If the imported file contains Geo-Objects that are not already in Geoprism Registry then these will not be imported.</li></ul> | Required |
    | Start Date        | The start of the date of validity of the Geo-Objects in the spreadsheet. All the Geo-Objects in the spreadsheet, whether new or for update, should have the same start date of validity.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | Required |
    | End Date          | The end of the date of validity of the Geo-Objects in the list. All the Geo-Objects in the spreadsheet, whether new or for update, should have the same end date of validity. If the Geo-Objects in the spreadsheet are still valid on the date it is being imported in Geoprism Registry, click the **Set as most current** button.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               | Required |
    | Import blank cell | Selecting this option ensures that if there are empty cells in the list being imported, they are imported as empty attribute values (overwrite). This option gives more control to ensure that updates will either only update cells with values or to overwrite existing values with null values.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |          |

    <figure><img src="https://lh6.googleusercontent.com/q_Kt90IuIgvWshDkgY5dbR1l_tcmlloKsfumtiAxKKFWn5HzzLeOn90f91SqqdpYJ7PtRgZswMNcJhMwtV0akMaOOrioiJ0Avs_251HMUO-ikiz4TpJnajBzU5zNKiV3bDR7JxN0pX1HKawyPo8yuEWK1v5hNpENZOo9tAE4fb6wzuPLxKI4S3w1JA" alt=""><figcaption></figcaption></figure>
4. Click the **Choose file** button and select the shapfile you'd like to download.
5. Click the **Submit** button in the _Spreadsheet import_ window.
6.  The _Attribute Matching_ window opens containing the attributes for the Geo-Object Type. The number of attributes that appears depends on the number of attributes created for the Geo-Object Type for which the spreadsheet is being imported. In the dropdown option for each field, choose the attribute from the list being imported that matches the created attribute of the Geo-Object Type. Click the **Next** button.\
    \
    _&#x4E;ote:_ When the spreadsheet is formatted correctly and completely as mentioned at the start of this section, you should be able to match all of its attributes to the Geo-Object Type for which it is being imported. Otherwise, some of the attributes will be left blank.

    <figure><img src="../../../../.gitbook/assets/image (11) (3).png" alt=""><figcaption></figcaption></figure>
7. The Alternative ID Mapping window opens providing an opportunity to add a mapping to additional ID columns from the shapefile so that can be included in the import.&#x20;
   1. Click _Add ID Mapping._
   2. Select a source authority and an attribute from the source data to be included.
   3.  Click _Next._<br>

       <figure><img src="../../../../.gitbook/assets/Screenshot from 2026-09-23 15-41-53.png" alt=""><figcaption></figcaption></figure>
8.  The _Hierarchy Matching_ window opens listing the Geo-Object Types considered as parents in to the Geo-Object Type for which the spreadsheet is being imported. The number of parent Geo-Object Types that will be listed depends on the position of the imported Geo-Object Type data in the hierarchy. Fill out the following fields for each parent Geo-Object Type:

    | Field                     | Description                                                                                                                                                     | Required |
    | ------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------- |
    | Source file parent column | The attribute from the spreadsheet being imported that corresponds to the parent Geo-Object Type (unique identifier or name)                                    |          |
    | Match Strategy            | <p>The strategy by which the selected attribute will be matched:</p><ul><li>Using the code, label, and synonyms</li><li>Using the code only (fastest)</li></ul> |          |

    _Note:_ Hierarchy matching is optional.

    <figure><img src="https://lh6.googleusercontent.com/yz7Xwzre_HPMwY0HHOl1QyaEJU6-WfxBLaETyPJB9y4Aj93EgfpFWPmKAMItWC70ygZpx-3v1qrAOnSB6wss12E9Em4kBGM-cfvIboC7Q7Jxn7rTmZxSFXlnJLvyjKDAh3hB1PrVrkv-e4_sWVspvbJLPA6QZ83hl35te5Gw2PYEC8nI7zcjCLEBJg" alt=""><figcaption></figcaption></figure>
9. Click **Submit**.
10. The import will start processing. Click the **Go to jobs** button to view the progress. This will direct you to the _Scheduled Jobs_ page.&#x20;

    <figure><img src="../../../../.gitbook/assets/image (22).png" alt=""><figcaption></figcaption></figure>

