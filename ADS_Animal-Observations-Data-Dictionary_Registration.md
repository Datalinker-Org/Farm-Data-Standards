### Registration Observations

Contents:
* [Register Identification](#Register-Identification)
* [Change Identification](#Change-Identification)
* [Change Fate](#Change-Fate)
* [Change Herd Membership](#Change-Herd-Membership)
* [Change Ownership](#Change-Ownership)
* [Change Location](#Change-Location)


#### Register Identification

Also called “Tagging”; the act of applying an official tag. Applies to individual animals. 

Attribute | Data Type | Notes 
:-------- | :-------- | :----
Tag Type | Enumeration | See [Animal Tag Types](#Animal-Tag-Types).
ICAR Product Code | Integer | [Product code](https://www.service-icar.com/tables/Tabella3.php) from [ICAR](docs/ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations).
Animal Identifier | [URN](docs/ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) | An animal identifier as specified in [Animal Identification](#Animal-Identification) using a registered namespace.
Removing Tag | Boolean | True if the tag is being removed – the default is False.

#### Change Identification

The act of replacing an official tag, also called “Retagging” and “Replacement”. Applies to individual animals.	

Attribute | Data Type | Notes 
:-------- | :-------- | :----
Tag Type | Enumeration | See [Animal Tag Types](#Animal-Tag-Types).
Previous Animal Identifier | [URN](docs/ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) | Where known, the previous URN of the animal. 
ICAR Product Code | Integer | [Product code](https://www.service-icar.com/tables/Tabella3.php) from [ICAR](docs/ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations).
Animal Identifier | [URN](docs/ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) | The new [URN](docs/ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) of the animal.
Retagging Reason | String | A textual explanation.


#### Change Fate

Records that the animal Fate (or Status) has changed. This typically occurs when an animal dies or leaves the herd.	

Attribute | Data Type | Notes 
:-------- | :-------- | :----
Fate Code | Enumeration | See [Animal Fate Values](#Animal-Fate-Values).
Fate Reason | Enumeration | See [Animal Fate Reasons](#Animal-Fate-Reasons).
Disposal Waybill | String | Waybill or disposal identifier.
Disposal Method | Enumeration | See [Animal Disposal Methods](#Animal-Disposal-Methods).

#### Change Herd Membership

The act of changing from one “herd” (including flock), or other official recording group to another. May comprise part of a movement. Applies to individuals or a group. Also called sale, purchase, transfer.	

Attribute | Data Type | Notes 
:-------- | :-------- | :----
Source Herd Identifier | [URN](docs/ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) string | Herd identifier.
Source Herd Display Name | String | Display name.
Destination Herd Identifier | [URN](docs/ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) string | Herd identifier.
Destination Herd Display Name | String | Display name.

#### Change Ownership

Records a change of ownership of an animal, group, or herd.
Often (but not always) associated with a movement between locations. This may also include a Lease (a change of ownership arrangements). Also called sale, purchase, transfer.

Attribute | Data Type | Notes 
:-------- | :-------- | :----
Previous Owner Identifier | URN string | Owner identifier.
Previous Owner Display | Name String | Display name.
New Owner Identifier | URN string | Owner identifier.
Previous Lessee Identifier | URN string | Owner identifier.
Previous Lessee Display Name | String | Display name.
New Lessee Identifier | URN string | Owner identifier.
New Lessee Display Name | String | Display name.
Tally | Integer | Count of animals involved.

#### Change Location

A movement from one official location to another. We have called this “Change Location” rather than Movement to avoid confusion with moves within a location (for instance, between paddocks). Also called movement, transfer, grazing, sale, or purchase. Recorded for individuals for cattle and deer because of [NAIT](docs/ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) requirements.

Attribute | Data Type | Notes 
:-------- | :-------- | :----
Source Location Identifier | [URN](docs/ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) string | Location identifier.
Source Location Display Name | String | Display name.
Destination Location Identifier | [URN](docs/ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) string | Location identifier.
Destination Location Display Name | String | Display name.
Transport Method | Enumeration | See [Transport Methods](#Transport-Methods).
Transport Operator | String | Operator name.
Waybill | String | Waybill or transaction ID.
Vehicle Identification | String | Fleet number or licence plate.
Transit Time | [ISO(docs/ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) 8601  | Period (duration).
Tally | Integer | Count of animals involved.

##### Animal Tag Types

Animal Tag Type is used in the Register Identification and Change Identification observations in the Registration category.

Valid values for Tag Type|
:------------------------|
Ear Tag|
Inject|
Bolus|
Tag Attachment|

Note that Tag is a synonym for Ear Tag.

##### Animal Fate Values

Animal Fate is specified in both the Change Fate observation (in Registration) and for progeny in the Parturition observation (in Reproduction).  Some codes are specific to one of these observations.  The relevant context for each code is given below.  

Valid values for Fate Code are:

Fate Value | Used in observation(s):
:--------- | :----------------------
Alive | Change Fate.
Culled | Change Fate; Parturition.
Dead | Change Fate; Parturition.
Grazing Off | Change Fate.
Grazing On | Change Fate.
