# Import Business Data

The Import Business Data page loads data from a spreadsheet into Geoprism Registry. It imports two kinds of objects:

* **Business Objects:** tabular data that isn't geospatial. Each row becomes an object of a [Business Type](../configure/business-types/README.md).
* **Concept Objects:** the Concepts of a [Concept Class](../configure/concepts/concept-classes.md), such as the terms in a classification or taxonomy. Each row becomes a Concept.

{% hint style="info" %}
Concept Objects imports the Concepts themselves, not the relationships between them. After you import your Concepts, load their relationships on the [Import Edge Data](import-edge-data.md) page. See [Concepts](../configure/concepts/README.md) for the full setup order.
{% endhint %}

## Preparing the spreadsheet

* The file must be an XLS or XLSX spreadsheet.
* Only the first worksheet is imported. All other worksheets are ignored.
* The first row must be a header with a name for each column.
* The spreadsheet must have a column with a unique **code** for each row. Geoprism Registry uses the code to tell whether a row is a new object or an update to an existing one.
* Include a column for each attribute of the Business Type or Concept Class you want to import, such as the label.
* Set each column to the data type of the attribute it will be matched to (text, number, date or boolean). Only columns of the matching type are offered when you match attributes.

## Importing the data

1. Navigate to the **Import Business Data** page from the sidebar.
2. Fill out the form:

   | Field              | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                      | Required |
   | ------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------- |
   | Object Class       | <p>The kind of object you're importing:</p><ul><li><strong>Business Object:</strong> data for a Business Type.</li><li><strong>Concept Object:</strong> Concepts for a Concept Class.</li></ul>                                                                                                                                                                                                                                                                | Required |
   | Type               | The Business Type or Concept Class to import into. The list changes depending on the Object Class you choose.                                                                                                                                                                                                                                                                                                                                                    | Required |
   | Import Strategy    | <p>How rows are matched with objects already in Geoprism Registry, using the code column:</p><ul><li><strong>New and update:</strong> Creates objects whose code isn't in the registry yet and updates the ones that are.</li><li><strong>New only:</strong> Creates new objects. A row whose code already exists is recorded as an error.</li><li><strong>Update only:</strong> Updates existing objects. A row whose code isn't in the registry is recorded as an error.</li></ul> | Required |
   | Start Date         | The start of the period of validity for the imported values.                                                                                                                                                                                                                                                                                                                                                                                                     |          |
   | End Date           | The end of the period of validity for the imported values. If the values are still valid today, click **Set as most current**. The end date shows as "Present".                                                                                                                                                                                                                                                                                                 | Required |
   | Data Source        | The [Data Source](../configure/data-sources/add-a-data-source.md) the data comes from.                                                                                                                                                                                                                                                                                                                                                                           |          |
   | Description        | An optional description of this import.                                                                                                                                                                                                                                                                                                                                                                                                                          |          |
   | Import blank cells | When selected (the default), empty cells are imported as empty values and overwrite existing values. Clear it to leave existing values unchanged where a cell is empty.                                                                                                                                                                                                                                                                                          |          |
   | Spreadsheet        | The XLS or XLSX file to import.                                                                                                                                                                                                                                                                                                                                                                                                                                  | Required |

3. Click **Submit**.
4. The **Attribute Matching** window opens with one row for each attribute of the selected type. Attributes that can be translated have one row per installed locale. For each attribute, choose the spreadsheet column that holds its values, then click **Ok**.
5. The import starts processing. Click **Go to jobs** to follow its progress on the [Scheduled Jobs](scheduled-jobs/view-scheduled-jobs.md) page, or **Close** to stay on the page.

Rows that can't be imported, such as a row with no code, are recorded as errors on the import job. The other rows are still imported. See [Troubleshooting scheduled jobs](scheduled-jobs/troubleshooting-scheduled-jobs.md) for how to review and fix them.
