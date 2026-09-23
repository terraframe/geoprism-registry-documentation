# Import a Shapefile

{% hint style="info" %}
Registry Administrators and Registry Maintainers can import the lists and spatial data of the Geo-Object Types under the curation mandate of their organization
{% endhint %}

Spatial data is imported into GeoPrism Registry through shapefiles.

To be able to smoothly import shapefiles into GeoPrism Registry, these basic requirements must be followed:

* The spatial data must be in [shapefile](https://support.esri.com/en/white-paper/279) format.
* As a shapefile consists of multiple files that collectively make up a shapefile, these files must be compressed into a zipped (.zip) file before importing.
* The shapefile must include data only for a single Geo-Object Type.
* The shapefile must be unprojected ([World Geodetic System 1984; EPSG:4326](https://epsg.io/4326)). Otherwise, GeoPrism Registry will give an error message and the import will not take place.

Shapefiles are imported as follows:

1.  Go to the _Import_ module either by clicking the module icon on the homepage or by clicking the hamburger menu (![](https://lh3.googleusercontent.com/4ieAODNcwrlKZ6iUiZnYlbLGZmQJiEse_Z8mls7B1vwiKHOfldO3TWH3smxfa1IJQb_BhxM7c6iTe--Wm0sPvlovt4jp-DaoMkTqq5MNslg-imIrXqyoa3A3Fnq-Ct_7AAaQzW-xMCIbev1kGSUU8xN5v8iFIayG4z8c4H78mU80Ms6J_4PBB1ghQw)) in the upper right corner and selecting **Import**.\\

    <figure><img src="../../../../.gitbook/assets/image (9) (2).png" alt=""><figcaption></figcaption></figure>
2.  Click on the **Import Shapefile** tab.

    <figure><img src="../../../../.gitbook/assets/image (8) (2).png" alt=""><figcaption></figcaption></figure>
3.  If an external system has been registered in GeoPrism Registry (see [section 4](../../../../versions/current/external-system-integration.md)) a window will open providing the option for the import to take place from an external system or from your computer. Choose the option that applies.\\

    <figure><img src="https://lh5.googleusercontent.com/gzrGuLtTRrA5Mjzgxqb-3bCZ8EupCmn-DBqw8im3wPxPxLSvRTrUsm6HUrlbdd2UejfDD1ZUrEgOkNy0a4ZAPjEAwqbG6-3zpMSHhAOhfIrjCMI5jNdgCsVuihaLS4AT5ULbSG7-u5LECgtna3HlKBua4dbc2PacOm8ZF82kxjo7jtMMIs3Y0LFSlQ" alt=""><figcaption></figcaption></figure>
4.  Fill out the following fields for the shapefile you would like to import:\\

    | Field              | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              | Required |
    | ------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | -------- |
    | Hierarchy          | The hierarchy the Geo-Object Type for which you are importing a shapefile belongs to. The dropdown list of hierarchies will depend on the hierarchies created for the organization you are a part of.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | Required |
    | Geo-Object Type    | The Geo-Object Type of the shapefile you would like to import. The dropdown list of Geo-Object Types will depend on the hierarchy selected in the _Hierarchy_ field.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | Required |
    | Import Strategy    | <p>The import strategy for the shapefile being imported:</p><ul><li><em>New and update:</em> This will import the Geo-Objects in the shapefile that are not yet in GeoPrism Registry as well as overwrite the attributes of Geo-Objects from the shapefile that are already in GeoPrism Registry.</li><li><em>New only:</em> This will import only the Geo-Objects from the shapefile that are not yet in GeoPrism Registry. If the imported file contains Geo-Objects that are already in GeoPrism Registry (same unique identifier and/or label depending on what is selected during matching) then the import will fail to avoid creating duplicates.</li><li><em>Update only:</em> This will overwrite the attributes of the Geo-Objects from the list that are already in GeoPrism Registry. If the imported file contains Geo-Objects that are not yet in GeoPrism Registry, these will not be imported.</li></ul> | Required |
    | Start Date         | The start of the date of validity of the Geo-Objects in the shapefile. All the Geo-Objects in the shapefile being imported, whether new or for update, should have the same start date of validity.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | Required |
    | End Date           | The end of the date of validity of the Geo-Objects in the shapefile. All the Geo-Objects in the shapefile being imported, whether new or for update, should have the same end date of validity. If the shapefile is still valid on the date it is being imported in GeoPrism Registry, click the **Set as most current** button.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         | Required |
    | Import blank cells | Selecting this option ensures that if there are empty cells in the list being imported, they are imported as empty attribute values (overwrite). This option gives more control to ensure that updates will either only update cells with values or to overwrite existing values with _null_ values.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |          |

    <figure><img src="https://lh3.googleusercontent.com/yGMQl8P3jzfSorz_rFV_EOfJ6MJDzLG629sT6eAUgrKr-TlkSBud_ygqeIqIMUY2TybEAkFSuNelEnHjqcNT4x7LeB7Lbq3FSssRnYwBXUXJ_wMyxZX6rE8yjqBLAqfmEoan71rNmwjYSvJ8nAhmKNyMhnE7PEZkGFCDEnUXRRYP67FmTu7LfpfTRw" alt=""><figcaption></figcaption></figure>
5.  Click the **Choose file** button and in the window that opens, browse to the location of the compressed shapefile (.zip file) you would like to import. Select the file and click **Open**.\\

    <figure><img src="../../../../.gitbook/assets/image (24) (1).png" alt=""><figcaption></figcaption></figure>
6. Click the **Submit** button in the _Shapefile import_ window.
7.  The _Attribute Matching_ window opens containing the attributes for the Geo-Object Type. The number of attributes that appears depends on the number of attributes created for the Geo-Object Type for which the shapefile is being imported. In the dropdown option for each field, choose the attribute from the shapefile being imported that matches the created attribute of the Geo-Object Type. Click the **Next** button.\
    \
    _&#x4E;ote:_ When the shapefile is formatted correctly and completely, you should be able to match all of its attributes to the Geo-Object Type for which it is being imported. Otherwise, some of the attributes will be left blank.

    <figure><img src="https://lh4.googleusercontent.com/0LMTC-BtSDHf5d2ewcO4vJQ1hqw2bQ0uQbkWQkuh9ZXq-EBl3yHW2aaVB0n0X2e0esf030QKmzpsBKkJbyG0Ces56Utu-cgAUF4YveFClWozozlYRcb7LEL4Ez-3MnIaSu_Nx9FCDp5EkLy7kJTEnUoJBxTdYICBeiNt4yIC0RpwkJxmzpKiyv29Lw" alt=""><figcaption></figcaption></figure>
8.  The _Hierarchy Matching_ window opens listing the Geo-Object Types above (parent) the Geo-Object Type for which the shapefile is being imported. The number of Geo-Object Types listed depends on the position in the hierarchy of the Geo-Object Type for which the shapefile is being imported. Fill out the following fields for each parent Geo-Object Type:\\

    | Field                     | Description                                                                                                                                                   |
    | ------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- |
    | Source file parent column | The attribute from the shapefile being imported that corresponds to the parent Geo-Object Type (unique identifier or name)                                    |
    | Match Strategy            | <p>The strategy on how the selected attribute will be matched:</p><ul><li>Using the code, label, and synonyms</li><li>Using the code only (fastest)</li></ul> |

    _Note:_ The hierarchy matching is optional. This could be completed if you have added the hierarchy information to the shapefile you are importing.

    <figure><img src="https://lh6.googleusercontent.com/N8qd9fvp_OhLXR3EpTF6tRW7o9f-JAP16_E_CUsy_AIO9E9Etd1rmbCYrO1Q_PbwubfpBu_MkO5GXc7WOWVhPhC-v7yQ0PppEuHk4QIR-EvxqQ0iWgNgeqFe3cbbhBOaaG6r1NMUAJx02TpITkjGwT-Dg3Q5uKo9sJBvCw7knkW6zaCuAb-Ewzp-Xw" alt=""><figcaption></figcaption></figure>
9. Click **Submit**.
10. The import will start processing. Click the **Go to jobs** button to view the progress.\\

    <figure><img src="https://lh4.googleusercontent.com/MFgb0ZyHkIoTrPb5pyh-sud87sA2SyWGSTIWjAnavPCoF9KR9ljzm9zE4W6T-r8BngyxwKL3jVwwmC_xZp9EyOUe8_nXvdZxbLy7Wenq7nmWGUY_ERYsnsrcdwbEeBu0W4wz0EUoqE7nz_VcPKIqMSKJtyiN6nIxEly8B-XpM2j31IYntNW-69ocWw" alt=""><figcaption></figcaption></figure>
11. This will direct you to the _Scheduled Jobs_ module. If there is no problem with the imported shapefile, the page will look as follows. You will see the imported shapefile listed as one of the completed jobs when you click on the **View completed jobs** button.\\

    <figure><img src="../../../../.gitbook/assets/image (18) (1).png" alt=""><figcaption></figcaption></figure>
12. If there is any problem with the shapefile being imported, you will see this in the _In progress_ section with the part of the process with the problem highlighted in red. Click on the **Resolve Problems** button to see the details of the problem.\\

    <figure><img src="../../../../.gitbook/assets/image (14) (2).png" alt=""><figcaption></figcaption></figure>
13. The _Job Details_ page will provide the problem type, message, and row number details of the issue and give you options on how to solve each problem when you click the **Resolve** button.\
    \
    _&#x4E;ote:_ Depending on the problem type, GeoPrism Registry may ask you to fix the problem in the shapefile itself and then re-import it.

    <figure><img src="https://lh4.googleusercontent.com/IhFFTih4s3WozWbMm45gssTdXBCZPzfiWERSX2eUAkDqOqKZDYNKgq696QBFKTEVRGzDB7lAfqKY9dGZFnu5GojoWgdr3J1j3sjiER3NJupj-i4Txa3k1jxw9wr0BJTO0HcIAo5tdDJnlgvCQpZlsNuumVjiXl68soFJFShsIy9cnoS4YT0BI-j-Xw" alt=""><figcaption></figcaption></figure>
14. Depending on the problem type, there may also be cases when you can ignore the errors and proceed with the import. When this is the case, click the **Ignore All Errors** button.\\

    <figure><img src="../../../../.gitbook/assets/image (26) (1).png" alt=""><figcaption></figcaption></figure>
15. A warning message will appear asking if you want to mark the import as completed. Click the **Complete import** button. This will complete the import process.\\

    <figure><img src="https://lh4.googleusercontent.com/dUb_qP2jbs_1Jhz2M7sL4o7SMNPXek9zMtd0Xp46sva4UFIpCsTrKtYZbineD3KV-a0sVu834moh72446WVaQ0JkGzugodEEHi86Mkar-GLpdgZ6t_GmLIclh1uBlGl6d-FGYyKI6-zGHAP8hpQ7KGXEjqGCiI1pDM-Zw4ULZizvbFCxF54ftmAmcQ" alt=""><figcaption></figcaption></figure>
16. You will see the imported shapefile when you click on the **View completed jobs** button.\\

    <figure><img src="../../../../.gitbook/assets/image (20).png" alt=""><figcaption></figcaption></figure>
