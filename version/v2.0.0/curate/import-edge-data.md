# Import Edge Data

The Import Edge Data page loads relationships (edges) between objects that are already in Geoprism Registry. You can import edges for any edge type in the system, including hierarchies, directed acyclic graph types, undirected graph types, Business Edge Types and [Concept Edge Types](../configure/concepts/concept-edge-types.md).

A common use is loading a Concept taxonomy. After you import your Concepts on the [Import Business Data](import-business-data.md) page, you import the "is a" relationships between them here.

{% hint style="info" %}
Edge Data imports only the relationships. The objects at both ends of each edge must already exist, or that row is recorded as an error.
{% endhint %}

## Preparing the file

The file must be a JSON file containing an array of objects. Each object is one edge and needs at least two keys: one that identifies the **source** (parent) object and one that identifies the **target** (child) object. You choose which keys to use when you import, so the key names are up to you.

For example, this file relates Concepts in a taxonomy of structures:

```json
[
  {
    "source": "Structure",
    "sourceType": "BuiltAsset",
    "target": "Building",
    "targetType": "BuiltAsset"
  },
  {
    "source": "Structure",
    "sourceType": "BuiltAsset",
    "target": "Dam",
    "targetType": "BuiltAsset"
  },
  {
    "source": "Building",
    "sourceType": "BuiltAsset",
    "target": "VisitorCenter",
    "targetType": "BuiltAsset"
  }
]
```

Here `source` and `target` hold Concept codes, and `sourceType` and `targetType` hold the code of the Concept Class (`BuiltAsset`). Codes can be any unique string, including URIs such as `https://example.com/taxonomy#Dam`.

* Identify objects by their **code**. For Geo-Objects, you can use an alternative ID instead (see [Field Mapping](#field-mapping) below).
* Include keys for the type code of the source and target, like `sourceType` and `targetType` above. If every source is the same type, and every target is the same type, you can leave them out and choose the type during import instead.

## Importing the data

1. Navigate to the **Import Edge Data** page from the sidebar.
2. Fill out the form:

   | Field           | Description                                                                                                                                                              | Required |
   | --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | -------- |
   | Edge Type       | The edge type to import into. The list includes every edge type in the system.                                                                                           | Required |
   | Import Strategy | <p>How incoming edges are treated:</p><ul><li><strong>New and update:</strong> Creates new edges and updates edges that already exist.</li><li><strong>New only:</strong> Treats every edge as new and skips checking for existing data. Use it only when none of the edges are in the registry yet.</li><li><strong>Update only:</strong> Treats every edge as an update to an existing edge.</li></ul> | Required |
   | Start Date      | The start of the period of validity for the imported edges.                                                                                                              | Required |
   | End Date        | The end of the period of validity for the imported edges. If the edges are still valid today, click **Set as most current**. The end date shows as "Present".           | Required |
   | Data Source     | The [Data Source](../configure/data-sources/add-a-data-source.md) the data comes from.                                                                                   |          |
   | Description     | An optional description of this import.                                                                                                                                  |          |
   | JSON            | The JSON file to import.                                                                                                                                                 | Required |

3. Click **Submit**.
4. The **Field Mapping** window opens. Map the keys in your JSON objects to the source and target of each edge (see [Field Mapping](#field-mapping)), then click **Ok**.
5. The import starts processing. Click **Go to jobs** to follow its progress on the [Scheduled Jobs](scheduled-jobs/view-scheduled-jobs.md) page, or **Close** to stay on the page.

Rows that can't be imported, such as an edge whose source or target doesn't exist, are recorded as errors on the import job. See [Troubleshooting scheduled jobs](scheduled-jobs/troubleshooting-scheduled-jobs.md) for how to review and fix them.

## Field Mapping

The **Field Mapping** window has the same fields for the source (parent) and the target (child) of each edge:

| Field                                                            | Description                                                                                                                                                                                                                                                              |
| ---------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Source Strategy / Target Strategy                                | <p>How the object is identified:</p><ul><li><strong>Code:</strong> the key holds the object's code.</li><li><strong>Alternative Id:</strong> the key holds an alternative ID from a <a href="../configure/source-authorities/README.md">Source Authority</a>. This only works for Geo-Objects. Concepts and Business Objects are always matched by code.</li></ul> |
| Source / Target                                                  | The key in your JSON objects that holds the identifier.                                                                                                                                                                                                                  |
| Source Column Source Authority / Target Column Source Authority  | The Source Authority that issued the alternative IDs. Only shown when the strategy is **Alternative Id**.                                                                                                                                                               |
| Source Type Strategy / Target Type Strategy                      | <p>How the object's type is found:</p><ul><li><strong>Code:</strong> a key in each JSON object holds the type code.</li><li><strong>Fixed Type:</strong> every object on that side of the edge is the same type, which you choose below.</li></ul>                        |
| Source Type / Target Type                                        | With **Code**, the key that holds the type code. With **Fixed Type**, the type itself, such as a Concept Class or Geo-Object Type.                                                                                                                                      |

For the Concept example above, set Source Strategy and Target Strategy to **Code**, and choose `source` as the Source and `target` as the Target. Set both type strategies to **Code**, and choose `sourceType` as the Source Type and `targetType` as the Target Type.
