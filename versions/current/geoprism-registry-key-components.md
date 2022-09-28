# GeoPrism Registry Key Components

### 5.1 Content

GeoPrism Registry is being used to simultaneously host, maintain, update and share **lists** as well as associated **hierarchies** and **spatial data** for the **geographic objects** core to development in general and public health in particular.

The following sections describe in more detail these different elements, as well as those associated with them (geographic features, geographic object types, data elements, classification tables).

Please refer to the CGR guidance \[1] for specific considerations to take into account when developing such content before uploading it in GeoPrism Registry (quality, unique identifier, master vs non-master list, etc.).

### 5.1.1 Geographic features and geographic objects&#x20;

Geographic features are features of the Earth, natural (e.g, rivers) or artificial (e.g., buildings), physical (e.g., roads) or abstract (e.g., administrative division). Each sector has its own set of geographic features that are core to the implementation of its programs and activities. Those core to the health sector for example include but are not limited to: health facilities, vaccination points, settlements, ambulances, patients, roads and administrative divisions.

GeoPrism Registry does nevertheless only handle geographic features for which it makes sense to establish and maintain a master list. These include fixed features such as health facilities, schools, bridges, or villages; artificially-created features such as administrative units, foci or health areas or mobile features such as vehicles or peoples. A master list for other geographic features would either generally not be necessary (e.g., roads, rivers) or not applicable (e.g., continuous features like topography or population distribution) \[2]. A geographic object, or geo-object, is itself the computer representation of a geographic feature. It can be represented as a point, line, or polygon on a map (more details on this in the next section).&#x20;

### 5.1.2 Geographic object types and groups&#x20;

The types geographic objects (or geo-object types) handled by GeoPrism Registry can be categorized based on how they would be represented on a map \[2]:&#x20;

* Fixed geographic objects that can be simplified by a point (examples: household, health facility, human settlement).&#x20;
* Fixed geographic objects that should be represented by polygons due to their much larger extent (examples: administrative units, health districts...) or by a line due to their shape (example: road, river...).&#x20;
* Mobile geographic objects (examples: individuals, patients, vehicles...): the geography of these objects would either be obtained by considering them attached to a fixed geographic object or by simplifying them as a point that would be located through their geographic coordinates (latitude and longitude) taken at a given point in time.&#x20;

In GeoPrism Registry, these can be further aggregated into groups of geographic object types having the same attribute configuration (e.g., health facilities as a geo-object type group could group health posts, health centers, and hospitals).

### 5.1.3 Data elements and classification tables

The GeoPrism Registry focuses on all the information that allows to contextualize any piece of information in both space and time. It therefore only handles data elements meant to uniquely identify , classify, locate, and, when applicable, contact each geographic object it contains (the set of data elements referred to as the signature domain). Such a list will be specific to each type of geographic object hosted in the platform.

Other types of data elements, including programmatic ones (e.g., statistics), are not meant to be managed in the GeoPrism Registry but in program-, or even sector-, specific information systems. Some of the reasons behind this are the sensitivities often linked to programmatic data, the difference in data flow between this type of data and the geographic objects they are attached to as well as the difference in the management of the time dimension (e.g., the temporal validity of a statistic might be different from the temporal validity of the geographic object it is attached to). In addition, managing these data elements in these other systems allows the programs to benefit from functionalities that are not available within a registry, including, but not limited to, data collection, statistical analysis, or visualization (graphs, thematic maps).

The identification of the data elements to be associated with each geographic object and stored in the GeoPrism Registry should take place as part of a process involving all the concerned stakeholders \[1]. The result is a data dictionary containing at least the following information for each of the selected data elements (an example for a health facility master list is presented in Annex 2 of the CGR guidance):

* The data element code as implemented in the GeoPrism Registry&#x20;
* A short description of the data element&#x20;
* The data element type&#x20;
* The size of the data element (number of storage units)&#x20;
* Whether the data element is considered as mandatory when adding a new record in the master list Examples, notes, and, when applicable, the source (reference) of each data element can be added to the above information if it can help those in charge of managing the GeoPrism Registry content and its users to have a clear understanding of each of these data elements. A classification table also needs to be defined for each of the data elements where the values are limited to a few options to ensure consistency across records (example: type, ownership, etc.). Such tables should at least contain the following for each option: a unique code, a label (English and local language) and/or acronym, a description (English and local language), and, when applicable, the source of the definition. Table 1 provides an example of a classification table for health facility types in Cambodia following this structure.

Table 1 – Example of classification table (health facility types in Cambodia)

### 5.1.4 Hierarchies

Knowing how geographic objects relate to each other over time as part of different hierarchies is important not only to be able to aggregate information to support decision making when applicable but also to ensure relational consistency between geographic objects.

One of the functions of the GeoPrism Registry is to capture and use not only geographic relationships that exist between geographic objects (is within, lives in) but also other types of relationships such as administrative (is reporting to), health-related (covers, providing service to, refers to), and associative (is part of).

These different relationships can be represented in distinct hierarchies like those included in Figure 1.

Figure 1 – Example of hierarchies

### 5.1.5 Lists

A list is a tabular representation of the data elements associated with all the active, and past active, geographic objects (records) of a given type at a given point in time.

Lists represent the most familiar way for users to look at the information associated with any type of geographic object. When they are authoritative and curated by the mandated governmental entity, these lists, referred as master lists in this case, also serve as a ground reference to assess the completeness, uniqueness, timeliness, validity, and consistency of the geospatial data also hosted in a CGR \[5], as well as a denominator for the implementation of any public health program.

Table 2 – Extract of list corresponding to the data dictionary reported in Annex 2

### 5.1.6 Spatial data

Also referred to as spatial data, geospatial data corresponds to information about the locations and shapes of geographic features and the relationships between them, usually stored as coordinates and topology (e.g., geographic location of health facilities, boundaries of administrative units…).

As the GeoPrism Registry only handles types of geographic objects for which it is important to host, manage, regularly update, and share a list, this corresponds to geographic objects that are stored in vector format GIS layers. Raster format GIS layers cannot be uploaded to the platform.

The GeoPrism Registry is able to handle the three modes of representation of geographic features in the vector format: points, lines, or polygons (Figure 2).

Figure 2 – Modes of representation in the vector format (points (a), lines (b), and polygons (c))

a)b)c)

### 5.1.7 Data quality

The content hosted in the GeoPrism Registry is meant to serve as the source of truth (ground reference) for any information system to properly contextualize, visualize, and analyze business data in both space and time. As such, this content is meant to present the highest level of quality possible across the 6 dimensions of data quality (uniqueness, completeness, timeliness, accuracy, validity, and consistency) \[3].

While the GeoPrism Registry is meant to help improve and maintain the quality of this content across these dimensions, the higher the quality of this content at the time of uploading it in the platform, the lesser the work afterwards and the faster positive impacts can be seen.

The quality of the content before its upload in the platform can be ensured through the implementation of good data management practices throughout the overall geospatial data management cycle in Figure 5 (extracted from \[4]). The implementation of this cycle, and associated good practices, should ideally take place as part of the activities of the NSDI.

If an NSDI is not in place, the reference material generated by the Health GeoLab Collaborative can be used as a reference to ensure the quality of the data and information to be uploaded in the platform. Figure 5 – Geospatial data management cycle

### 5.2 Content related capacities of GeoPrism Registry

The following sections describe in more detail the capacities of the GeoPrism Registry in managing the content being hosted in the platform ([Section 5.1](geoprism-registry-key-components.md#5.1-content)).

### 5.2.1 Changes over time

Geography evolves over time (creation of a new district, closing of a health facility, change of phone number for a community health worker).

This is why a core function of the GeoPrism Registry is to be able to capture the changes that are occurring over time for the geographic objects it hosts as well as conserve the information as it was before the change and, when applicable, the information necessary to rebuild the change (e.g., the unique identifier and name of the district from which a new district has been carved). This information is critical to perform trend analysis, especially in countries where the administrative structure changes frequently (e.g. to reconstruct disease prevalence trends across districts that have changed over time).

This capability of the GeoPrism Registry allows the retrieval of the lists and associated geospatial data for any geographic object at any point in time over the entire period for which data has been uploaded in the platform.

The three main types of changes that can be captured in the GeoPrism Registry for any given geographic object are presented in Table 3.

#### Table 3 – Type of changes that can be captured in the GeoPrism Registry

| Type               | Description                                                                             | Example                                                                                                            |
| ------------------ | --------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------ |
| Start of existence | The start of existence of the geographic object                                         | Opening a new health facility, creation of a new district                                                          |
| Value change       | A change in value for a given data element including parents in a hierarchy or geometry | Change of health facility name, phone number, or status or the geographic location/extent of the geographic object |
| End of existence   | The end of existence of the geographic object                                           | Closure of a health facility, end of existence of a province being merged with another one                         |

Figure 4 provides an illustration of these main types of changes for a health facility that opened on April 19, 1984, and closed definitively on April 1, 2021. Over that period, the health facility’s name, head, and phone number each changed once at different points in time.

#### Figure 4 – Example of changes occurring over time for some data elements associated with a health facility

![](https://lh6.googleusercontent.com/cB5LZJXz4YBUUCe3ziMytMwrW7U1R6Md0BRjdZk4-cPZZ7AAQVRW27rMdHx3sYvPxgQLi-sstaUvLztC3ohUres8Swa-b9BaPa6-J\_SIQH5pEXK4ILdTpDl9p59zv-dhrv2\_8JXrnrs1G7tSCgQbME43LkXr5rXBMhUsuwvUqlTvkYIEVBcqG4gB)

For this kind of change, the GeoPrism Registry has the capacity to:&#x20;

* Set the period of existence of the geographic object (1984-04-19 to 2021-04-01)&#x20;
* Capture and retain the value for each instance of the data elements that have changed through time together with the period over which each value has been valid (e.g., Patrick Dupont over the 1984-04-19 to 2008-06-06 period and then Henri Dunant over the 2008-06-06 to 2021-04-01 period as the health facility head).

Capturing the above information is sufficient to understand changes occurring to any independently created geographic objects, i.e., geographic objects that are not being created out of already existing ones (e.g., infrastructures such as health facilities or schools).

All of this happens as part of the management of the lists in the GeoPrism Registry. Please refer to Section 6.5.1 for more details on how this information is being captured and managed in the GeoPrism Registry.

The situation is different when looking at the changes occurring through time for geographic objects that are being carved out from existing one to start their existence. For example, this occurs when boundaries change (e.g., split or merge) across administrative, health, statistical, or electoral units covering the entire territory of a given country.

When this is the case, capturing the period over which each unit has been in existence is not sufficient to rebuild these changes. To illustrate this, Figure 5 captures the changes that occurred through time for part of the districts of Uganda over the January 1, 1990, to June 30, 2005, period.

#### Figure 5 – Example of changes occurring over time for a subset of the districts of Uganda

![](https://lh5.googleusercontent.com/W1lHU\_iicFzFDMi3NwMuBuNNFhw0ODkfD1jiG0bkrlQSD7liSLq2j07IQVFjEaDnOb4sZLxkOHf226hgy6WHe0GI85CjaA22B3JmNMyEYVdPF0JoBdU8o-X3RCphCsnpf3QM\_7NmSfAggiB\_XWufEpXUpcDP3NmSnaCNCP7QQBaWok7eUp4j3wWH)

While the district of Soroti, for example, has been in existence over the complete period reported in Figure 6, its geographic extent has significantly changed twice over that same period. In this case, a CGR should be able to capture the period of existence of the district of Soroti as well as the two changes in question including the indication of the instance (single occurrence) of the district of Soroti from which the district of Katakwi in March 1997 and then the district of Kaberamaido in July 2007 have been carved.

For such cases, the GeoPrism Registry has the capacity to capture:&#x20;

* The date of the change&#x20;
* The type of change (split, merge, transfer, upgrade, downgrade)&#x20;
* The type of geographic object before and after the change (same type in the case of a split, merge, or transfer or different type in the case of an upgrade or downgrade)&#x20;
* The unique identifier and name of the geographic object before and after the change&#x20;
* Notes allowing to understand and/or track the change (e.g., the legal document in which the change is recorded)

It does then allow the user to generate a report containing all the historic changes (events) for a given type of geo-objects and this over a specific period in time. Please refer to [Section 6.5.3](geoprism-registry-tutorial.md#6.5.3) For more information regarding how the historic events information is being captured and included in such a report.

### 5.2.2 Unique identifier

Critical to data interoperability is the ability to uniquely, and therefore unequivocally, identify each of the geographic objects in the GeoPrism Registry and ensure that this unique identifier is used across information systems. Therefore, it may be beneficial to use geography as a neutral platform for the integration of information and data coming from different sources.

While the selection of the appropriate coding scheme associated with each type of geographic object is not a functionality of the platform, the GeoPrism Registry has the capacity to capture and maintain such a scheme.

The choice of an appropriate coding scheme to be associated with each type of geographic object is therefore critical as modifying the scheme once implemented in different systems can not only be costly but also have a significant impact on data compatibility as well as on the trust in the CGR content.

Please refer to the CGR guidance \[1], the master facility list resource package \[5] and the implementation support guide for the development of a national georeferenced community health work master list \[6] for more guidance on the choice of an appropriate coding scheme.

### 5.2.3 Master vs non-master

The primary objective of a Common Geo-Registry is to share the authoritative data coming from the governmental entity having the official curation mandate over it. This is what is being referred to as the master data and information \[5,6].

While this is indeed the type of data and information that should be hosted in priority in the GeoPrism Registry to serve as the source of truth, it is possible that either the master data/information is not available, not of quality (incomplete, out-of-date…), and/or not accessible.

In these cases, and to ensure the continuity of operations, the GeoPrism Registry can host, manage, and share “non-master” data/information in parallel or in complement to the master one (meaning that both types should be clearly differentiated) as well as facilitate the converge the two lists once the master version is available, of quality, and/or accessible.

### 5.2.4 Accessibility

The full value of a Common Geo-Registry is expressed once its content is accessible to the largest number of users possible.

This being said, it is possible that not all content can be made publicly accessible, at least not at first (appropriate government approvals might be required, a certain level of quality needs to be reached and/or the necessary policy and legal framework be in place).

The GeoPrism Registry currently provides two levels of access (referred to as visibility in the platform) for the geo-object types, lists and spatial data it contains :&#x20;

* Public: The item is accessible to any user from within the platform and to external users through an API&#x20;
* Private: The item is only accessible to the organization having the curation mandate over it

Having these levels of accessibility for the content allows the platform to respect the current accessibility policy that each organization might want to apply to the content they are hosting in the platform while still benefiting from the functionalities it provides, but also to change such a level as the data sharing policy associated with this content evolves.

In the future the GeoPrism is meant to add other levels of access (restricted to given organizations for example), to apply these levels to hierarchies and to implement the rules reported in section 2.7.4 of the [CGR guidance document](https://healthgeolab.net/DOCUMENTS/Guidance\_Common\_Geo-registry\_Ve2.pdf).

### 5.2.5 Documentation (metadata)

Documenting the content of the GeoPrism Registry in a way that informs the users if such content corresponds to their needs is key to the proper use of this content

At this stage, GeoPrism Registry allows the authorized user to fill, manage and share a medata profile for the following key elements managed in the platform:&#x20;

* Organization&#x20;
* User Geo-object types and groups&#x20;
* Hierarchies&#x20;
* Lists&#x20;
* Spatial data

The content of such a profile is different for each of these elements and described in more detail in the GPR tutorial.

### 5.2.6 Languages and character encoding

In addition to the possibility for GeoPrism Registry user’s interface to be localized (see Section 3.4) users have the possibility to import, store and share the information associated with each data element in the local language.

Thanks to the libraries it integrates, GeoPrism Registry is able to cover any language as long as it is based on the UNICODE character encoding system.

### 5.3 User roles and their rights

This section describes which roles are currently implemented in the GPR platform before describing which rights each of these roles has.

### 5.3.1 Roles covered by the platform

These are the roles currently implemented in the GeoPrism Registry:&#x20;

* **System Administrator (SA):** User who is part of the GeoPrism Registry cross-sectoral governance structure who can set the platform, manage organizations and Registry Administrators user accounts, and view the public data across organizations.&#x20;
* **Registry Administrator (RA)**: User attached to a given organization and who has all the privileges of a RM plus the possibility to define user roles, create Geo-Object types and hierarchies and consult all the data under the mandate of his organization.&#x20;
* **Registry Maintainer (RM)**: User attached to a given organization and who has all the privileges of a RC plus the possibility to edit the CGR content for specific Geo-Object types under the curation mandate of that organization.&#x20;
* **Registry Contributor (RC)**: User attached to a given organization and who has the possibility to consult the CGR content for specific GeoObject types under the curation mandate of that organization and submit change requests about them.

In addition to the above, you can also access the platform through a REST API (See [Chapter 4](external-system-integration.md)) that uses the same roles for authentication.

There is no anonymous user being implemented. The plan is for any deployment to be able to use the API to create an interface that will provide access to all the public data stored within the GPR.

### 5.3.2 Rights by role

**The tables below present the rights by role currently implemented in the GeoPrism Registry. These are organized according to the steps in the CGR data/information flow (**[**https://healthgeolab.net/DOCUMENTS/Guidance\_Common\_Geo-registry\_Ve2.pdf**](https://healthgeolab.net/DOCUMENTS/Guidance\_Common\_Geo-registry\_Ve2.pdf)**):**

![](https://lh5.googleusercontent.com/-CR9Ja-Sp0pcDLp4Pw10qV\_02iquXyUJZqWK2nac8uKDrQ2jqZXHQC24oolVCvCqZVCdZ-aozpO4tn8lLpdeee\_zyGM4t4PmjYRw\_dPhEqXhd-2nGh-0rQxwKtXjrmAu0GcT5Yg9jWACJJIf-BLNyM2MmvF2UbtKnRKY3P9jCM9QdzcgwAVoTvUx8g)

The legend for the numbers indicated under each role is as follow:&#x20;

1. For all the organizations&#x20;
2. For his organization (for all the geographic object types)&#x20;
3. For his organization (geographic object types over which the user has the curation mandate)

Two examples on how to the read the information for each role:&#x20;

* Cell highlighted in gray: The SA role can view the information of an organization for all the organizations.&#x20;
* Cell highlighted in blue: The RA can manage data elements (including classification tables) for the private geographic object types and/or hierarchies for his organization (any geographic object type)

![](<../../.gitbook/assets/Screenshot from 2022-09-28 14-54-14.png>)

![](<../../.gitbook/assets/Screenshot from 2022-09-28 14-55-46.png>)

### 5.4 User interface

This section describes the user interface of the GPR platform for the home page as well as the modules the users are having access to depending on their role.

### 5.4.1 Home page

The home page is the first view the user sees after logging in to the GeoPrism Registry. It is organized in such a way that it allows users to (see figure below):&#x20;

1. Access each module either by clicking on the corresponding module icons (1 in the figure) or the module item from the burger menu&#x20;
2. Access the settings for the platform from the burger menu&#x20;
3. Switch locales for the interface in case different locales have been imported&#x20;
4. Access its own user information by clicking on the username appearing next to the burger menu&#x20;
5. Log out from the burger menu&#x20;

![](https://lh4.googleusercontent.com/FPRq72yf4zxA1wdnDeFUdOQAnL3BPAu-Vfv0orIMyFHi11-IJWS0FA6PAR5qFh70UsxhayD6H1nmejCAH4M7eI0XhhbzafiZIkCfSrwDoJZna\_MvZsnJwsqlANd4UpnPNP6srsWjNiV6qX8aaA8MXXCUcIlJeecT6KZ8cc8U05NkvjCbnH80G9A-DA)

The functionalities provided by the GeoPrism Registry are organized in modules. The modules that a user has access to is determined by their role (see [Section 5.3 User roles and rights](geoprism-registry-key-components.md#5.3-user-roles-and-their-rights)).

For example, the home page will look like this once accessed by a user having a RC role:

![](<../../.gitbook/assets/pasted image 0.png>)

### 5.4.2 Modules

The functionalities of GeoPrism are organized in modules accessible from the home page or the burger menu. What can perform in each module depends on the user role is described in the [rights by role section](geoprism-registry-key-components.md#5.3-user-roles-and-their-rights).

The modules currently included in the GPR ar as follow:

| Module name and icon                                                                                                                                                                                                                  | Module description                                                                                                                                                           | Actions that can be performed in the module depending on the user role                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ![](https://lh4.googleusercontent.com/cbKIQmz903iImxE57c27KI1tByy6v3Qju0p4AlPOSKuNRvqJaXgVxeBPYSYKWQgaqlESoG9-SJfRGSKtreIBQD4X-Z0PLsnUOfohD3GqO-ZNldeXFvOI5e-Qol2bfZNn3EUqnz6sAWIjr58unYEyUzZG2LxNHKnZIZkto2x61f2jGc3RCx7q18QxWQ)     | The Geo-objects and Hierarchies module is used to define the Geo-Object types being managed in the system as well as the relationships between the Geo-Objects types.        | <ul><li>View the Geo-Objects Types and Hierarchies and corresponding metadata created by all the organizations or those that are made public </li><li>Create, edit, or delete Geo-Object types and groups for the organization the user is attached to </li><li>Create, edit, or delete custom attributes for Geo-Object types or groups </li><li>Create, edit, or delete Hierarchies for the organization the user is attached to</li></ul>                                                                                                                                                                                                                        |
| ![](https://lh6.googleusercontent.com/d5tkzGVrwEmt7L9eImm1gQiCfR5lMqKLfXfGRAMAbI1odmx4i-T46IFaJ62aHBorCGW3Y3doZb941YkWbHuCLL11nTz-wvft6z4S1oM8W9v2O\_8TlsvmjhZO-qGaNSD5eFa\_fX65xA9J-9ZShwwcZOQiRL5AnAJPXzT8x5FYjMK7opioZKf1GiIQLw)   | The Lists and Spatial Data module is used to manage the lists and spatial data of Geo-Objects types as well to make modifications to the Geo-Objects types from those lists. | <ul><li>Configure the lists and spatial data as a set (single, frequency-based, period-based) </li><li>Manage the metadata, set visibility and authoritativeness for both lists and spatial data </li><li>Manages versions </li><li>View public and private lists and spatial data and their corresponding metadata </li><li>Explore lists in tabular format using column filters and sorting </li><li>View corresponding spatial data of lists on map (redirected to Explorer module) </li><li>Add or edit Geo-Objects in a list directly or through a Change Request </li><li>Export lists or spatial data with associated metadata and data dictionary</li></ul> |
| ![](https://lh5.googleusercontent.com/9dP\_91U74lb5CW3ZEESMYcoZq6MyusQY9AXzznNqL9kiz8vZT4Xxf\_CuFYU4FKQ5DO5Hp9vwv4w0JTOuv3ufYmWrS1z-myZy7aD4BLMdrCeFqfiBGJnun8t1V38NQgd6MhjGOHxfageowUlk9wri6GyOGTbcWGv1o5\_wLUokVHWKAcLXErTDskuryA)  | The Import module is used to upload and/or update data in the GeoPrism Registry using spreadsheets or shapefiles.                                                            | <ul><li>Import a spreadsheet from a local computer </li><li>Import a shapefile from a local computer </li><li>Configure imports to align with Geo-Object Types and Hierarchies registered in the system </li><li>Merge disparate terminology (e.g., different names for a village) of a Geo-Object by registering semantic differences as synonyms</li></ul>                                                                                                                                                                                                                                                                                                        |
| ![](https://lh4.googleusercontent.com/aVLbT3UPzjQmmtHTsiolSQeKDxdC9pWo--h03OOXZJ8A13I4HwbvkRORzBmLChslQGm9ibIKGfFCFd29lleQwY4SXimZjo6nWTJIram4l2IH2yRhOOsrzYhwBC9B6SdPCxEw255HHSjS6kGJAPbSvr274-zvJzQnSCFrUCA2qx6zDmESjaYl2ZeS2w)     | The Schedule Jobs module is used to monitor and manage the progress of the data being imported.                                                                              | <ul><li>View the progress and status of imported data </li><li>Resolve detected problems with imported data </li><li>Cancel data import in progress</li></ul>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| ![](https://lh4.googleusercontent.com/2AzauTT9dlCng\_FJg7j4hbd\_BBJ7HEumvv0cPD3vlMR67rWigk149iRZ9HDWmxO1Wk5M2yuvFAveHnTTveOpwR5dSGnZsZSt1v4gqkcWFnQvPpuh-jsQ4kydCRcOeeya7H6tXYLwfnIzr3tcadoBipaPGKfHzKlOzP8kdmLihHA6IS2WFcxz-F-gxg)   | The Explorer module is used to explore and manage the geo-object types through their geometry (spatial data)                                                                 | <ul><li>Search and visualize Geo-Objects (including types and groups) </li><li>Visualize Geo-Objects for a specified date </li><li>Add context layers to the map </li><li>Zoom in and out </li><li>View the attributes, hierarchy, and geometry of Geo-Objects and their changes through time </li><li>Edit attributes, hierarchy, and geometry of Geo-Objects</li></ul>                                                                                                                                                                                                                                                                                            |
| ![](https://lh4.googleusercontent.com/vvYxUE5Zo2A-zU3h-FY6k78AWdpA\_snKoXUv1vCxnBq8AgcfFeMNfKxpc6ru1MLEngqtbzVDS4Ojh6gVDJENrOrLatoNFC8X5cfB\_5paCTbKzdvirnUyXwsip7ZQWoBF5jBpemY7azBlM3XaNv\_ARlzF6NiYUt6g1qJH6Ij9AWgZyGQ\_ReobzVokJA) | The Change Requests module is used to submit and manage the change requests that have been submitted.                                                                        | <ul><li>View the details and status of all pending, accepted and rejected change requests that you have access to </li><li>Review all properties of the original Geo-Object and the proposed changes </li><li>Add historical notes to Change Requests to help others understand why it was rejected or what might have been changed during the review process. </li><li>Accept or reject submitted change requests </li><li>Submit a new change request without needing to find that object in a</li></ul>                                                                                                                                                          |
| ![](https://lh6.googleusercontent.com/\_7gaGQn3hup5AZcUpu56QYU0AK1s9p9BnlfksR3\_eyL4pTzOR0bWxteLA1i6QK5-7ZIHHJbQSiWW\_srbl-L9PEBwzB5cEI7E3WPCEiRXD9dCcIdhXwNywOJZwHrY4T2zLwvrmkJMCEo9UHW1vLwOdc0Ql513F4GoMkagiFRC6HD6UW1daeJs8hEijA)  | The Curation module is used to monitor tasks that have been automatically generated by the platform as part of curation tasks                                                | <ul><li>View all open and completed tasks </li><li>Mark tasks as complete</li></ul>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| ![](https://lh4.googleusercontent.com/FpZPrMT915hCVXVI2hPRauyiqcxNIvfduCV6EUbWa\_elIsBKFim5yxbOZgf-mlfMPqVKFYVo-jddby7p0Ojl6BeWXCr9wnE13WSzi9uFyTnyqq51uvi6s829HL1oXcyQefcv5gG6Z9hoIq7MpOPdN6s814e\_Cks4c5ZMqsKIk1YqOiJYTVpbVcYTdQ)   | The Historical Events module is used to capture additional information about the changes that happen to Geo-Object Types through time.                                       | <ul><li>Capture the information linked to specific types of changes happening through time for the geo-object under the curation mandate of the organization (split, merge, reassignment, upgrade/downgrade) </li><li>View the additional information that has been captured </li><li>Export the captured the information in a machine readable tabular form (Ms Excel file)</li></ul>                                                                                                                                                                                                                                                                              |

The general layout of modules is structured in four ways:&#x20;

1. A unique window containing a set of fields to be completed (import)&#x20;
2. A unique window with horizontal sections that can expand depending on the actions being taken (scheduled jobs, change requests, curation)&#x20;
3. A window separated into two vertical panels (geo-object type and hierarchies, lists and spatial data&#x20;
4. A unique window with side panels that can be displayed or not (explorer)

For types 1 and 2, the user will start from the top of the window to complete the desired action.

For type 3, the user will first have to select items (geo-object types, hierarchies) in the left panel for the information to appear in the right panel and then be able to complete the desired action in that panel.

For type 4, the user might first have to expand one of the panels before being able to complete the desired action.
