
### Identification of Observations

Contents:
* [Location Identification](#Location-Identification)
* [Spatial Attributes](#Spatial-Attributes)

#### Location Identification 

Distinct identification of property locations will be useful in health and safety recording for general reference, and contexts such as the affected locations of a natural event. A number of identifiers are accepted for property identification in New Zealand:

* Ministry of Primary Industry FarmsOnLine identifier; 

* [NAIT](HSDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) Location identifier (one or more FarmsOnLine identifiers registered with [NAIT](HSDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations)) 

* AgriBase farm_id (based on a coordinate pair in lat/long, NZTM or NZMG coordinates)

* EPCglobal Serialised Global Location Number5 (as used by the NZ Business Number system); and 

* Herd Testing Location identifier using the NZMS1 (1939 to 1975) map grid reference.

The identification of property locations is further defined in the Farm & Model Data Standards, and is therefore not included in the Health and Safety Standard. The Farm & Model Standard includes features, data types and definitions for location data, and so any location data must be shared according to that standard.

For historic reasons it will be necessary to support the interchange of data utilising all of these mechanisms. This standard therefore requires that location identifiers [SHALL](HSDS_Definitions-and-Abbreviations_Interpretation.md#Interpretation) be prefixed with a [URN](HSDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) namespace identifier.

Acceptable [URN](HSDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) namespaces for use in New Zealand location identifiers shall be: 

* urn:epc:id:sgln or 

* a nzl:pri: registered location namespace. 

For specific interchanges agreed between parties, the parties may agree to exchange identifiers within a single namespace only, and dispense with the namespace prefix. 

#### Spatial Attributes

Location is a key piece of information for health and safety management. Location points and physical features (e.g. first aid points and fuel storage dumps) can be described by a set of geographic information. **When transferring data about physical features, geographic coordinates and geographic shape [SHOULD](HSDS_Definitions-and-Abbreviations_Interpretation.md#Interpretation) be interchanged with that data.**

The Farm Features and Attributes Data Standard defines attributes for farm features which have a spatial representation. Some of the attributes described in that Data Standard may be useful in a Health and Safety management context, for example the recording of information about spatial features which may also present as a hazard risk. 

Attributes or Fields | Data Types | Notes
:------------------- | :--------- | :----
Geographic Coordinates | | Coordinates representing a location, using latitude and longitude, or a recognised coordinate system identified using the [European Petroleum Survey Group (EPSG) parameter registry guide](http://www.iogp.org/pubs/373-07-3.pdf).
Geographic Shape | | [OGC](HSDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) Web Feature Service URL or string of embedded feature, using a recognised coordinate system identified using the [European Petroleum Survey Group (EPSG) parameter registry guide](http://www.iogp.org/pubs/373-07-3.pdf).
Feature Identifier | String | Identifier used to identify the feature.
Feature Name | String | Name used to identify the feature.
validFrom | [ISO Date](HSDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) | Date at which this spatial data object begins.
validThrough | [ISO Date](HSDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) | Date at which this spatial data object ends.
