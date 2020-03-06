### Pasture, Grazing and Feed Observations

Contents:
* [Date and Time of an Observation](#Date-and-Time-of-an-Observation)
* [Supplementary feed](#Supplementary-feed)
* [Grazing](#Grazing)
* [Pasture](#Pasture)
* [Pasture and Feed Analysis](#Pasture-and-Feed-Analysis)

For the purpose of this Standard, an observation is the act or instance of viewing or noting a fact or occurrence for some scientific or other special purpose. Thus an observation can include a note or record of an activity carried out, an event that has occurred, or a measurement taken.

In this standard the subject of an observation may be a farm, a block of land or paddock on that farm, or a mob of animals grazing on the block or farm.

#### Date and Time of an Observation

All observations are observed or sampled at a point within time, so the record of an observation [SHALL](PGFDS_Definitions-and-Abbreviations_Interpretation.md#Interpretation) be accompanied by a date, or date and time. An Observation Date may also describe a duration or period (for example, the period of 12 months from a known date).

Item Name | Description | Cardinality | Type & Validation
:-------- | :---------- | :---------- | :----------------
Observation Date | Date (and depending on observation, time) at which the observation was made. For some events, the time component of the observation is critical; for others, the rate of change is slow enough that time is irrelevant. | 1 | [ISO 8601](PGFDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) date (and time), and optionally duration 

#### Supplementary feed

This section of the standard is concerned with supplementary feed and encompasses the harvesting, purchase, storage, consumption, and the sale of supplementary feed.

All of these observations will be identified by the farm concerned and the type of feed.  Each observation includes one or more fields that specify the quantity or weight of the feed and the units concerned. There is a table in [Supplementary Feed Observations](PGFDS_Pasture_Grazing_and_Feed_Data_Dictionary.md#Supplementary-Feed-Observations) that defines the information associated with the units specified.

The harvest may also include a block or paddock identifier and the date it was harvested.  Details of the harvesting include the feed type grown, the weight harvested and how it is packaged.

Storage of feed will include a time period identifier. Data stored includes the storage condition and the type of storage, the total feed in the inventory and the change in the amount on hand from the beginning to the end of the period.

The Consume observation will include the time period that the consumption pertains to. It describes the use of the feed including the amount fed out and the feed consumed. The Purchase and Sale observations include the date the supplement was purchased or sold respectively and the quantity.

#### Grazing

The Grazing section provides a grazing event observation and summaries for grazing off and the grazing system employed on the farm or block.

The grazing observation specifies the amount of pasture consumed and its utilisation percentage.

#### Pasture

Pasture data are identified by a farm, block, and time period.

The Pasture Cover observation defines the type of pasture and the level of cover.  The Pasture Growth observation defines the growth rate, the clover level, and the number of tillers. 

Observations of the monitoring in pasture and crops of insects and other pests and monitoring of weeds are defined.  Massey University has created a database of over 70 of the more troublesome weeds found in New Zealand agriculture and horticulture<sup id="Weeds">[1](#f1)</sup>. 

#### Pasture and Feed Analysis 
Pasture and feed analysis data describe the characteristics and nutrient analysis of the pasture and supplementary feed. 

#### Footnotes

<b id="f1">1.</b> [New Zealand Weeds](http://www.massey.ac.nz/massey/learning/colleges/college-of-sciences/clinics-and-services/weeds-database/weeds-database_home.cfm) , Dr Kerry Harrington, Massey University. [↩](#Weeds)
