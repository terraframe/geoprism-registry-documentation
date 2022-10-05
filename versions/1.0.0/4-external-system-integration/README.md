# 4 External System Integration

The GPR supports integrating with external systems to help facilitate the exchange of data between systems. Registering an external system enables the GPR to send data to an external system instance in a predictable way. This is useful to ensure that data in another system is using updated data from the curated data in the GPR.

### 4.2 Register an external system

The GPR supports integrating with external systems to help facilitate the exchange of data between systems. Registering an external system enables the GPR to track data from one or more external system instances. The primary goal is to enable the ability to store external system identifiers in the GPR so that they can be used to reference objects between systems. By storing both a standard GPR identifier and external system identifier, the GPR can maintain a mapping between object instances in the two systems. The external identifiers are set in the system through the data import process.

Registering an external system can only be done by a Registry Administrator and that external system will only be available to the organization that Registry Administrator is a member of.

### 4.3 Synchronize an external system

Setting up an external system synchronization enables a user to push data to that external system. Synchronization configurations require an external system to be registered and the external identifiers to be set through the data import process.

The GeoPrism Registry currently supports integrations with the following systems:

* District Health Information System 2 (DHIS2)&#x20;
* Reveal&#x20;
* Fast Healthcare Interoperability Resources® (FHIR)

The following sections provide more details for the integration of the GPR with these different systems.

#### 4.3.1 DHIS2

**Compatibility**

Not all versions of DHIS2 are known to be capable of integrating with the GPR via OAuth. The following table represents whether or not the steps in this document have been found to work with the listed version of DHIS2.

| DHIS2 Version | Integration via OAuth |
| ------------- | --------------------- |
| 2.35.1        | No                    |
| 2.35.0        | No                    |
| 2.34.2        | Yes                   |
| 2.33.7        | Yes                   |
| 2.32.7        | Yes                   |
| 2.31.9        | Yes                   |

**Registration**

1. Navigate to the Settings page using the burger menu.\
   ![](https://lh3.googleusercontent.com/V6iTLYYMsOhUW7E2qCDU-KVRLY9GGZesruWPTUvyj2IC5FTWpyHMVKt0zcmN7LVPPa26BEkO7A-1A-15Fy9E8AGxj3UD4-H3J4x3i9Fk\_fi2n6yJen2xXyGt-OMjjqivOKYEQsIEsy-4SFlVxg)
2. Scroll down to the “External Systems Synchronizations” section and click on the ‘+’ button to open the Registration modal.\
   ![](https://lh3.googleusercontent.com/mMZQM8NaOW9vOYbkThyI869Y8qy6Rs948cRAtxEeVQmOLAZ33CMvyDsgYVL0a4dSZW95jjo9SYXGRnIqcs4V7qP3jYg\_TZ3FwiVNYs6VATy4h3IbFeT5mzW3wSECJBXm5xadKsocyyQ8l6Ldiw)
3. Select the type of synchronization you want to initiate from the Type dropdown and fill out the fields (DHIS2, Reveal or FHIR) .\
   ![](https://lh5.googleusercontent.com/640rwQ9zze0TndBd7C3Vm3ym1JZiKuSnhGjX0HEMQc9nrdjA6OFbqeZAxhk4RwDoxnUr4Ag682Nfa8Z8YVS67Tgoib948nRDaAswMhO2S9RIFZdlwei6ypN7lvS6VF\_nhHzLVglsowiCJI-EYA)

| Field Name   | Description                                                                                                                 | Required |
| ------------ | --------------------------------------------------------------------------------------------------------------------------- | -------- |
| Type         | The type of external system.                                                                                                | Yes      |
| Organization | The organization the user belongs to. An external system will only be available to data and users within this organization. | Yes      |
| ID           | The identifier for this external system.                                                                                    | Yes      |
| Label        | The label of the external system.                                                                                           | Yes      |
| Description  | A description of the external system.                                                                                       | No       |
| Username     | The username of the user from the DHIS2 instance to be used for authentication.                                             | Yes      |
| Password     | The password of the user from the DHIS2 instance to be used for authentication.                                             | Yes      |
| URL          | The URL of the DHIS2 instance.                                                                                              | Yes      |
| Version      | The version of the DHIS2 instance.                                                                                          | Yes      |

**Import**

If Geo-Object data is already present as organization units in a DHIS2 instance, it must first be imported using the ‘Import from an external system’ option in the Import module.

**Synchronization**

The GPR supports using an external system synchronization to push data to a DHIS2 instance. The purpose of the external system synchronization is to define how Geo-Object Types in a specific hierarchy will map to organization units in a DHIS2 instance. The latest version of the Geo-Objects will be synchronized with DHIS2, as the GPR currently does not support exporting at a specific date.

1. Navigate to the Settings page.\
   \
   ![](https://lh3.googleusercontent.com/V6iTLYYMsOhUW7E2qCDU-KVRLY9GGZesruWPTUvyj2IC5FTWpyHMVKt0zcmN7LVPPa26BEkO7A-1A-15Fy9E8AGxj3UD4-H3J4x3i9Fk\_fi2n6yJen2xXyGt-OMjjqivOKYEQsIEsy-4SFlVxg)
2. Find the External System Synchronizations section and click on the Register Synchronization button.\
   ![](https://lh4.googleusercontent.com/U2PvsRhRx3JpICTHaSg\_gp0ikPStMK65N8LI5geBxiE-uu6nVbtOjvRSPYIxuNLcgO4KoGZctazpYIOOi8aV5T8vSKrsm9kr47KLX09hAMU39Qa-vffmWmQgEb7hO2Y7D2pWT70JT8kh02hBEQ)
3. Click the Create button on the Synchronization Configurations page.\
   ![](https://lh6.googleusercontent.com/cnxDqD8oHLHZN8orbex55i1Ls63XHGwQVPHSvYNR04hGhPX0tkWL4oAdgvaSa3b\_fgBfqqdR2r9qjMi9qUWaIt1FKigCcD8Y-nL8Efw3-YwWU7vuY0d9\_Bpl1Y51c-cbOzNcYsC61OgHFKbgcA)
4. Fill out the fields in the Synchronization Configuration modal and click Submit.\
   ![](https://lh5.googleusercontent.com/h9rpNFq1dfzeih5quAu9D9Ee-OyIMHiYVxcCFMdU4gDG25Y9YR8fUtQ1XxPpkpbq5VrieH4QkmA3yuZAXXYVUntyFqmj83XwACf9wXMuYPusuoJ0mbgM-vAgKJeeqOYySWm09-id9bEkSdgQ2w)

| Field Name      | Description                                                                                               |
| --------------- | --------------------------------------------------------------------------------------------------------- |
| Label           | Label of the synchronization configuration.                                                               |
| Organization    | The organization the synchronization configuration will be available to.                                  |
| Hierarchy       | The hierarchy this synchronization will use to push data to an external system.                           |
| External System | The registered external system that this synchronization will use to push data to an external system.     |
| Org Units       | A mapping between the Geo-Object Types in the selected GPR hierarchy and the types in the DHIS2 instance. |

**Matching organization units**

The Org Units section of the configuration dialog allows you to map each Organization Unit Level in DHIS2 to a Geo-Object Type in the GPR. There is no limit to the amount of levels that can be matched, however no more levels should be matched than exist in the DHIS2 instance being synchronized with. Additionally, the matched Geo-Object Type of each level should be a direct child of the level before it.

The Geo-Objects in the GPR are matched to their DHIS2 counterparts using the external identifiers of the GPR Geo-Object and the identifiers of the Organization Unit in DHIS2. It is important to note that this matching does not use the Code properties from either system. If a Geo-Object does not have an external identifier, then it will be considered new and will be created in DHIS2 if the synchronization type is set to ‘Org Units and Relationships’. The GPR will then save the external identifier of that new Organization Unit in the database to be used for future updates. If the Geo-Object has an external identifier while DHIS2 does not have an organization unit with a matching identifier in their system, an error will be thrown.

The DHIS2 Synchronization Type specifies what data will be synchronized to DHIS2.

|                             |                                                                                                                                                                                                                                                                                                                                                                                                  |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Org Units                   | Synchronizes attributes from Geo-Objects over to existing Organization Units in DHIS2. New Geo-Objects cannot be synchronized with this setting.                                                                                                                                                                                                                                                 |
| Relationships               | Synchronizes relationships between Geo-Objects with DHIS2. If an Organization Unit in DHIS2 has a different parent than what exists in the GPR, the existing parent will be set to the one in the GPR. If multiple parents in the GPR are detected for a Geo-Object an error will be thrown and the relationship will not be exported. New Geo-Objects cannot be synchronized with this setting. |
| Org Units and Relationships | Synchronizes both attributes and relationships over to DHIS2. If the Organization Unit does not exist in DHIS2 it will be created.                                                                                                                                                                                                                                                               |

**Matching organization unit groups**

Geo-Object Types (levels) can be matched to an organization unit group, so that only select organization units within that group are synchronized. The ‘Org Unit Group’ dropdown lists all organization unit groups which currently exist in the DHIS2 instance. When a Geo-Object Type is matched to a group, all Geo-Objects that are of that Geo-Object Type will be assigned to the selected organization unit group the next time the system synchronizes with this configuration.

This behavior operates in an additive fashion only. Any organization units which are already assigned to the organization unit group will not be affected.

**Custom attribute matching**

If a Geo-Object Type is matched which contains custom attributes, the custom attribute matcher will be displayed.\
![](https://lh4.googleusercontent.com/OniYJAgD99nao2Za-lJPicx9FQRoApid2gPfpJ1Og48Pav8jkT-wBTMLChI0gdV2wOkpPtjMENTAIYnV3h4Yw5KbPBhpAeVRBuINyoE-kfW3yZjFM1X\_\_FgYAp1QJR8Wkw1vvvuTniP9OjJp0g)

This attribute matching is specific to a Geo-Object Type and level. In order for a DHIS2 attribute to be a valid selection for the matching, it must be applied to organization units, and it must be close enough in Type to be a candidate. Here are the appropriate selection types:

| GPR Data Type | Appropriate DHIS2 Value Types                               |
| ------------- | ----------------------------------------------------------- |
| Text          | Text, Long Text, Letter, Phone Number, Email, Username, URL |
| Boolean       | Boolean, True Only                                          |
| Date          | Date, Date Time, Time, Age                                  |
| Integer       | Integer, Integer Positive, Integer Negative, Integer Zero   |
| Decimal       | Number, Unit Interval, Percentage                           |
| Term          | Option Set                                                  |

GPR data type Appropriate DHIS2 value types Text Text, Long Text, Letter, Phone Number, Email, Username, URL Boolean Boolean, True Only Date Date, Date Time, Time, Age Integer Integer, Integer Positive, Integer Negative, Integer Zero Decimal Number, Unit Interval, Percentage Term Option Set

The following DHIS2 value types cannot be mapped to attributes in the GPR:

* Tracker Associate&#x20;
* Coordinate&#x20;
* Organization Unit&#x20;
* File Resource&#x20;
* Image

If an attribute in the GPR is not matched to one in DHIS2 (either because there were no valid selections, or the dropdown was intentionally left as ‘not matched’), then the data in that attribute will not be synchronized with DHIS2. It will not, however, prevent the rest of the attributes or relationships from being synchronized.

**Term matching**

A. Option sets

GPR Term-type attributes can be matched to DHIS2 option sets. When the ‘Target Type’ is set to ‘Option Set’, the ‘Target Attribute’ dropdown will populate with all DHIS2 attributes which contain an option set and are assigned to organization units. When a GPR Term-type attribute is matched to a valid option set in the DHIS2, then the user interface expands to allow matching between GPR terms and DHIS2 options.\
![](https://lh6.googleusercontent.com/mdsCKs1md40j1YwVREsFgZMV0RwP-vIlfZmO9oFTTKvnufVUyLmLJNvgnoqhCHAf9nSjhCi2tYjwcDLRdDwRgMCsdRQDpzmtVcF3eguV027w\_KB9JHU-hofQ4dyuG9TcRr\_DMyFc2Is7o712EA)

If a Geo-Object does not have values for the Term-type attribute, then the attribute will not be set on the DHIS2 Organization Unit. Geo-Objects with terms which have not been matched (‘Not Mapped’) will not be exported and an error will be presented.

B. Organization unit groups

Terms can also be mapped instead to Organization Unit Groups. This can be done by selecting ‘Org Unit Group’ in the ‘Target Type’ dropdown.\
![](https://lh6.googleusercontent.com/njSf72eXu63RsBxUT0H\_QawOB-Sa6xsiaokwHIxCvmFMaapu0lByyKjea1gXUzIMMmm3jdxU46yIyVqJTC1Bp7\_aNi23hR4sZwwvQQ9G9hUlIT9EraLcmuj02dGBbmdFUnnjrz3yJKnbv0Qeuw)

Geo-Objects will be assigned to the Organization Unit Group as matched in the above screenshot. This provides some basic support for Org Unit Group synchronization.

Similar to option set matching, if a Geo-Object does not have a value for the Term-type attribute, then it will not be assigned to an Organization Unit Group. Geo-Objects with terms which have not been matched (‘Not Mapped’) will not be exported and an error will be presented.

This behavior operates in an additive fashion only. Any organization units which are already assigned to the organization unit Group will not be affected.

If a level is matched to a DHIS2 organization unit group, and the Geo-Object Type also contains a term which is matched to DHIS2 organization unit groups, then the synchronized organization unit will be added to all organization unit groups which have been matched (in an additive fashion). Import DHIS2 to CGR plugin

#### 4.3.2 Reveal Registration Import

#### 4.3.3 FHIR
