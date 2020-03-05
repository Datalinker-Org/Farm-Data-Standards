### Hazard Data Dictionary

Contents:
* [Hazard Identification](#Hazard-Identification)
  * [Hazard Control](#Hazard-Control)
* [Hazard Types – Additional Attributes](#Hazard-Types-–-Additional-Attributes)
  * [Hazardous Substances Location](#Hazardous-Substances-Location)
  * [AgriBuilding/Installation](AgriBuilding/Installation)

#### Hazard Identification

A Hazard Name [SHALL](HSDS_Definitions-and-Abbreviations_Interpretation.md#Interpretation) be recorded if the hazard is not already recorded as a Feature with spatial attributes as defined in [Spatial Attributes](HSDS_Identification-of-Observations.md#Spatial-Attributes). If the Hazard already exists as a Feature, then Hazard Name [MAY](HSDS_Definitions-and-Abbreviations_Interpretation.md#Interpretation) be ignored for that Feature.

##### Hazard Identification 

Attributes | Data Types | Notes
:--------- | :--------- | :----
Feature Identifier | String | Identifier used to identify the feature.
Feature Name | String | Name used to identify the feature.
Hazard Name | String | Name or identifier of the hazard. (NOT required if Feature ID and/or Feature Name are used to identify the Hazard).
Hazard Type | Enumeration | Activity, AgriBuilding/Installation, Biological, Climatic/Natural, Environmental, Equipment, Hazardous Substance,  Vehicle.
Hazard Location | String | Description of location of the hazard (NOT required if geographic coordinates are used to identify the Hazard).
Hazard Description | String | Describe the hazard .
Hazard From	| ISO Date | All Hazards [MUST](HSDS_Definitions-and-Abbreviations_Interpretation.md#Interpretation) have a Hazard From Date.
Hazard To | ISO Date | Temporal Hazards [MAY](HSDS_Definitions-and-Abbreviations_Interpretation.md#Interpretation) have a Hazard To date which defines when the feature is no longer deemed to be hazardous.
Hazardous Period | String | Describes a temporal period in which this hazard exists: e.g. it may be seasonal, or exist only at certain times of the day.
Hazard Exposure Consequence	| Enumeration | Describes the result of contact with or exposure to the hazard. Enumeration: Minimal, Low, Serious, Very Serious, Catastrophic.
Potential Harm | String | Description of the potential harm the hazard poses and what/whom it may affect, e.g. Burn risk.

##### Hazard Control	

Attributes | Data Types | Notes
:--------- | :--------- | :----
Hazard Management | Enumeration | Eliminate, Minimize.
Training Required | String | Description of the training required for staff / visitors to mitigate risk.
PPE Required | String | Description of the Personal Protection Equipment required to mitigate risk .
Process Control | String | Description of the process to be followed to mitigate risk.
Other Control | String | Description of the controls or actions in place to mitigate risk.

#### Hazard Types – Additional Attributes
Some hazard types typically have a range of additional attributes beyond those captured in the [Hazard Identification](#Hazard-Identification). 

##### Hazardous Substances Location
Any hazardous substances within the [HSNO](HSDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) classification. 

Attributes/Codes | Data Types | Notes
:--------------- | :--------- | :----
Storage Type | Enumeration |  Shed, Tank, Drum, Container, Silo, Bin, Other
Quantity | Float | Expressed in kg’s.
Class | Enumeration |  Class code, e.g. 3.1A. (See EPA [HSNO](HSDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) Hazardous Goods Classification codes for complete list).
Location Test Certificate | String
Location Test Certificate Date | [ISO Date](HSDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations)
Stationary Container System Test Certificate | String
Stationary Test Certificate Date | [ISO Date](HSDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations)
Person in Charge | String | Person ID
Approved Handler | String | Person ID
Approved Handler Job Title | String
Approved Handler Contact Details | String
Other Environment Hazard | String | Description of other environmental hazard type.

##### AgriBuilding/Installation

Terms used to describe farm structures and activity facilities by INSPIRE and adopted by the Farm Features and Attributes Data Standard. D2.8.III.9 INSPIRE Data Specification on Agricultural and Aquaculture Facilities – [Technical Guidelines](http://inspire.ec.europa.eu/documents/Data_Specifications/INSPIRE_DataSpecification_AF_v3.0.pdf)
	
Attributes/Codes | Data Types | Notes
:--------------- | :--------- | :----
AgriBuilding Type | | Refer to [Type of AgriBuilding Value](https://github.com/Datalinker-Org/Farm-Data-Standards/blob/master/Farm%20Features%20and%20Attributes/FFADS_Enumeration-Lists.md#Type-of-AgriBuilding-Value) in the Farm Features and Attributes Data Standard.
