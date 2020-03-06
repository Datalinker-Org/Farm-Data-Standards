### Pasture, Grazing and Feed Data Dictionary (Normative)

Contents:
* [Supplementary Feed Observations](#Supplementary-Feed-Observations)
  * [Harvest](#Harvest)
  * [Purchase](#Purchase)
  * [Store](#Store)
  * [Consume](#Consume)
  * [Sale](#Sale)
* [Grazing Observations](#Grazing-Observations)
  * [Grazing event](#Grazing-event)
  * [Grazing off](#Grazing-off)
  * [Grazing system](#Grazing-system)
* [Pasture Attributes](#Pasture-Attributes)
  * [Pasture Observations](#Pasture-Observations)
  * [Pasture](#Pasture)
  * [Pest monitoring](#Pest-monitoring)
  * [Weed Monitoring](#Weed-Monitoring)
* [Pasture and Feed Analysis Observations](#Pasture-and-Feed-Analysis-Observations)
  * [Feed characteristics](#Feed-characteristics)
  * [Feed minerals](#Feed-minerals)

#### Supplementary Feed Observations

Characteristics of the units referenced in the Supplementary Feed observations.

Attributes | Data Types | Notes
:--------- | :--------- | :----
Units | Enumeration | tonnes, tonnes [DM](PGFDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations), bales, big bales, m3, litres.
Unit wet weight | Float | kg per unit.
Unit dry weight | Float | kg per unit.
Unit volume | Enumeration | m3, litres.

The following table defines observations we have categorised as supplementary feed and relates to all supplementary feed on farm.

##### Harvest	
On-farm harvest of feed

Attributes | Data Types | Notes
:--------- | :--------- | :----
Crop Class | Enumeration | See [Crop Class](PGFDS_Lists-of-Valid-Values.md#Crop-Class).
Supplementary feed type harvested | Enumeration | See [Feed Type](PGFDS_Lists-of-Valid-Values.md#Feed-Type).
Paddock ID | String | Area ID on farm being harvested for supplementary feed.
Dry weight | Float | Total dry weight of a supplementary feed; tonnes of dry matter.
Harvest units | | See {Error! Reference source not found. above
Dry matter % | Float | %
Packaging type | Enumeration | Way a bale has been packaged; square, round, wrapped.

##### Purchase
Purchase of supplementary feed

Attributes | Data Types | Notes
:--------- | :--------- | :----
Supplementary feed type purchased | Enumeration | See [Feed Type](PGFDS_Lists-of-Valid-Values.md#Feed-Type).
Total supplementary feed purchased | Float | Amount of supplementary feed which has been bought.
Purchase units | | See {Error! Reference source not found. above
Dry matter % | Float | %
Supplementary feed cost | Integer | Cost of feed which has been bought; dollars ($), dollars/year ($/year).

##### Store
Storage of feed	

Attributes | Data Types | Notes
:--------- | :--------- | :----
Supplementary feed type stored | Enumeration | See [Feed Type](PGFDS_Lists-of-Valid-Values.md#Feed-Type).
Total supplementary feed stored | Integer | Amount of supplementary feed which is stored.
Change in inventory | Integer | Difference between total feed on hand at the start of the period, and feed on hand at the end of the period.
Storage units |  | See table above.
Storage condition | String | Conditions of the supplementary feed storage.
Structure type | Enumeration | Type of storage of feed supplement; See Farm Features & Attributes for full [Enumeration List](https://github.com/Datalinker-Org/Farm-Data-Standards/blob/master/Farm%20Features%20and%20Attributes/FFADS_Enumeration-Lists.md#Type-of-AgriBuilding-Value).

##### Consume	
Change in inventory from consumption and loss.

Attributes | Data Types | Notes
:--------- | :--------- | :----
Supplementary feed type consumed | Enumeration | See [Feed Type](PGFDS_Lists-of-Valid-Values.md#Feed-Type).
Total fed out | Float | Total amount of feed which has been fed out for date or period.
Total feed consumed | Float | Amount of feed which has been consumed.
Consume units | | See {Error! Reference source not found. above
Fed out per stock unit | Float | Amount of feed which has been fed out per [SU](PGFDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) per day; ([kgDM](PGFDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations)/[SU](PGFDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations)/day).
Feed consumed per stock unit | Float | Amount consumed per [SU](PGFDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) per day [kgDM](PGFDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations)/[SU](PGFDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations)/day.
Percentage of feed consumed | Float | Amount of feed eaten over the total amount of feed fed out; %
Crude protein | Float | Amount of total protein which can be metabolised from consuming the feed; kilograms of protein/kilograms of dry matter (kg/[kgDM](PGFDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations)).
Metabolisable energy | Float | Amount of energy which can be metabolised from consuming the feed; megajoules of metabolisable energy/kilogram of dry matter ([MJ](PGFDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations)/[kgDM](PGFDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations)).
Average utilisation of purchased supplements | Float | Weighted average of all feed imported; %

##### Sale
Sale of supplementary feed

Attributes | Data Types | Notes
:--------- | :--------- | :----
Supplementary feed type sold | Enumeration | See [Feed Type](PGFDS_Lists-of-Valid-Values.md#Feed-Type).
Feed Sold | Float | Amount of feed sold.
Sale units | | See table above.

#### Grazing Observations

The following section defines items we have categorised as grazing. Grazing observations are typically of short duration (hours, a few days, or potentially weeks).

##### Grazing event

Animals grazing a paddock, block or area.

Attributes | Data Types | Notes
:--------- | :--------- | :----
Paddock name | String | Name or identifier of paddock, block or area.
Mob ID | String | Mob Identifier of animals currently grazing.
Total pasture consumed | Float | Amount of pasture which has been consumed; tonnes of dry matter/hectare; [tDM](PGFDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations)/[ha](PGFDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations).
Pasture consumed per mm of water applied | Float | Amount of pasture consumed per millimetre of water applied by rain and irrigation; [kgDM](PGFDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations)/[ha](PGFDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations)/mm.
Pasture utilisation | Float | Percentage of total pasture grown that is eaten by animals in the period; %

The following table defines grazing summaries. In contrast to grazing events, a grazing summary describes a longer duration grazing interaction between mobs of animals and a farm or block, which may summarise multiple individual grazing events. A grazing summary requires both a date and duration (which may be specified in the Observation Date).

##### Grazing off	
Summary of grazing off event	

Attributes | Data Types | Notes
:--------- | :--------- | :----
Farm ID	| String | Identifier of farm where animals are currently grazing.
Mob ID | String | Mob Identifier of animals currently grazing.
Animals grazing off | Integer | Number of animals being grazed off.

##### Grazing system
Summary of grazing system for the farm or block for a period.

Attributes | Data Types | Notes
:--------- | :--------- | :----
Grazing System | Enumeration | See [Grazing System](PGFDS_Lists-of-Valid-Values.md#Grazing-System).
Rotation Length | Integer | Number of days.
Grazeable Area | Float | Size of the area being grazed (net of bush, swamps, etc); in m2 (SI unit) or hectares (ha, accepted non-SI unit). Implementations must clearly specify which unit is used, and ensure consistent use. For spatial data interchange m2 should be used<sup id="INSPIRE">[1](#f1)</sup>. 


#### Pasture Attributes

The following table defines items we have categorised as pasture (the type of pasture and level of cover).

Attributes | Data Types | Notes
:--------- | :--------- | :----
Pasture type | Enumeration | See [Pasture Type](PGFDS_Lists-of-Valid-Values.md#Pasture-Type)
Years in pasture | Integer | Amount of time a block has been in pasture since the last regrassing.
Clover level | Enumeration | Annual average clover content (as a proportion of pasture dry matter) where fertiliser N inputs are not applied; Very low, Low, Medium, High, Very high.
 
#### Pasture Observations

The following section defines items we have categorised as pasture. 

##### Pasture
The type of pasture and level of cover.

Attributes | Data Types | Notes
:--------- | :--------- | :----
Last Pasture Cover | Float | Amount of pasture dry matter per hectare; kilograms of dry matter/hectare ([kgDM](PGFDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations)/ha).
Last Pasture Cover Date | Date | Previous pasture cover measurement.
Pasture growth | Float | Rate of growth of pasture; kilograms of dry matter/hectare/day ([kgDM](PGFDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations)/ha/day).
Tiller Number | Integer | Number of tillers/m2.

##### Pest monitoring	

Monitoring of insects and other pests in pasture and crops. 

Attributes | Data Types | Notes
:--------- | :--------- | :----
Pest | Enumeration | See [Pests](PGFDS_Lists-of-Valid-Values.md#Pests)
Pest population | Integer | Number/m2
Insect size | Integer | Average insect size; mm.
Sampling technique | Enumeration | See {Appendix 0

##### Weed Monitoring	

Monitoring of weeds in pasture and crops.

Attributes | Data Types | Notes
:--------- | :--------- | :----
Weeds | Enumeration | See New Zealand Weeds<sup id="WEEDS">[1](#f1)</sup>.

#### Pasture and Feed Analysis Observations

The following table defines items we have categorised as analysis of pasture and supplementary feed.

##### Feed characteristics
Properties of the pasture or supplementary feed

Attributes | Data Types | Notes
:--------- | :--------- | :----
Dry matter | Float | %[DM](PGFDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations)
Crude protein | Float | Amount of total protein which can be metabolised from consuming the feed; kilograms/kilograms of dry matter.
Crude fat | Float | Crude fat content; %[DM](PGFDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations)
Ash | Float | Ash content; %[DM](PGFDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations)
Acid detergent fibre | Float | Cellulose and lignin fraction in forages; %[DM](PGFDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations).
Neutral detergent fibre | Float | Fraction containing hemicelluloses, cellulose and lignin in forages; %[DM](PGFDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations).
Soluble sugars | Float | Soluble sugars content; %[DM](PGFDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations).
Starch | Float | starch content; %[DM](PGFDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations)
Digestibility | | The percentage of feed that is able to be digested 
Metabolisable energy | Float | Amount of energy which can be metabolised from consuming the feed; mega joules/kilograms of dry matter (MJ/[kgDM](PGFDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations)).
Dietary cation anion difference | Integer | mEq (milliequivalents) / 100g [DM](PGFDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations).
pH | Float | 
Volatile Fatty Acid Profile | Float | %
Ammonium N:Total N | Float | %
Nitrate-Nitrogen level | Float | %

##### Feed minerals
Mineral composition of the pasture or supplementary feed. 

Attributes | Data Types | Notes
:--------- | :--------- | :----
Mineral | Enumeration | See [Nutrient](PGFDS_Lists-of-Valid-Values.md#Nutrient)
Mineral concentration | Float/Integer | Float: % for N, P, K, S, Ca, Mg, Na, Cl; <br>Integer: mg/kg for Fe, Mn, Zn, Cu, B, Mo, Co, Se

#### Footnotes

<b id="f1">1.</b> See section 6.1.3 of D2.8.I.2 Data Specification on Administrative Units – [Technical Guidelines](https://inspire.ec.europa.eu/id/document/tg/au). [↩](#INSPIRE)

<b id="f2">2.</b> [New Zealand Weeds](http://www.massey.ac.nz/massey/learning/colleges/college-of-sciences/clinics-and-services/weeds-database/weeds-database_home.cfm), Dr Kerry Harrington, Massey University.. [↩](#WEEDS)

