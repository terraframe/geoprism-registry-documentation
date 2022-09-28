# GeoPrism Registry Tutorial

### 6.1 GeoPrism Registry Sandbox

### 6.1.1 Purpose

The GeoPrism Registry sandbox is a controlled testing and demo environment that resets at 12:00 AM Geneva, Switzerland (GMT+1) every day. This allows users to test and learn about the GeoPrism Registry functionalities without the risk of affecting some specific content.

Because of the above, the sandbox is used as the reference for all the examples included in the present tutorial.

### 6.1.2 Organizations and roles

The Tolkien dataset has been designed in such a way that it is distributed among 3 organizations: &#x20;

* Ministry of Home Affairs (MOHA)&#x20;
* Ministry of Health (MOH)&#x20;
* Ministry of Education (MOE)

For each of these organizations, a Registry Administrator (RA), Registry Maintainer (RM) and Registry Contributor (RC) user role has been created. Users can also access the demo instance as a System Administrator (SA). Please refer to the [CGR role section ](geoprism-registry-key-components.md#5.3-user-roles-and-their-rights)for more details on each of them.

### 6.1.3 Content

The sandbox contains fake data that has been generated in order to facilitate testing sessions and demos that would cover a large number of use cases including changes over time.

This “Tolkien land” was initially created for a training that took place in the Philippines in 2019. It has since been expanded for GPR demonstration purposes.

#### Geo-Object Types

As it currently stands, the Tolkien land dataset contains Geo-Object Types under the curation mandate of three different organizations as follows:&#x20;

* Ministry of Home Affairs (MOHA)&#x20;
  * Provinces - Polygons&#x20;
  * Counties - Polygons&#x20;
  * Shire - Polygons&#x20;
  * Villages - Points&#x20;
* Ministry of Health (MOH)&#x20;
  * National Hospitals - Points&#x20;
  * Referral Hospitals – Points&#x20;
  * Health Centre – Points&#x20;
  * Health Posts – Points&#x20;
  * Catchment areas – Polygons&#x20;
  * Community Health workers - Points&#x20;
* Ministry of Education (MOE)&#x20;
  * Universities - Points&#x20;
  * Colleges - Points Secondary schools - Points&#x20;
  * Primary schools - Points

#### Hierarchies

Organization specific hierarchies based on the above Geo-Object Types and the geographic location (latitude/longitude) or the geographic extent (polygon) of each Geo-Object are also being implemented in the dataset.

The hierarchies that were created per organization are as follows:

* MOHA&#x20;
  * Administrative structure hierarchy: hierarchy showing how the different administrative divisions are aggregated from the lowest level to the highest.\
    ![](https://lh3.googleusercontent.com/4UsBNirqTK0IpOyc3fNSZjMC1YjokQAFKMBgvlNSJc8zeLUCVTXtpd3ggyBcAZOoAJctNYT0NahJiqdXXEZxUspxTkZ8NSPM7i7\_z-GPXJVwx-gwt9oGIsaWlhDXZhc5\_FG4C2ZAjMMqi-EpXKxgniJNYOieG7kBY2xE3L8qctSLAknn\_-MjME5d)
* MOH
  * Community Health Workers (CHW) - Health Post hierarchy: hierarchy linking each CHW to the health post she/he is reporting to\
    ![](https://lh3.googleusercontent.com/j1wjHMr6XV8aWsAx0gsE1a0nAHlMv0LwGon0pmQ0JArSpyJuVn0s7skJPhjAoia901W9q4XS7KicWlqeNY3oPHlBzt9x4b9HrIbjPezY6wdj5DT9p5e3aiK5D0zlR8i0CPN32URr2hEd\_-TofVNARBktra5vRH0MysSqSv94OM9BWO8bjfeIKpOL)
  * Health care referral hierarchy: hierarchy that describes how patients are being referred from the village to the national hospital level\
    ![](https://lh6.googleusercontent.com/wMYOwYZMl6dagIUS3L7V\_vWofo5duYia-TdEU\_8IGpQoys5g2vOqtDzxT-g0FukNln0-WSG6RBHM75Uk-uw\_m5u5KzgkS-eXdypd09WYdhAkFU6mYmjKjWA3e4JbB1AoBaPPAY9XwjYTavv7UhYvroJleUbTozgC72mIOcbbpyH4fnisISZrUMEa)
  * Health geography hierarchy: hierarchy that allows to link each health facility with the Shire in which it is located\
    ![](https://lh5.googleusercontent.com/gQLefeAo5O9U1KfMVbWth17LvEN8JOKiukH0ftIPbn6tOjdBOPaq6Z\_n5UhCaARpmJTPHyiBQ5X0QpTlpI-UQiuPaPnGEXlWc3z3DsyWBA3MqeVlvFqwWVhrqgExuK9ESpgajv7IaW7vpu9XolMMKg35Mj2u1UG9uLyKijKwAkrimtekp02r9RxP)
  * MOH-MOHA Village hierarchy: hierarchy linking the MOHA with the MOH village for the purpose of managing MOH-specific hierarchies and lists\
    ![](https://lh5.googleusercontent.com/FDOl2jLp3PSDFbP6S6DXpFI2EX6J\_K6oYNKjrcpSNZPVAIubGRZKhVpWpa1woU\_UbriRjL2aQEMmJwEsIOYGDcQ1C09zTbCLyffyPkdOT3\_SNCYSX34ai3DVZhfNzLPt5KyAsvEHIYSwtvruyX8YEM0DVL7RljOGTNtzk0EzSr9Mu5VR9dbJPaIG)
* MOH
  * Educational geography hierarchy: hierarchy that allows to link each school with the administrative division in which it is located\
    ![](https://lh4.googleusercontent.com/eNqXvK5Q1v1XKOmcnD2cW3Q9JAOYf8KxstTjpim\_azV7SF-a\_XyJrmeiwv8xfoTJ7gOG4UiuCk\_8YDjhaNJpbYx1CSf2TDsACNah91hIP9iFfwLlY5OeNfQeNOiMKjJoLI-6\_93Neln0fYqAmQ7DO5GQnySj0iLGbVWCtuVfyYQzTYP4BtyquzQb)
  * Educational path hierarchy: hierarchy that describes the journey through which students go through during their education\
    ![](https://lh4.googleusercontent.com/v7vCOkEgbMpdrnzfLIJOmrhQT89tZR-bmf9WDfklkKniIhMFxZguGEI5R4G2QR5GzIl3iSuWgPR\_TcDmumb3lAx1AfJdCvk9orBIBS72EiOR5CeJIumanfUOT3S\_5O6cCXlJH-tO9JzNovtA0iicy8eRrYT5uwi17ctXtN2maQEwlvu6OGhF\_GaY)

### 6.1.4 Access

The GeoPrism Registry Sandbox can be accessed from the following URL : https://demo-georegistry.geoprism.net

The sandbox is currently accessible through the following set of roles to external users.

![](<../../.gitbook/assets/Screenshot from 2022-09-28 15-56-36.png>)

### 6.2 Logging in

There are two ways a user can log in to the GPR. These methods are described in detail below.

### 6.2.1 Local GeoPrism Registry credentials

Logging in using this approach is done following these steps:&#x20;

1. In the GPR login page, type the username and password assigned to you in the appropriate fields.\
   ![](https://lh3.googleusercontent.com/nyz9L2nR22zu\_gPQQooghRC9Fcm\_6xAyx3sMtGZzP6vzvxDDzCls0UUZogMb9qf1wixR-5o1MW3DJpORQ3xln2KLh64W2aJIbfSKP46LqYH2MQhu-9ADcQ53wF-OA8Ok-xPWGlN8IGUR6tb71xtfq9QRdbjGgzXZbF5WdM0xEl3p8vkyTsGXfOEuVg)
2. Click the Login button.

### 6.2.2 DHIS2 credentials

The GPR supports logging in with DHIS2 credentials using OAuth 2.0 for a specific DHIS2 instance.

{% hint style="info" %}
To log in with this method a user must first exist in both the GPR and DHIS2 instance with the same user name and the GPR user must have OAuth enabled. For more information about creating or configuring GPR users to use OAuth see the user management section.
{% endhint %}

{% hint style="info" %}
Requires the DHIS2 instance to be registered as an external system in the GPR.
{% endhint %}

1. Ensure that the DHIS2 instance you want to use to connect is registered as an external system (see the [registering a new DHIS2 external system](external-system-integration.md) section for more info).&#x20;
2. From the GPRlogin page, click the Log in with DHIS2 button.\
   ![](https://lh5.googleusercontent.com/AXAUGJ48WzTZ1C4hpzBfN4xgiao\_gneE9Qn70zqN8lXUy0RgvdO\_-xiTmgS8eUyYCBVaAw-vINt74oVwSycNkSaOIBLvk9VxT2ASWZn\_TwvruJHl2UhSIyCazbnoi6rTbxCa8L\_cyqTtdWyVBM6cxXJvOCkVdzYah\_0-7n98Lrzr-2qCz7lBqucR)
3. If there is more than one DHIS2 external system registered, a dropdown will appear of all the registered DHIS2 instances. Select the instance you want to use to login with which will route you to the login screen of that instance. If there is only one system you will be routed to the login screen of that instance without needing to select that instance from a dropdown.\
   ![](https://lh3.googleusercontent.com/\_G0cZal4S6oKRWM9VpnneSspLnaWQAzpT8nOqD2hPmuJljYEkaioiSojqd65OXll8XvloLxy9p3AhrhzQXM6Am7Y1GlXn247BWrztT4KrT8Jxlxj74-Cxdh8i-9UUHNLTCFagivBrhjjQV6daOJ0uEw57ccm1\_6o6vfCoQMURB6X11PCfuOISLno)
4. Login to the DHIS2 instance. Once logged in, you will be asked to authorize the georegistry. Click Authorize to continue.\
   ![](https://lh4.googleusercontent.com/ICTjXYND51ZhyqMA8oSIUnM0yQn7lztBqouGpdDmVCdCHoIEeAt3JEs3UUyWn1HPuqzTMMCH3x4RpFnd3NvlYHMA0xHyEQiCv6uXd\_TVg89tF02p275T7BQ2BShsq9QVw-tJ-KTMiCceCTZMrajH4QxmSD7dTZmuASlrKxH31k9CAV5iYt8ZjFMQ)
5. After clicking Authorize you will have access to the GPR instance you started in.

### 6.3 User management

This section describes how users are being managed within the GPR.

### 6.3.1 Add users

### 6.3.2 Invite users

### 6.3.3 Reset a forgotten password (local GPR credentials)

### 6.3.4 Change a password

### 6.3.5 Enable OAuth integration

### 6.5.3
