# Import Geospatial Data

The Import Geospatial Data page loads Geo-Objects into a Geo-Object Type from a file. You can import:

* **A spreadsheet** (XLS or XLSX) with one row per Geo-Object. Point locations can be included as latitude and longitude columns. See [import-a-spreadsheet.md](import-a-spreadsheet.md "mention").
* **A shapefile** (zipped) with the geometry of each Geo-Object, such as points, lines or polygons. See [import-a-shapefile.md](import-a-shapefile.md "mention").

Both imports follow the same steps:

1. Choose the Geo-Object Type, import strategy and period of validity, and upload the file.
2. Match the columns in your file to the attributes of the Geo-Object Type.
3. Optionally, map columns that hold alternative IDs and link Geo-Objects to their parents in a hierarchy.
4. Fix any parent location or term problems the import finds.
5. Follow the import on the [Scheduled Jobs](../scheduled-jobs/view-scheduled-jobs.md) page.

{% hint style="info" %}
To import data that isn't geospatial, or Concepts, use [Import Business Data](../import-business-data.md). To import relationships between existing objects, use [Import Edge Data](../import-edge-data.md).
{% endhint %}
