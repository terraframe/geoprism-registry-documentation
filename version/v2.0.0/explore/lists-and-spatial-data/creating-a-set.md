# Creating a Set

{% hint style="info" %}
Registry Administrators and Registry Maintainers can create sets for the Geo-Object Types under the curation mandate of their organization.
{% endhint %}

A set is the configuration that defines a container for creating versions of lists. See [Key terms](README.md#key-terms).

1.  Navigate to the **Lists and Spatial Data** page from the sidebar. On the left, click the Geo-Object Type under its organization.

    <figure><img src="https://lh5.googleusercontent.com/l_CMQeZLPJuwSJnAJO5DmWtkN0Q5L5PbnilvjjzdFl7NBSDTYCcjxNjBEhX3d9XLYa9NUbV_WZkR_F16PmdVhenTc2goHPrcTbnDSv_3Hr6FP3rupPLM3_0GcYQVxlchXjYmLmTA7PcOQtUyXgH_8TFOTja-1EY_wKr2kKngns6_6FloApXgci5xsA" alt=""><figcaption></figcaption></figure>
2.  Click **Create New List and Spatial Data**.

    <figure><img src="../../../../.gitbook/assets/image (17) (2).png" alt=""><figcaption></figcaption></figure>
3.  The **Configuration** window opens. Choose the type of set. It can't be changed later.
    * **Single date:** one list of the data as it was on a single date.
    * **Frequency-based:** a list for each period at a fixed frequency from a start date.
    * **Period-based:** a list for each period you define.

    <figure><img src="../../../../.gitbook/assets/image (5) (2).png" alt=""><figcaption></figcaption></figure>
4.  Fill out the form:

    | Field | Description | Required |
    | ----- | ----------- | -------- |
    | Code | The unique identifier of the set. A code is generated for you, and you can replace it. It can't be changed later. | Required |
    | Title | The title of the set, with one field per installed locale. | Required |
    | Description (Abstract) | A description of the set, with one field per installed locale. | Required |
    | Geo-Object Type, Geo-Object Type Code | The Geo-Object Type the set covers. Filled in automatically. | |
    | Include Latitude and Longitude | For point Geo-Object Types, adds latitude and longitude columns to the list. Selected by default. | |
    | Hierarchies | One row for each hierarchy the Geo-Object Type belongs to. Select parent Geo-Object Types to add their codes and labels as columns. | |
    | Group hierarchies | For a group, the hierarchies of the Geo-Object Types in the group. | |
    | Filter | Only include Geo-Objects that match. Choose an attribute, a condition (**Equals**, or **Exact** for a classification) and a value. Click **New** to add another filter. Filters can only be set when the set is created. | |

    <figure><img src="https://lh4.googleusercontent.com/XC9BhDN9ZDODe4AL4pv7MRJZISWIbTPy2mgQ3ym2Lb91Ux7XvROZF0UUYr1qPxfz5JchoupwAWE9Xl0SHTuxI8vWV_ZG_U26gxjIg12NXtDfsg5H9j8UKQsHiDVa8-3fz_mi89_lodENjnmJYCbG3nskELNTaN5QZmQYQWoVRk0V6v2YbECd4Zn_zw" alt=""><figcaption></figcaption></figure>
5.  Fill out the dates for the type of set you chose:
    * **Single date:** the **Valid For** date.
    * **Frequency-based:** the **Frequency** (**Annual**, **Biannual**, **Quarter** or **Monthly**) and the **Start date**.
    * **Period-based:** click **New** to add each period, and enter its **Start Date** and **End Date**. Periods can't overlap. A warning appears if there's a gap between periods.

    <figure><img src="https://lh3.googleusercontent.com/bHrIx2WV26gpgq3o-NBBKouMEdNrbpqJbPX_Y7q3t4qOBCpoJo0daQrgkViPM9Kis1cVYNZk-alLw484EaxAmljk23BylvPXYwoURUgb1MixPcPYIr3szXVP7DiBxwNAwWC2cVkAAivcTs8N8QkeIKuN__rzG-Kxxz8qQmKmTJ4moVYtS3JOLlvg3w" alt=""><figcaption></figcaption></figure>
6.  Fill out the **Metadata** section. It has a **List** tab and a **Spatial Data** tab, and both have these fields:

        | Field | Description |
        | ----- | ----------- |
        | Title | The title, with one field per installed locale. |
        | Credit | Credits given to any individuals or groups. |
        | Description (Abstract) | A description of the contents. |
        | Process | The process used to create and curate the data. |
        | Status | The progress so far in creating and curating the data (for example, ongoing or completed). |
        | Access Constraints | Any access constraints. |
        | Use Constraints | Any use constraints. |
        | Acknowledgements | Any acknowledgements related to the data. |
        | Disclaimer | The disclaimer. |
        | Contact name, Telephone Number, Email Address | The person to contact with questions (under **Primary contact**). |

        <figure><img src="https://lh4.googleusercontent.com/KoOZcldBb_Xnjhq-6R7qa5rhQ_6gWA12JaRzN_da6_U6vLxuLXYdaBxniYIbUYngMBrVf2VnyjA1HgBYTNhftZAAUZYr4aGw2mtBu9GIdJs6jCM8ekLe-f6Bmz77pNPdCisXnVoCzdbTON-HqBhlLM2OAFZyhe1FmkrQE2yCl0gS2OeDzl0TEjTVog" alt=""><figcaption></figcaption></figure>

    The **Spatial Data** tab also has:

        | Field | Description |
        | ----- | ----------- |
        | Topic Categories | Topics covered by the spatial data. |
        | Place Keywords | Keywords describing the places covered. |
        | Update Frequency | How often the spatial data is updated. |
        | Lineage | The process history or overall quality of the spatial data. |
        | Languages | The languages the spatial data is captured in. |
        | Scale or Resolution | The scale or resolution the spatial data was captured at. |
        | Spatial Representation Type | Always **Vector**. |
        | Reference System | Always **EPSG 4326 (WGS 84)**. |
        | Report and Specification | A link to the report and specification of the spatial data. |
        | Distribution Format | Always **Shapefile**. |

        <figure><img src="https://lh5.googleusercontent.com/7VEay15EN2fY8UKdO_rFiM8BoT9_VSbrSigxxESDD7ntkY-sns1bKhtTrZdwD4IjENAqIyHO1vvyXxIE_YeW0aN-Gwibf70kcBrmnYV60rkkX-2kgQczypjIgyi-HEpqV8FmzLGe_wvL3TRfefwcTUXnhKRy2Rh92E-FDSxMRqGfP0rcliZVT43Sfg" alt=""><figcaption></figcaption></figure>
7.  Click **Submit**. Geoprism Registry creates a working version for each date or period of the set.
8.  The set appears on the page. Click its title to open it.

    <figure><img src="../../../../.gitbook/assets/image (25).png" alt=""><figcaption></figcaption></figure>

## Setting visibility and authoritativeness

Each version's **List** and **Spatial Data** has its own visibility and authoritativeness. You set them in the version's metadata.

1.  Open the set and click **Metadata** next to the working version.

    <figure><img src="../../../../.gitbook/assets/image (15) (2) (1).png" alt=""><figcaption></figcaption></figure>
2.  On the **List** and **Spatial Data** tabs, set:
    * **Is Master:** select this if the list or spatial data is the master (authoritative) data.
    * **Visibility:** **Public** (visible to all organizations) or **Private** (visible only to your organization). Public isn't available for a private Geo-Object Type.

    <figure><img src="../../../../.gitbook/assets/image (27) (1).png" alt=""><figcaption></figcaption></figure>
3.  Click **Submit**.
