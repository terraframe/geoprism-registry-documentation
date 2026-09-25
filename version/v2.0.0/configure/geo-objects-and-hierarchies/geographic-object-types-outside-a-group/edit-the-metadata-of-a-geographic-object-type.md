# Editing a Geo-Object Type

{% hint style="info" %}
Registry Administrators can edit the metadata of Geo-Object Types under the curation mandate of their organization
{% endhint %}



1.  Navigate to the _Geo-Objects and Hierarchies_ page from the sidebar.<br>

    <figure><img src="../../../../../.gitbook/assets/image (84).png" alt=""><figcaption></figcaption></figure>
2.  Click the three dot menu option button to open the options for a Geo-Object Type. Select the _Edit_.<br>

    <figure><img src="../../../../../.gitbook/assets/image (82).png" alt=""><figcaption></figcaption></figure>
3. The _Manage Geo-Object Type_ window will open. Edit the Geo-Object Type information as necessary.

| Field                                                               | Description                                                                                                                                                                                                                                                                             | Required |
| ------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------- |
| Code                                                                | The unique human readable identifier. The code can be used to determine the uniqueness of a Geo-Object Type if duplicate display labels exist in the system.                                                                                                                            | Required |
| Label (defaultLocale)                                               | The default display label for the Geo-Object Type. The default value will be used if the default locale is selected in the language toggle or if another language is selected but no value exists for that language.                                                                    | Required |
| Label… (for any other locale that is installed in the system)       | Display label for any locales installed in the system. A common geo-registry can have as many locales installed as needed. The system will allow the setting of the display label for each locale.                                                                                      |          |
| Description (defaultLocale)                                         | The default description for the Geo-Object Type. The default value will be used if the default locale is selected in the language toggle or if another language is selected but no value exists for that language.                                                                      |          |
| Description… (for any other locale that is installed in the system) | Description for any locales installed in the system. A common geo-registry can have as many locales installed as needed. The system will allow the setting of the description for each locale.                                                                                          |          |
| Group Geo-Object Type (Group Membership)                            | The option for setting this Geo-Object Type as a group type.                                                                                                                                                                                                                            |          |
| Private (Visibility)                                                | The option for setting if the Geo-Object Type is private or public. Private makes the Geo-Object Type accessible only to people within the organization it belongs to. Public is visible (read only) to all organizations in the system.                                                |          |
| Geometry Type                                                       | The geometry type (point, line, or polygon) that all instance data loaded to this Geo-Object Type must adhere to.                                                                                                                                                                       |          |
| Enable geometry editing                                             | Sets whether the Geo-Object geometries can be edited through Geoprism Registry's web-based editing tools.                                                                                                                                                                               |          |
| Organization                                                        | The organization this Geo-Object Type will be managed by.                                                                                                                                                                                                                               |          |
| Concept Set                                                         | <p>The concept set this Geo-Object Type will have available to use on an attribute during import. This is how Concept Sets are used as constraints for Geo-Object values.<br><br><mark style="color:$warning;">IMPORTANT: This attribute can never be edited after creation.</mark></p> |          |

4. Click the **Submit** button.
