# 5.1.2. Geographic object types and groups

The types of geographic objects (a.k.a. **Geo-Object Types**) handled by GeoPrism Registry can be categorized based on how they would be represented on a map:

* Fixed geographic objects that can be simplified by a point, for example: household, health facility, human settlement
* Fixed geographic objects that should be represented by polygons due to their much larger extent, for examples: administrative units, health districts, or by a line due to their shape, for example: road, river
* Mobile geographic objects, for example: individuals, patients, vehicles; the geography of these objects would either be obtained by considering them attached to a fixed geographic object or by simplifying them as a point that would be located through their geographic coordinates (latitude and longitude) taken at a given point in time.

In GeoPrism Registry, these can be further aggregated into groups of geographic object types having the same attribute configuration (e.g., health facilities as a Geo-Object Type group could group health posts, health centers, and hospitals).
