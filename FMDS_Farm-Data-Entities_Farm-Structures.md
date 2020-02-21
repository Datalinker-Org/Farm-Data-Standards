### Farm Structures

Contents:
* [Identification of each structure](#Identification-of-each-structure)
* [Details of dairy shed](#Details-of-dairy-shed)
* [Description and usage of feed pads, stand-offs, and housing](#Description-and-usage-of-feed-pads,-stand-offs,-and-housing)
* [Details of Effluent System](#Details-of-Effluent-System)

The following tables define attributes applying to common farm structures, and for which there is an existing data interchange purpose (E.g. DairyBase benchmarking or Overseer models).  See the Farm Features and Attributes Data Standard for a [list of attributes relating to AgriBuildings](docs/FFADS_Enumeration-Lists.md). 

#### Identification of each structure

Attributes | Data Types | Notes
:--------- | :--------- | :----
Structure type | Enumeration | Dairy shed, Feed pad, Stand-off or loafing pad, Uncovered wintering pad, Covered wintering pad, Yards, Woolshed, Loading facility, Equipment shed, House, Calf rearing shed
Structure stock type | Enumeration | Dairy cow, Dairy cow replacements, Dairy grazing, Beef, Deer, Dairy goats (enumeration from Overseer)

#### Details of dairy shed 

Attributes | Data Types | Notes
:--------- | :--------- | :----
Dairy shed type | Enumeration | Herringbone, Rotary, Other 
Sets of cups | Integer

#### Description and usage of feed pads, stand-offs, and housing

Attributes | Data Types | Notes
:--------- | :--------- | :----
Structure Name | String
No. days facility used | Integer | Number of days facility is used by month.
No. cows using facility | Integer | Number of cows using facility each month.
Daily usage	| Integer | Hours facility user per day each month.
Surface of facility	| Enumeration | Lime or rock mix, Sawdust or peelings, Concrete, Other.
Limited grazing	| Boolean | Is limited grazing used (3-6 hours per day)?
Effluent removal | Enumeration | Scraped, Hosed.

#### Details of Effluent System

Attributes | Data Types | Notes
:--------- | :--------- | :----
Effluent disposal | Enumeration |  Irrigated to pasture, Discharge to water, Both.
Effluent spread location | Enumeration | effluent block, non-effluent block, exported off-farm.
Effluent spraying method | Enumeration | travelling irrigator, K-line system
Area land effluent applied | Integer | Area expressed in m<sup>2</sup> (SI unit) or hectares (ha, accepted non-SI unit). Implementations must clearly specify which unit is used, and ensure consistent use. For spatial data interchange m<sup>2</sup> should be used. 
Blocks solid applied | String | Blocks where the solid effluent is applied.
Number days storage	| Integer
Decision to irrigate | String: how is decision made?
Facility covered | Boolean
Liquid effluent collected | Boolean
Stored solids covered | Boolean
Period solids stored | Integer: time solids are stored, days
Effluent storage pond | Boolean
Solid effluent separated before pond | Boolean
Frequency pond solids removed | Float | Years.
Solid disposal location	| Enumeration | Effluent block, non-effluent block, exported off-farm.
Depth of application | Integer | Average depth of application, mm; by month, total.
