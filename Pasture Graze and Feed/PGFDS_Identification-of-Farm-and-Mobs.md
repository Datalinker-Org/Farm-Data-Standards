### Identification of Farm and Mobs

The [Animal Data Standard](https://github.com/Datalinker-Org/Farm-Data-Standards/blob/master/Animal%20Data%20Standards/ADS_Identification-of-Animals-Herds-and-Locations.md) discusses the identification of locations or farms. It specifies a number of identifiers that are accepted for property identification in New Zealand and supports the interchange of data using all of these mechanisms.  This Grazing and Feed Data Standard adopts the same location identification.

A number of identifiers are accepted for property identification in New Zealand:

* Ministry of Primary Industry FarmsOnLine identifier;

* [NAIT](PGFDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) Location identifier (one or more FarmsOnLine identifiers registered with [NAIT](PGFDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations)).

* AgriBase<sup id="AgriBase">[1](#f1)</sup> farm_id (based on a coordinate pair in lat/long, NZTM or NZMG coordinates)

* EPCglobal Serialised Global Location Number<sup id="ECPG">[2](#f2)</sup> (as used by the NZ Business Number system); and

* Herd Testing Location identifier using the NZMS1 (1939 to 1975) map grid reference.

For historic reasons it will be necessary to support the interchange of data utilising all of these mechanisms. This standard therefore requires that location identifiers shall be prefixed with a [URN](PGFDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) namespace identifier. Acceptable [URN](PGFDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) namespaces for use in New Zealand location identifiers shall be:

* urn:epc:id:sgln or

* a nzl: registered location namespace.

For specific interchanges agreed between two parties, the parties may agree to exchange identifiers within a single namespace only, and dispense with the namespace prefix.

The Animal Data Standard (see [Groups of Animals](https://github.com/Datalinker-Org/Farm-Data-Standards/blob/master/Animal%20Data%20Standards/ADS_Groups-of-Animals.md), [Observation Attributes](docs/ADS_Animal-Observations.md#Observation-Attributes) and [Group Membership](ADS_Animal-Lifecycle-Data-Dictionary_Group-Membership.md)) refers to mobs in its discussion of groups of animals. The Grazing observation is defined in this Grazing and Feed Data Standard for mobs.  A mob is identified by a group name.  It is uniquely identified by a [URN](PGFDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) identifier and may have a non-unique display name.

#### Footnotes

<b id="f1">1.</b> [AgriBase](https://www.asurequality.com/our-solutions/agribase/), AsureQuality. [↩](#AgriBase)

<b id="f2">2.</b> EPCglobal [SGLN and GLN](http://www.gs1.org/access-gdsn-standards). [↩](#ECPG)
