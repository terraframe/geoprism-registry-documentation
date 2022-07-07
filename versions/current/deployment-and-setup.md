# Deployment and Setup

### 3.1 License and citation

The GPR is released under a GNU Lesser General Public Version 3 license. The details can be found on the public code repository on GitHub.

### 3.2 Creating a new installation

{% hint style="info" %}
This documentation is written assuming you are using Amazon Web Services (AWS) with an Amazon Linux 2 operating system. While it is possible to install GeoPrism Registry on other environments, this documentation does not cover the configuration differences that may be needed.
{% endhint %}

#### Hardware requirements

The standard hardware for the target machine is an AWS r4.large server (16 GB RAM), as the GeoPrism Registry tends to be memory intensive, and 500GB gp2 (general purpose SSD) hard drives.

#### SSL

GeoPrism Registry is configured to use HTTP by default. Any SSL/HTTPS configuration should be done outside of the GeoPrism Registry web container. The recommended way to do this is to use a reverse proxy.

#### Installation with Docker (recommended)

All production GeoPrism Registry Docker containers can be found on Docker Hub along with the most current documentation for install and update.&#x20;

* https://hub.docker.com/r/terraframe/geoprism-registry

### 3.5 Organization management

The GeoPrism Registry supports the management of lists, spatial data and hierarchies across multiple organizations, so that only those with the responsibility to maintain data for a given organization can do so within that organization only.

#### 3.5.1 Create organization

Organizations can only be created by users with the System Administrator role.

1. Go to the Settings module.\
   \
   ![](https://lh6.googleusercontent.com/hQu5GCHC-h11UA08oAy4\_4ify1PS0M4z-l8ZrYALEH6jkZyaP0Ew7L8vxBUjOQNhB7mLn7eV-IEMvevGpRSbZYPpQ7oTPmK71OyfpQzpgX0oSPVVRMPCjBTUbTwiLsWf3k3xLkQqBS1vIH\_GAfc)

2\. Scroll down to the ‘Organizations’ section and click on the plus icon.\
\
![](https://lh5.googleusercontent.com/E2c1IFW2i0WQGlr0tVP8JshmoaNRJtGsdznHrRW-7sKhXfEvP9B6fGr2NhM\_U-n5VUYtDJ8qzvfG-G55tpB08\_s0iWQIRQsOyVJGHPDyAe5p8N6DV6iBddZNPSzi5CIr0CNNkzNm4PuuI2syK-c)

3\. Complete the ‘Organization’ modal that opens up.\
\
![](https://lh6.googleusercontent.com/ELMCDwJEaNJaQhr3Qpyq23Rb3jHZI8f-p9uhenPef\_CWIIg3TmPE2YcBoY8DO8FuI5Ueh9g5XmYCmpN5XqZSeDLnmvc3UpdVxW5qb8by-UYVJid4BUyHkyiTZ-K5sRV93wcOI03k-6IHf34Ltds)

| Form Field | Description                                                                                        |
| ---------- | -------------------------------------------------------------------------------------------------- |
| Unique ID  | Unique identifier of the organization.                                                             |
| Name       | Name of the organization in the default and any installed locales.                                 |
| Contact    | Details of the primary contact point of the organization in the default and any installed locales. |

4\. Click Submit. The organization now appears in the table under the ‘Organizations’ section in the Settings module.\
![](https://lh5.googleusercontent.com/tJ4fwkktvtDh3PojxBNFyBHr\_C\_9aeEE0gRIbEmoCuIriQnYfv9l-ms9MquFk0LG58daebLZNfwT5A67u48yJL4nESt7qFcJhpgXE9VpWZAyhTVakJhAYJ\_PFWYxqYtxs0FRBvFEc8H0lx9e37s)

### 3.6 Localisation

The GPR can be localized to different languages. The default locale of the system is English, however support for other locales can be added Localization management must be done by a System Administrator.

The GPR currently supports the following localization tasks:

* Exporting the localized values of the system to an Excel spreadsheet
* Importing the localized values from an Excel spreadsheet
* Extending the system to support new locales

{% hint style="info" %}
Note: Locales cannot be uninstalled.
{% endhint %}

#### 3.6.1 Install a new locale

Installing a locale enables the GPR to be translated to that language. This is the first step to enable a GPR instance to be translated. All locale options can be found here.

You must install all the locales you expect your users to need. Sometimes there are slightly different locales that all need to be included because a browser may have only one version and not the other. As an example, Khmer has two locale versions (kh\_KM and kh). Both of these locales must be installed and imported to ensure the Khmer language is shown in all browsers.

1. Navigate to the Settings page and scroll to the Localization section.
2. Click the + button to open the modal for installing a new locale.\
   ![](https://lh4.googleusercontent.com/FevM1EBoMs5dvLGO6vRn9M0VsM3mBKVE8toTmocj4Y5BIv\_tZBtQrkkvbWFC5IoHZTLFi9UgtHyZbNeIRcS31ImVCayGLiIHtoEo2c9twNWYMaWN1-aiZt1BUN52iemVTlc67uIxI-HbHxcHuQ)
3. Select the language and country. Click Submit.

#### 3.6.2 Export the default localization

All GPR text that can be localized is found in the localization spreadsheet. The localization spreadsheet must be exported by a System Administrator.

1. Navigate to the Settings page and scroll to the Localization section.\
   ![](https://lh5.googleusercontent.com/OkbhkgHsMEoPi-Re4ts2q9i64YmaN68mY-5q8CHynXjBnapVolGiPgQRzcO\_4yhHIVzKDq-Kog2atvv2Jt\_WUCOnLGVgrMvq6D8Vq2GesZXFAoYlDGdp7t7SIw2g-P7a9eL0\_Ov\_yCgdWv1qrA)
2. Click the Export Localization button to export the localization spreadsheet.

#### 3.6.3 Import a new locale

To set localized values in the system, the localization spreadsheet first needs to be exported and translated. After this is done, the spreadsheet must be re-imported.

1. Navigate to the Settings page and scroll to the Localization section.\
   ![](https://lh5.googleusercontent.com/OkbhkgHsMEoPi-Re4ts2q9i64YmaN68mY-5q8CHynXjBnapVolGiPgQRzcO\_4yhHIVzKDq-Kog2atvv2Jt\_WUCOnLGVgrMvq6D8Vq2GesZXFAoYlDGdp7t7SIw2g-P7a9eL0\_Ov\_yCgdWv1qrA)
2.  Click the Import Localization button to open the Import modal.

    ![](https://lh3.googleusercontent.com/d8OikI4Fw0-62715CH52JmIsbevygcL9fOtHdXo-0p-U59XWIeIC-7ZIZwE-ZSKD9B-xcYxGHr5XiTiwybIr1eV8\_UKNiPgKXrWrIBpx\_ohHb1ZBYw-j96VpNHE7FTq5RBTCiIwY3B6e2P1KXg)

#### 3.6.4 Edit a locale

The only values that should be changed in the localization spreadsheet are those in any of the locale columns, marked with the locale name in the header, e.g., kh\_KM.

{% hint style="info" %}
Note: Do not reorder columns, tabs, or change keys or column headers or types. The system needs this data to be able to read the spreadsheet.
{% endhint %}

The exported localized values are organized into tabs based on the type of text to localize:

* Exceptions&#x20;
* Core Exceptions&#x20;
* UI Text&#x20;
* Registry Metadata

#### 3.6.5 Switching locale

The language toggle is used to switch the GPR to any locale that is installed.

1. Expand the menu options from the hamburger menu in the top right of the GPR.&#x20;
2. If any additional locales have been installed the option will appear in the dropdown as displayed below. If no additional locales are installed the language toggle will not appear.\
   ![](https://lh3.googleusercontent.com/aUXzgf6BUerlFVTMrwnglPG8FbZkd4oAjOqtn0bfCgWHXHtH3KGvCupzXOsX7nmJ1p328Bc78OBKsL5zlUqVQffo5uIxNVsZfJ\_5PxAKy1aqS2xaiXC-EXiTNleoZxqjqHAHRcBg6RWQ5FwWBQ)
3. Select the locale option you would like to use. The page will refresh and the application will translate all text in the app that has entries for that language.\
   ![](https://lh4.googleusercontent.com/cTUx0qGYFLHhIIWTZmG3D79pwDWTxq2HlyPDAp\_xZJRe4ta4MIbHE40Gx0H70CzBzlaMFMF98Pg2-0pwS9m0bgQVsupY-AwRGJgZw9NVfCo4sXDjet14LQ-a6-NrOgjuAsxpgJQB0grS\_MAFhw)

### 3.7 System email management

The GPR uses email settings to send emails to users of the system. Email configuration must be done by a System Administrator.

{% hint style="info" %}
Note: The system only works with Simple Mail Transfer Protocol (SMTP) compliant email servers.
{% endhint %}

1. Navigate to the Settings page.\
   ![](https://lh6.googleusercontent.com/JNJ\_5kHmojp8sTrDQeraISNAF\_hGpqpM7MaGO5YHuVnStAu3FP7ESdUuCz11S0IsA8RlCEPXZA2Wfy9mPFcrsdAs5gKeb5KYuLFu7I2vHOj4pjWsuvhHdKKUEO9NCm2MYmUNRQHoXvPBVtiGSQ)
2. Under the Email section, click Configure.\
   ![](https://lh3.googleusercontent.com/rOpB1nFHNQJg59-fPShClxyYPSNkp2U-\_hLVmO73stA3pN8eZkuqpV9BPo8-U40qoWsp0y\_hNzdcJqikYgymgxrmIEvObw-pxTi1iZR5\_3VRlnTqQAIxOGbp7td-64CSdscpA1zsx0Ni4PcpOA)
3. Enter the values in the displayed form.

| Form Field | Description                                                                                                |
| ---------- | ---------------------------------------------------------------------------------------------------------- |
| Server     | The server URL hosting the SMTP system (e.g., email-smtp.us-west-2.amazonaws.com)                          |
| Username   | Username with ability to send emails                                                                       |
| Password   | Password for the user                                                                                      |
| Port       | Port used to provide access to the SMTP server. This is configured on the email server, not the GPR server |
| From       | An email address used to send emails                                                                       |
| To         | An email address used to receive emails                                                                    |

4\.  Click Submit.

### 3.8 Branding (Logo)

The logo displayed in the top left of the GPR is configurable by a System Administrator.

1. Navigate to the Settings page from the burger menu.\
   ![](https://lh6.googleusercontent.com/JNJ\_5kHmojp8sTrDQeraISNAF\_hGpqpM7MaGO5YHuVnStAu3FP7ESdUuCz11S0IsA8RlCEPXZA2Wfy9mPFcrsdAs5gKeb5KYuLFu7I2vHOj4pjWsuvhHdKKUEO9NCm2MYmUNRQHoXvPBVtiGSQ)
2. Under the Branding section, click on the edit icon (pencil) for the logo entry.\
   ![](https://lh3.googleusercontent.com/\_NsdcCTNVD5QFCM2AAq8C\_7zVQfarydd3qFuXsv4KISTOSxajC3sV0PkslfJ68ctZvkI6L07JWJtjxkdJVTBdBGhVFTdd47TeOYG34AM12LYjr6RqaxNhLEKQh3JkHEg0r3Rat47DjysgLZ6sA)
3. Drag and drop a file containing the logo into the modal.\
   ![](https://lh4.googleusercontent.com/0Yz7kaSSpjtop5MLNXJlWaantR9aUi38PlLWYc-OhZ7HdhxwfB8JUSm3Paa8nMGiqMYC4VGnlu\_4iPlVeOgyH-eH7JFtbQRSIORyEWqQMoigrFsVAcvldPbCR72FoYn519LNvYpyUXzd20lotg)
4. Click Upload.
