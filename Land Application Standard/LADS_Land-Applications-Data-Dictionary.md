### Land Applications Data Dictionary (Normative)

Contents:
* [Application Information](#Application-Information)
  * [Order or Job Details](#Order-or-Job-Details)
  * [Spreading Information](#Spreading-Information)
* [Product Information](#Product-Information)
  * [Product Details](#Product-Details)
  * [Nutrient Concentrations](#Nutrient-Concentrations)
* [Spread Representations](#Spread-Representations)
  * [Ecological Hot-spot](#Ecological-Hot-spot)
  * [Feature attributes](#Feature-attributes)

#### Application Information

The following table defines items categorised as Application information. These attributes relate to an application that has been created.

##### Order or Job Details

Attributes | Data Types | Notes
:--------- | :--------- | :----
Application ID | String | identifies the application or job being processed (within system or interchange scope).
Application Name | String | Name of the application.
Block Name | String | Name of the block the application is to be applied to.
Order Date | [ISO 8601](LADS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) | Date. 
Customer Name | String | The name of the customer the application is being processed for.
Planned Start Date | [ISO 8601](LADS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) | Date and time: planned start date of execution of the job. 
Planned Completion Date | [ISO 8601](LADS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) | Date and time: planned completion date of execution of the job.
Date Started | [ISO 8601](LADS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) | Date and time: actual date the job was started.
Date Completed | [ISO 8601](LADS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) | Date and time: actual date the job was completed.

##### Spreading Information

Attributes | Data Types | Notes
:--------- | :--------- | :----
Area Requested  | Float | Total area for which application is to be applied to; in m<sup>2</sup> (SI unit) or hectares (ha, accepted non-SI unit). Implementations must clearly specify which unit is used, and ensure consistent use. For spatial data interchange m<sup>2</sup> should be used<sup id="INSPIRE">[1](#f1)</sup>. 
Area Nominal | Float | Area exposed to the application in m<sup>2</sup> (SI unit) or hectares (ha, accepted non-SI unit). Implementations must clearly specify which unit is used, and ensure consistent use. For spatial data interchange m<sup>2</sup> should be used<sup id="INSPIRE2">[1](#f1)</sup>.
Area Spread | Area Spread Floating | Actual area applied in m<sup>2</sup> (SI unit) or hectares (ha, accepted non-SI unit). Implementations must clearly specify which unit is used, and ensure consistent use. For spatial data interchange m<sup>2</sup> should be used<sup id="INSPIRE3">[1](#f1)</sup>. 
Distance Working | Integer | Total distance that was covered while spreading; metres
Distance Not Working | Floating | Distance that was captured when the vehicle was not spreading (e.g. access track to paddock); metres.
Buffer to neighbouring areas | Float | Distances to neighbouring paddocks or ecosystems that have to be respected as sensitive or no-go areas; metres.
Operator ID | String | Identifier to represent the operator (defined within system or interchange scope).
Operator Name | String | Operator planned to complete the job.
Equipment ID | String | Identifies the equipment planned or used to complete the job (defined within system or interchange scope).
Equipment Name | String | description of the equipment planned or used.
Rate Method	| Enumeration | Fixed rate, variable rate.
Application Rate | Float | Effective application rate in [Units] per hectare (e.g. kg/ha); kg or litres per hectare.
Dressing Name | String | Name of the dressing (a single application may contain multiple dressings).

#### Product Information

The following table defines items categorised as product information. One job may have multiple products (i.e., a mix) or a single product (which may itself be a mix or a normal stock unit).

##### Product Details	

Attributes | Data Types | Notes
:--------- | :--------- | :----
Product Category | Enumeration | See [Product Category](LADS_Lists-of-Valid-Values.md#Product-Category).
Product Code | String | An identifier for the product (within the application scope), for example an inventory stock keeping unit ([SKU](LADS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations)).
Product Name | String | A display or common name of the product.
Application Rate Units | Enumeration | (per hectare); kg, litres, pounds.
Spread Rate | Float | [Application Rate Units] per hectare.
Total quantity | Float | Total quantity of product that is planned to be applied; [Units].
Mix % | Float | % of the product in the mix for the job; %.

##### Nutrient Concentrations	

Attributes | Data Types | Notes
:--------- | :--------- | :----
Nutrient | Enumeration | Standardised short name of a nutrient; see [Nutrients](LADS_Lists-of-Valid-Values.md#Nutrients).
Concentration | Float | Concentration within the product as spread; %

#### Spread Representations

The following tables defines items categorised as spread representations, which are used to define spatial representations of features. A job [SHALL](LADS_Definitions-and-Abbreviations_Interpretation.md#Interpretation) have at least one spatial representation, which [MAY](LADS_Definitions-and-Abbreviations_Interpretation.md#Interpretation) utilise one or more formats, and [MAY](LADS_Definitions-and-Abbreviations_Interpretation.md#Interpretation) be included with the other job data or referenced as a separate internet resource, and [MAY](LADS_Definitions-and-Abbreviations_Interpretation.md#Interpretation) represent one of several job features. See [Spatial Attributes](LADS_Components_of_an_Observation.md#Spatial-Attributes) for accepted Spatial Attributes.

##### Spread Representation	

Attributes | Data Types | Notes
:--------- | :--------- | :----
Data Format | Enumeration | Format of the data; e.g. KML, SHP, KMZ, WKT
URL | URI string | Online [URL](LADS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) to access this data or relative reference to a file attachment included with the job message.
Zone Category | Enumeration | Soil quality, yield potential.
Number of Zones | Integer |
Representation ID | String | Optional identifier for this spatial representation of an ecological hot-spot.
Hot-spot Type | Enumeration | Plant, Insect, Fish, Bird.

##### Ecological Hot-spot 

Attributes | Data Types | Notes
:--------- | :--------- | :----
Representation | Integer | Number of Hot-spots
Hot-Spot Size | Floating | Area of the hotspot identified in m<sup>2</sup> (SI unit) or hectares (ha, accepted non-SI unit). Implementations must clearly specify which unit is used, and ensure consistent use. For spatial data interchange m<sup>2</sup> should be used. 

The following table defines items we have categorised as feature attributes. These [MAY](LADS_Definitions-and-Abbreviations_Interpretation.md#Interpretation) be associated with features within a spatial representation (for example: feature attributes in a KML file, or columns in the DBF file that accompanies an ESRI Shape file.

##### Feature attributes	

Attributes | Data Types | Notes
:--------- | :--------- | :----
Vehicle Speed | Float | metres per second.
Release Rate | Float | Product release rate; kg or litres per second.
Spread Width | Float | Width of the boom or throw distance; metres.
Application Rate | Float | Effective application rate at this feature in [Units] per hectare; kg or litres per hectare.
 
#### Footnotes

<b id="f1">1</b> See section 6.1.3 of D2.8.I.2 Data Specification on Administrative Units – [Technical Guidelines](https://inspire.ec.europa.eu/id/document/tg/au). [↩](#INSPIRE)

