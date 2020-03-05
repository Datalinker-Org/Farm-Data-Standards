### Location Identification

A Farm Feature or Attribute SHALL be defined as a location. The [Animal Data Standard](https://github.com/Datalinker-Org/Farm-Data-Standards/blob/master/Animal%20Data%20Standards/README.md) discusses in [Location Identification](https://github.com/Datalinker-Org/Farm-Data-Standards/blob/master/Animal%20Data%20Standards/ADS_Identification-of-Animals-Herds-and-Locations.md#Location-Identification) the identification of locations or farms. The standard specifies several identifiers that are accepted for property identification in New Zealand and supports the interchange of data using these mechanisms.  This Data Standard adopts the same location identification.

Several identifiers are accepted for property identification in New Zealand:

* Ministry of Primary Industry FarmsOnLine identifier;

* [NAIT](FFADS_Definitions-and-Abbreviations.md#Definitions-and-Abbreviations) Location identifier (one or more FarmsOnLine identifiers registered with NAIT)

* AgriBase<sup id="AgriBase">[1](#f1)</sup> farm_id (based on a coordinate pair in lat/long, NZTM or NZMG coordinates)

* EPCglobal Serialised Global Location Number<sup id="GDSN">[2](#f2)</sup> (as used by the NZ Business Number system); and

* Herd Testing Location identifier using the NZMS1 (1939 to 1975) map grid reference.


For historic reasons, it will be necessary to support the interchange of data utilising all of these mechanisms. This standard therefore requires that location identifiers shall be prefixed with a [URN](FFADS_Definitions-and-Abbreviations.md#Definitions-and-Abbreviations) namespace identifier. Acceptable URN namespaces for use in New Zealand location identifiers shall be:

* urn:epc:id:sgln or

* a nzl: registered location namespace.

For specific interchanges agreed between two parties, the parties may agree to exchange identifiers within a single namespace only, and dispense with the namespace prefix.

### Spatial Attributes

Features with location attributes can be described by a set of geographic information. **When transferring data about physical farm features, the following Geographic Coordinates, Geographic Shape, and Feature Identifier [SHOULD](FFADS_Definitions-and-Abbreviations.md#Interpretation) be interchanged with that data. Geographic coordinates and shape are applicable for each location feature so will not be replicated throughout the document.**

Attributes | Data Types | Notes
:--------- |:---------- | :----
Geographic Coordinates | Coordinates | Representing a location, using latitude and longitude, or a recognised coordinate system identified using the European Petroleum Survey Group (EPSG) parameter registry guide.
Geographic Shape | [OGC](FFADS_Definitions-and-Abbreviations.md#Definitions-and-Abbreviations) Web Feature Service URL or string of embedded feature. |  Using a recognised coordinate system identified using the European Petroleum Survey Group (EPSG) parameter registry guide.
Feature Identifier | String | Identifier used to identify the feature.
Feature Name | String | Name used to identify the feature.
validFrom | [ISO Date](FFADS_Definitions-and-Abbreviations.md#Definitions-and-Abbreviations) | Date at which this spatial data object begins.
validThrough | [ISO Date](FFADS_Definitions-and-Abbreviations.md#Definitions-and-Abbreviations) |  Date at which this spatial data object ends.

#### Footnotes

<b id="f1">1.</b> [AgriBase](https://www.asurequality.com/our-solutions/agribase/), AsureQuality. [↩](#AgriBase)
 
<b id="f2">2.</b> See EPCglobal [SGLN and GLN](https://www.gs1.org/standards). [↩](#GDSN)
