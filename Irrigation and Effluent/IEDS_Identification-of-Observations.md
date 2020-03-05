### Identification of Observations

Contents:
* [Location Identification](#Location-Identification)
* [Spatial Attributes](#Spatial-Attributes)

This section focusses on the identification of the observations and attributes defined in this standard.  The identifier of the observation may be a location (such as of a farm or irrigation scheme), a block or paddock within a farm, a transect or a geographic feature, a pond, a system, or piece of equipment.

#### Location Identification

A farm or irrigation scheme [SHALL](IEDS_Definitions-and-Abbreviations_Interpretation.md#Interpretation) be defined as a location as per the [Animal Data Standard](https://github.com/Datalinker-Org/Farm-Data-Standards/blob/master/Animal%20Data%20Standards/README.md). The standard specifies several identifiers that are accepted for property identification in New Zealand and supports the interchange of data using these mechanisms.  This Irrigation and Effluent Data Standard adopts the same location identification. 

Several identifiers are accepted for property identification in New Zealand:

* Ministry of Primary Industry FarmsOnLine identifier;

* [NAIT](IEDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) Location identifier (one or more FarmsOnLine identifiers registered with [NAIT](IEDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations))

* AgriBase<sup id="AgriBase">[1](#f1)</sup> farm_id (based on a coordinate pair in lat/long, NZTM or NZMG coordinates)

* EPCglobal Serialised Global Location Number<sup id="ECP">[2](#f2)</sup> (as used by the NZ Business Number system); and

* Herd Testing Location identifier using the NZMS1 (1939 to 1975) map grid reference.

For historic reasons, it will be necessary to support the interchange of data utilising all of these mechanisms. This standard therefore requires that location identifiers shall be prefixed with a [URN](IEDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) namespace identifier. Acceptable [URN](IEDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) namespaces for use in New Zealand location identifiers shall be:

* urn:epc:id:sgln or

* a nzl: registered location namespace.

For specific interchanges agreed between two parties, the parties may agree to exchange identifiers within a single namespace only, and dispense with the namespace prefix.

#### Spatial Attributes

Features with location attributes can be described by a set of geographic information. **When transferring data about physical farm features, the following Geographic Coordinates, Geographic Shape, and Feature Identifier [SHOULD](IEDS_Definitions-and-Abbreviations_Interpretation.md#Interpretation) be interchanged with that data. Geographic coordinates and shape are applicable for each location feature so will not be replicated throughout the document.**

Attributes | Data Types | Notes
:--------- | :--------- | :----
Geographic Coordinates |  | Coordinates representing a location, using latitude and longitude, or a recognised coordinate system identified using the European Petroleum Survey Group (EPSG) parameter registry guide.
Geographic Shape | | [OGC](IEDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) Web Feature Service URL or string of embedded feature, using a recognised coordinate system identified using the European Petroleum Survey Group (EPSG) parameter registry guide.
Feature Identifier | String | Identifier used to identify the feature.
Feature Name | String | Name used to identify the feature.
validFrom | [ISO Date](IEDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) | Date at which this spatial data object begins.
validThrough | [ISO Date](IEDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations)| Date at which this spatial data object ends.

#### Footnotes

<b id="f1">1.</b> [AgriBase](https://www.asurequality.com/our-solutions/agribase/), AsureQuality. [↩](#AgriBase)

<b id="f2">2.</b> [EPCglobal SGLN and GLN](http://www.gs1.org/gdsn/standards). [↩](#ECP)
