### Management Blocks

Contents:
* [Management block identification and location information](#Management-block-identification-and-location-information)
* [Pastoral Block details](#Pastoral-Block-details)
* [Support block details](#Support-block-details)

The spatial blocks that a farmer uses to manage the land may be different to those defined by land titles, soil, or climate zones. In New Zealand, we use the term “Management Block” to define blocks that are managed differently. Typically, these differ in irrigation or effluent application, fertilisers applied, and types and numbers of stock grazed. The following table defines items in entities that apply to each management block.  These are also known as Sites by INSPIRE, and this is a synonymous term used in the Farm Features and Attributes Data Standard. 

#### Management block identification and location information

Attributes | Data Types | Notes
:--------- | :--------- | :----
Runoff | Boolean | True if runoff block
Block Total Area | Float | Block total area expressed in m<sup>2</sup> (SI unit) or hectares (ha, accepted non-SI unit). Implementations must clearly specify which unit is used, and ensure consistent use. For spatial data interchange m<sup>2</sup> should be used.  
Block Effective Area | Float | Effective area  of the farm taking into account slope. Valid units for expressing  area in m<sup>2</sup> (SI unit) or hectares (ha, accepted non-SI unit). Implementations must clearly specify which unit is used, and ensure consistent use. For spatial data interchange m<sup>2</sup> should be used<sup id="INSPIRE">[1](#f1)</sup>.
Block Grazeable Area | Float |  Area of the farm for grazing purposes. Valid units for expressing area are m<sup>2</sup> (SI unit) or hectares (ha, accepted non-SI unit). Implementations must clearly specify which unit is used, and ensure consistent use. For spatial data interchange m<sup>2</sup> should be used<sup id="INSPIRE2">[1](#f1)</sup>.  
Block Cultivable Area | Float | Area of the farm for cultivation (cropping) purposes. Valid units for expressing area are m<sup>2</sup> (SI unit) or hectares (ha, accepted non-SI unit). Implementations must clearly specify which unit is used, and ensure consistent use. For spatial data interchange m<sup>2</sup> should be used<sup id="INSPIRE3">[1](#f1)</sup>.  
Block ownership | Enumeration | Owned, Leased
Topography | Enumeration | Flat, Rolling, Easy hill, Steep hill (this enumeration is defined by Overseer).
Distance from coast | Integer | kilometres
Pasture type | Enumeration | Ryegrass/white clover, Browntop, Unimproved/tussock grasslands, Summer C4 (paspalum) pastures, C4 (kikuyu) pastures, Lucerne, Grass only (enumeration defined by Overseer).
Pasture Species | Array | Plant species names as defined in Feedipedia forage plants.
Clover level | Enumeration | Annual average clover content (as a proportion of pasture dry matter) where fertiliser N inputs are not applied. Enumeration defined by Overseer. <br> Enumeration: Very low, Low, Medium, High, Very high.
Pasture utilisation	| Integer: | %

#### Pastoral Block details

Attributes | Data Types | Notes
:--------- | :--------- | :----
Average pasture N concentration	| Integer: | %
Support block owned | Enumeration | Owned, Leased.
Support block address | String
Stock type on support block | Enumeration | Dairy Cows [Cows], Dairy Replacements [Young Stock], Pigs, Sheep, Beef Cattle [Cattle], Deer.

#### Support block details

Attributes | Data Types | Notes
:--------- | :--------- | :----
Number of stock | Integer
Date stock come | [ISO Date](FMDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations)
Date stock leave | [ISO Date](FMDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations)
Area hay/silage harvested | Integer | Area expressed in m<sup>2</sup> (SI unit) or hectares (ha, accepted non-SI unit). Implementations must clearly specify which unit is used, and ensure consistent use. For spatial data interchange m<sup>2</sup> should be used. 
Destination hay/silage | Enumeration | Fed on support block, Milking area, Elsewhere (defined by Overseer).

#### Footnotes

<b id="f1">1.</b> See section 6.1.3 of D2.8.I.2 Data Specification on Administrative Units – [Technical Guidelines](https://inspire.ec.europa.eu/id/document/tg/au). [↩](#INSPIRE) [↩](#INSPIRE2) [↩](#INSPIRE3)
