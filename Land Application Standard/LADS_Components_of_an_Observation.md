### Components of an Observation

Contents:
* [Location Identification](#Location-Identification)
* [Spatial Attributes](#Spatial-Attributes)

For the purpose of this Standard, an observation is the act or instance of viewing or noting a fact or occurrence for some scientific or other special purpose. Thus an observation can include a note or record of an activity carried out, an event that has occurred, or a measurement taken.

The Open Geospatial Consortium describes observations<sup id="OGC">[1](#f1)</sup> as involving “sampling of an ultimate feature of interest”.

The subject of the observations In the Land Application Data Standard is a geographic feature. The geographic feature may be identified by a farm identifier and a block or paddock identifier or by a spatial representation (such a polygon or polyline).

Observations will also have other principle components, particularly an observation date (and optionally) time of observation (or planned activity), and reference identifications within source or destination systems (typically order numbers or job numbers).

#### Location Identification

A farm [SHALL](LADS_Definitions-and-Abbreviations_Interpretation.md#Interpretation) be defined as a location.  The Animal Data Standard discusses in the [identification of locations or farm](https://github.com/Datalinker-Org/Farm-Data-Standards/blob/master/Animal%20Data%20Standards/ADS_Identification-of-Animals-Herds-and-Locations.md). It specifies a number of identifiers that are accepted for property identification in New Zealand and supports the interchange of data using all of these mechanisms.  This Land Application Data Standard adopts the same location identification.  

A number of identifiers are accepted for property identification in New Zealand:

* Ministry of Primary Industry FarmsOnLine identifier;

* [NAIT](LADS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) Location identifier (one or more FarmsOnLine identifiers registered with [NAIT](LADS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations))

* AgriBase<sup id="AgriBase">[2](#f2)</sup> farm_id (based on a coordinate pair in lat/long, NZTM or NZMG coordinates)

* EPCglobal Serialised Global Location Number<sup id="ECPG">[3](#f3)</sup> (as used by the NZ Business Number system); and

* Herd Testing Location identifier using the NZMS1 (1939 to 1975) map grid reference.

For historic reasons it will be necessary to support the interchange of data utilising all of these mechanisms. This standard therefore requires that location identifiers shall be prefixed with a [URN](LADS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) namespace identifier. Acceptable [URN](LADS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) namespaces for use in New Zealand location identifiers shall be:

* urn:epc:id:sgln or

* a nzl:pri: registered location namespace.

For specific interchanges agreed between parties, the parties may agree to exchange identifiers within a single namespace only, and dispense with the namespace prefix.

#### Spatial Attributes

[GPS](LADS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) guidance systems are commonly used for the management of spreading either in a vehicle or an aircraft to provide benefits such as accuracy, even spread of the product, reduced distance travelled, traceability and audit requirements, a means for billing the customer, identification of ecological hot-spots.  [GPS](LADS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) farm maps may be imported into the guidance system.

[Spread Representations](LADS_Land-Applications-Data-Dictionary.md#Spread-Representations) provides for the capture of spread and spray tracks, or for providing guidance of planned application areas and hot-spot areas to be avoided or protected.  A variety of formats are allowed for the spatial representation.

Features with location attributes can be described by a set of geographic information. **When transferring data about spatial features, the following Geographic Coordinates, Geographic Shape, and Feature Identifier [SHOULD](LADS_Definitions-and-Abbreviations_Interpretation.md#Interpretation) be interchanged with that data. Geographic coordinates and shape are applicable for each location feature so will not be replicated throughout the document.**

Attributes or Fields | Data Types | Notes
:------------------- | :--------- | :----
Geographic Coordinates | |Coordinates representing a location, using latitude and longitude, or a recognised coordinate system identified using the [European Petroleum Survey Group (EPSG) parameter registry guide](http://www.iogp.org/pubs/373-07-3.pdf).
Geographic Shape | |[OGC](LADS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) Web Feature Service [URL](LADS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) or string of embedded feature, using a recognised coordinate system identified using the [European Petroleum Survey Group (EPSG) parameter registry guide](http://www.iogp.org/pubs/373-07-3.pdf).
Feature Identifier | String | Identifier used to identify the feature. 
Feature Name | String | Name used to identify the feature.
validFrom | [ISO Date](LADS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) | Date at which this spatial data object begins.
validThrough | [ISO Date](LADS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) | Date at which this spatial data object ends.

#### Footnotes

<b id="f1">1.</b> [Observations and Measurements](https://www.opengeospatial.org/standards/om). [↩](#OGC)

<b id="f2">2.</b> [AgriBase](https://www.asurequality.com/our-solutions/agribase/), AsureQuality . [↩](#AgriBase)

<b id="f3">3.</b> See EPCglobal [SGLN and GLN](https://www.gs1.org/standards/id-keys/gln). [↩](#ECPG)
