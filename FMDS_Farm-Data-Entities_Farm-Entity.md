### Farm Entity

Contents:
* [Farm identification and location](#Farm-identification-and-location).
* [Farm system overall description](Farm-system-overall-description).
* [Cadastral Parcel](#Cadastral-Parcel).

The following table defines items that apply to the overall farm. The farm system overall description is equivalent to a Holding as defined in the Farm Features and Attributes Data Standard. Note that sections which can be linked to spatial attributes will be headed as a feature, conforming to the Farm Features & Attributes Standard, whereas non-spatial items will be headed as Category.

#### Farm identification and location

Attributes | Data Types | Notes
:--------- | :--------- | :----
Country | ISO 3166 | Country code or name
Physical Address | | Physical Address specified using [schema.org/PostalAddress](https://schema.org/PostalAddress) or as a formatted address string in the local format of the relevant country.
Statistical Region | URN String | Defined in [Registration of Namespaces](docs/FMDS_Identification-of-Locations-and-Herds.md#Registration-of-Namespaces).
Territorial Local Authority	| String | The primary rating authority of the farm.
Regional Council | String | The primary resource management authority of the farm.
Catchment | String | A name of a catchment.
Total Area | Float | Total farm area expressed in m<sup>2</sup> (SI unit) or hectares (ha, accepted non-SI unit). Implementations must clearly specify which unit is used, and ensure consistent use. For spatial data interchange m<sup>2</sup> should be used[^INSPIRE/AU]. 
Cultivable Area | Float | Area of the farm for cultivation (cropping) purposes. Valid units for expressing area are m<sup>2</sup> (SI unit) or hectares (ha, accepted non-SI unit). Implementations must clearly specify which unit is used, and ensure consistent use. For spatial data interchange m<sup>2</sup> should be used[^INSPIRE/AU]. 

#### Farm system overall description

(This is synonymous with the Holding feature described in Farm Features & Attributes)	

Attributes | Data Types | Notes
:--------- | :--------- | :----
Grazeable Area | Float | Area of the farm for grazing purposes. Valid units for expressing area are m<sup>2</sup> (SI unit) or hectares (ha, accepted non-SI unit). Implementations must clearly specify which unit is used, and ensure consistent use. For spatial data interchange m<sup>2</sup> should be used[^INSPIRE/AU].  
Effective Area | Float | Effective area of the farm taking into account slope. Valid units for expressing area are m<sup>2</sup> (SI unit) or hectares (ha, accepted non-SI unit). Implementations must clearly specify which unit is used, and ensure consistent use. For spatial data interchange m<sup>2</sup> should be used[^INSPIRE/AU]. 
Principal Farm System | Enumeration | Australian and New Zealand Standard Industrial Classification (ANZSIC) class[^ANZSIC], Division A (Agriculture, Forestry and Fishing), Subdivision 01 (Agriculture).  Use of the International Standard Industrial Classification[^ISIC]  ISIC V4 Code may be appropriate for organisations considering international compatibility.
Primary activity | Enumeration | From list of ANZSIC Primary Activities for the Principal Farm System[^ANZSIC].
Farm System Sub-type | String | DairyNZ farm system number, B+LNZ farm class.
Irrigation used	| Enumeration |  Not irrigated, < 30% irrigated, > 30% irrigated.
Distance to furthest paddock | Float | Distance from dairy shed to furthest paddock (kilometres).
Proportion at different height | Integer | % farm at a different height/altitude to farm dairy.
Average height difference | Integer | Average difference in height between farm dairy and hill paddocks (metres).
Organic farm | Boolean | No, Yes
Title identifier | String | Land registration reference (Certificate of Title Number).
Legal Description | String

#### Cadastral Parcel

(See [Farm Features](docs/FFADS_Feature-Catalogue.md#Farm-Features) Farm Features and Attributes Data Standard for full definition)	   

Attributes | Data Types | Notes
:--------- | :--------- | :----
Title area | Float | Title area expressed in m<sup>2</sup> (SI unit) or hectares (ha, accepted non-SI unit). Implementations must clearly specify which unit is used, and ensure consistent use. For spatial data interchange m<sup>2</sup> should be used. (titles are often specified using square metres – divide by 10,000 to produce hectares). Equivalent to a [Cadastral](docs/FMDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) Parcel in the Farm Features and Attributes Data Standard.
Title purchase date | [ISO Date](docs/FMDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) | 
Rateable capital value | Currency |
Date of revaluation | [ISO Date](docs/FMDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations)
Revaluation district | String | Territorial Local Authority in which this title was revalued.
Area sold during year | Float | Area sold expressed in m<sup>2</sup> (SI unit) or hectares (ha, accepted non-SI unit). Implementations must clearly specify which unit is used, and ensure consistent use. For spatial data interchange m<sup>2</sup> should be used[^INSPIRE/AU]. 
Sale date | ISO Date
Opening market value | Currency | Estimated market value at start of year.
Closing market value | Currency | Estimated market value at end of year.
Valuation source | String

#### Footnotes

[^INSPIRE/AU]: See section 6.1.3 of D2.8.I.2 Data Specification on Administrative Units – [Technical Guidelines](https://inspire.ec.europa.eu/id/document/tg/au)
  
[^ANZSIC]: See the [ANZSIC classification](http://www.abs.gov.au/AUSSTATS/abs@.nsf/DetailsPage/1292.02006%20(Revision%202.0)?OpenDocument).

[^ISIC]: See the [ISIC registry](http://unstats.un.org/unsd/cr/registry/isic-4.asp) 
