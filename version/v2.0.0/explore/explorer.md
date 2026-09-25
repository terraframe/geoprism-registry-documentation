# Explorer

The **Explorer** shows registry data on a map. Use it to view Geo-Objects and their history, edit them, add new ones, and explore how they're related to other data.

{% hint style="info" %}
The System Administrator, Registry Administrators, Registry Maintainers and Registry Contributors can use the Explorer. Registry Contributors' edits are submitted as change requests.
{% endhint %}

## Opening the Explorer

* Navigate to the **Explorer** page from the sidebar.
* From a list on the [Lists and Spatial Data](lists-and-spatial-data/README.md) page:
  * **View on map** opens the Explorer with the list's spatial data as a layer.
  * The eye icon on a row opens the Explorer with that Geo-Object selected.
  * **Spatial Data**, under a version on the set's page, opens that version's spatial data.
  * **Add Geo-Object** opens the Explorer with a new Geo-Object ready to fill in.
* From a curation report, **Resolve** opens the Explorer at the Geo-Object with the problem.

The page has a full-screen map, with a search bar at the top left and buttons to open the **Layer Panel**, the **Attribute Panel** and the **Graph Visualizer**.

## Adding layers to the map

The map shows the spatial data of list versions as layers.

1.  Click the layers icon (**Open Layer Panel**), then the expand icon (**Expand and Search For Layers**).
2.  Enter a **Start Date** and **End Date**, and click **Find Layers**.
3.  The available lists are grouped by organization and Geo-Object Type. Click the plus icon (**Add To Legend**) next to a working version or a published version to add it to the map.

Each layer in the legend has:

* A checkbox to show or hide it. You can drag layers to change their order.
* A link to the version. Click it to open the list in a panel at the bottom of the map, where you can filter it, export it, or click a row's eye icon to select that Geo-Object.
* **Zoom To Feature**, **Pin** or **Unpin**, and **Remove Layer**.
* **Add New Geo-Object**, on working-version layers only (see below).

Layer colours are assigned automatically. The Explorer also adds layers for search results, the selected Geo-Object and related objects.

## Searching for a Geo-Object

1.  In the search bar, optionally enter a date, then type a name or code in **Search for Geo-Objects to edit** and click the search button.
2.  The results are listed, and shown on the map as a **Search Results** layer. Click a result to select it.

## Viewing a Geo-Object

Click a Geo-Object on the map, in the search results or in a list to open it in the **Attribute Panel**.

    <figure><img src="../../../.gitbook/assets/image (3) (1).png" alt=""><figcaption></figcaption></figure>

* **History** shows the periods in which the Geo-Object changed. Use the arrows to move between periods, or choose to view all periods.
* The **Attributes**, **Hierarchies** and **Geometry** tabs show its values for each period, including its **Geo-Object Name** and **Geo-Object Unique ID**.
* The gear tab shows whether the Geo-Object **Exists** and its **Validity** over time.

    <figure><img src="../../../.gitbook/assets/image (29).png" alt=""><figcaption></figcaption></figure>

Business objects open in a similar panel.

## Editing a Geo-Object

1.  Select the Geo-Object and click **Edit** in the Attribute Panel.

    <figure><img src="../../../.gitbook/assets/image (24) (2).png" alt=""><figcaption></figcaption></figure>
2.  Click the tab with the information you want to change: **Attributes**, **Hierarchies**, **Geometry** or the gear tab.

    <figure><img src="../../../.gitbook/assets/image (33).png" alt=""><figcaption></figcaption></figure>
3.  Make your changes. Each value has a start and end date, and you can click **New instance** to add a value for a new period. Changed tabs are marked with an orange dot, changed values turn orange, and each change is labelled:
    * **Value Change:** only the value changed.

        <figure><img src="../../../.gitbook/assets/image (15) (2).png" alt=""><figcaption></figcaption></figure>
    * **Time Change:** only the dates changed.

        <figure><img src="../../../.gitbook/assets/image (2) (1) (2).png" alt=""><figcaption></figcaption></figure>
    * **Update:** both the value and the dates changed.

        <figure><img src="../../../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>
4.  To undo the changes in a tab, click the revert arrow.

    <figure><img src="../../../.gitbook/assets/image (26) (2).png" alt=""><figcaption></figcaption></figure>
5.  On the **Geometry** tab, if geometry editing is enabled for the Geo-Object Type, click **Edit Geometry** to draw or change the shape on the map, and **Stop editing** when you're done. For points, you can type the **Latitude** and **Longitude**. **Show original** displays the geometry before your changes.
6.  Click **Submit**. If you're a Registry Contributor, enter a **Reason** and click **Submit A Change Request** instead.

    <figure><img src="../../../.gitbook/assets/image (32).png" alt=""><figcaption></figcaption></figure>
7.  A message confirms the edit was submitted. For a change request, click **View change request** to see it, or **Ok**.

If you leave while editing, a message warns that your changes will be lost.

## Adding a Geo-Object

1.  Start a new Geo-Object in one of these ways:
    * On a working version of a list, click **Add Geo-Object**.
    * In the Layer Panel, click **Add New Geo-Object** next to a working-version layer. ![](<../../../.gitbook/assets/image (4) (1) (3).png>)

    For a group, choose which Geo-Object Type to add in **Select a Geo-Object Type**.
2.  On the gear tab, set when the Geo-Object **Exists**: select **Yes** and enter the start and end dates. The other tabs are available once this is filled in. Check that **Validity** is set to **Valid**.

    <figure><img src="../../../.gitbook/assets/image (12) (1).png" alt=""><figcaption></figcaption></figure>
3.  Fill in the **Attributes**, the parents on the **Hierarchies** tab and, if geometry editing is enabled, the **Geometry**.
4.  Click **Submit**, or **Submit A Change Request** with a **Reason** if you're a Registry Contributor.

    <figure><img src="../../../.gitbook/assets/image (19) (1).png" alt=""><figcaption></figcaption></figure>
5.  A message confirms the Geo-Object was submitted. Click **Ok**.

    <figure><img src="../../../.gitbook/assets/image (14) (3).png" alt=""><figcaption></figcaption></figure>

## Exploring relationships with the Graph Visualizer

The Graph Visualizer shows how the selected Geo-Object is related to other Geo-Objects and business objects.

1.  Select a Geo-Object and click **Open Graph Visualizer**.
2.  Choose a relationship type from the list, which shows how many related objects each type has. Optionally choose a period, or select **Restrict to map bounds** to show only objects in the current map view.
3.  The graph shows Geo-Objects as hexagons and business objects as rectangles. The related objects are also drawn on the map as **Relationship** layers.
4.  Click an object in the graph to select it. Click a relationship (the line between two objects) to see its attributes.

### Deleting a relationship

{% hint style="danger" %}
Deleting a relationship can't be undone.
{% endhint %}

1.  Click the relationship in the graph.
2.  Click **Delete**, then **Yes, delete** to confirm.
