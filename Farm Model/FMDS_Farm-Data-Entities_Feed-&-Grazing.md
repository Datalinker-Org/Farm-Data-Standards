### Feed & Grazing

Contents:
* [Grazing for young Dairy Replacements on the milking area](#Grazing-for-young-Dairy-Replacements-on-the-milking-area)
* [Grazing for dry cows](#Grazing-for-dry-cows)
* [Grazing and feed activities for sheep, beef cattle, deer, and goats](#Grazing-and-feed-activities-for-sheep,-beef-cattle,-deer,-and-goats)
* [Crops grazed and feed harvested](#Crops-grazed-and-feed-harvested)
* [Imported supplements fed out on effective area during season](#Imported-supplements-fed-out-on-effective-area-during-season)

The following table defines items in entities that summarise feed and grazing.  See the Farm Features and Attributes Data Standard for a [list of plot activity values](https://github.com/Datalinker-Org/Farm-Data-Standards/blob/master/Farm%20Features%20and%20Attributes/FFADS_Enumeration-Lists.md#Plot-Activity-Value-Enumeration-List) for crops and grazing.

#### Grazing for young Dairy Replacements on the milking area

Attributes | Data Types | Notes
:--------- | :--------- | :----
Stock class | Enumeration | See [Stock Reconciliation Data Standard](https://github.com/Datalinker-Org/Farm-Data-Standards/blob/master/Stock%20Reconciliation/README.md).
Number animals | Integer
Age at start of grazing	| Float | Mean age at start of grazing, months.
Total months grazed	| Integer | Total months grazed on effective area.

#### Grazing for dry cows

Attributes | Data Types | Notes
:--------- | :--------- | :----
Number cows	| Integer | Number of cows grazed off from 1st June including in-calf heifers.
Days grazed away | Integer | Total days grazed away from milking area.
Date left milking area	| [ISO Date](FMDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) |
Grazed away location | Enumeration | Owned run-off, Leased run-off, Grazier (from Overseer).
Feed offered | Integer | Grass and supplement offered, kgDM/cow/day.
Digestibility | Integer | %
Metabolisable energy | Float | Average metabolisable energy of all feeds including supplements, MJME/kgDM.
Utilisation % | Integer | Utilisation of feed offered, %

#### Grazing and feed activities for sheep, beef cattle, deer, and goats	

Attributes | Data Types | Notes
:--------- | :--------- | :----
Species Simple Name | Enumeration | Cattle, Deer, Goats, Sheep see Animal Data Standard
Stock class	| Enumeration | See [Stock Reconciliation Data Standard](https://github.com/Datalinker-Org/Farm-Data-Standards/blob/master/Stock%20Reconciliation/README.md).
Number of Stock | Integer | 
Cost of Feed | Integer | $
Feed eaten | Integer | kg DM
Feed grown | Integer | Tonnes
Feed sold | Integer | Tonnes
Date on-farm | [ISO Date](FMDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) |
Date off-farm | [ISO Date](FMDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) |
Age	| Integer | Age of animals at arrival, months.

#### Crops grazed and feed harvested	

Attributes | Data Types | Notes
:--------- | :--------- | :----
Area hay & silage | Float | Area harvested for hay and silage, expressed in m<sup>2</sup> (SI unit) or hectares (ha, accepted non-SI unit). Implementations must clearly specify which unit is used, and  ensure consistent use . For spatial data interchange m<sup>2</sup> should be used. 
Crop fate | Enumeration | Grazed in paddock, Cut and carry, Exported off-farm, Carried over to next season.
Area harvested crop | Float | Area of harvested crop, including cereal and maize, expressed in m<sup>2</sup> (SI unit) or hectares (ha, accepted non-SI unit). Implementations must clearly specify which unit is used, and  ensure consistent use . For spatial data interchange m<sup>2</sup> should be used<sup id="INSPIRE">[1](#f1)</sup>.
Feed exported | Float | Feed grown on milking platform and exported, t DM.
Area summer crop grazed	| Float | Area of summer crop grazed on effective area, expressed in m<sup>2</sup> (SI unit) or hectares (ha, accepted non-SI unit). Implementations must clearly specify which unit is used, and  ensure consistent use . For spatial data interchange m<sup>2</sup> should be used<sup id="INSPIRE2">[1](#f1)</sup>.
Area winter crop grazed	| Float | Area of winter crop grazed on effective area, expressed in m<sup>2</sup> (SI unit) or hectares (ha, accepted non-SI unit). Implementations must clearly specify which unit is used, and  ensure consistent use . For spatial data interchange m<sup>2</sup> should be used<sup id="INSPIRE3">[1](#f1)</sup>. 
Type of feed grown | Enumeration | 
Destination of feed | Enumeration | Non-effluent block, effluent block, feed pad, etc.
Method of feeding |  | 
Cropping activity month | Enumeration | Month when activity occurred.
Cropping activity | Enumeration | Minimum till, conventional cultivation, direct drilled, sowing, harvesting, grazing (list from Overseer).
Month first cultivated | [ISO 8601 Date](FMDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) | Year/Month
Effluent applied | Boolean | 
Irrigation applied | Boolean | 
Month re-sown | Enumeration |
Hours grazed per day | Integer |  hrs/day
Month first grazed | Enumeration | 
Month last grazed | Enumeration | 
Cut and carry destination | String | Location fed if cut and carry.

#### Imported supplements fed out on effective area during season	

Attributes | Data Types | Notes
:--------- | :--------- | :----
Type of feed | Enumeration | List of feed types from Animal Data Standards B.8.
Wet matter | Float | Tonnes.
DM % | Integer | %
Dry matter | Float | tonnes
Metabolisable energy | Float | Average metabolisable energy, MJME/kgDM
Utilisation % | Integer | Utilisation of feed offered, %
Destination of feed | Enumeration | Non-effluent block, effluent block, feed pad.
Method of feeding | String |     

#### Footnotes

<b id="f1">1.</b> See section 6.1.3 of D2.8.I.2 Data Specification on Administrative Units – [Technical Guidelines](https://inspire.ec.europa.eu/id/document/tg/au). [↩](#INSPIRE) [↩](#INSPIRE2) [↩](#INSPIRE3)
