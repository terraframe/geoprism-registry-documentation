# Adding a Geo-Object Type to a group



1. Navigate to the _Geo-Objects and Hierarchies_ page from the sidebar.
2.  Click the three dot menu option button to open the options for that group. Select the _Add Sub Type_ option to open the form for adding a Geo-Object Type as a member to the group.<br>

    <figure><img src="../../../../../.gitbook/assets/image (82).png" alt=""><figcaption></figcaption></figure>
3.  Fill out all the required fields and any optional fields that are relevant in the form that appears. Note that some of the fields cannot be edited as these properties are inherited from the Geo-Object Type group.

    | Field                                                               | Description                                                                                                                                                                                                                                          | Required |
    | ------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------- |
    | Code                                                                | The unique human readable identifier. The code can be used to determine the uniqueness of a Geo-Object Type group if duplicate display labels exist in the system.                                                                                   | Required |
    | Label (defaultLocale)                                               | The default display label for the Geo-Object Type group. The default value will be used if the default locale is selected in the language toggle or if another language is selected but no value exists for that language.                           | Required |
    | Label… (for any other locale that is installed in the system)       | Display label for any locales installed in the system. A common geo-registry can have as many locales installed as needed. The system will allow the setting of the display label for each locale.                                                   |          |
    | Description (defaultLocale)                                         | The default description for the Geo-Object Type group. The default value will be used if the default locale is selected in the language toggle or if another language is selected but no value exists for that language.                             |          |
    | Description… (for any other locale that is installed in the system) | Description for any locales installed in the system. A common geo-registry can have as many locales installed as needed. The system will allow the setting of the description for each locale.                                                       |          |
    | Group Geo-Object Type (Group Membership)                            | The option for setting this Geo-Object Type as a group type. This is automatically selected and cannot be unchecked in this case.                                                                                                                    |          |
    | Private (Visibility)                                                | The option for setting if the Geo-Object Type Group is private or public. Private makes the Geo-Object Type group accessible only to people within the organization it belongs to. Public is visible (read only) to all organizations in the system. |          |
    | Geometry Type                                                       | The geometry type (point, line, or polygon) that all instance data loaded to this Geo-Object Type group must adhere to.                                                                                                                              |          |
    | Enable geometry editing                                             | Sets whether the Geo-Object geometries can be edited through Geoprism Registry's web-based editing tools.                                                                                                                                            |          |
    | Organization                                                        | The organization this Geo-Object Type group will be managed by.                                                                                                                                                                                      |          |
    | Concept Set                                                         | <p>Optional. The Concept Set used to classify Geo-Objects of this type. Selecting one adds a <strong>classification</strong> attribute to the type. When you import Geo-Object data, you map a column in your file to this attribute, and its values must be Concepts in the Concept Set.<br><br><mark style="color:$warning;">IMPORTANT: The Concept Set can't be added, changed or removed after the Geo-Object Type is created.</mark></p>                                                                               |          |

    <br>

    <figure><img src="../../../../../.gitbook/assets/image (87).png" alt=""><figcaption></figcaption></figure>
4.  Click the **OK** button. Once one or more group members have been created, you will be able to see them under the Geo-Object Type group in the Geo-Object Types section on the sidebar.<br>

    <figure><img src="../../../../../.gitbook/assets/image (83).png" alt=""><figcaption></figcaption></figure>
