### Identification of Locations and Herds

Contents:
* [Location Identification](#Location-Identification)
* [Spatial Attributes](#Spatial-Attributes)
* [Herd and Flock Identification](#Herd-and-Flock-Identification)
* [Registration of Namespaces](#Registration-of-Namespaces)

#### Location Identification

Distinct identification of locations is required in animal recording to support both traceability systems and identification of environmental contemporary groups for genetic analysis. A number of identifiers are accepted for property identification in New Zealand:

* Ministry for Primary Industries FarmsOnLine identifier;

* AgriBase[^AgriBase] farm_id (based on a coordinate pair in lat/long, NZTM or NZMG coordinates);

* EPCglobal Serialised Global Location Number[^ECPglobal] (sGLN) (as used by the EPC Network Architecture).  (The NZ Business Number is based on a GS1 GLN through a partnership with GS1 NZ); and

* Regulated Dairy Herd Testing Location identifier using the NZMS1 (1939 to 1975) map grid reference.

For historic reasons it will be necessary to support the interchange of data utilising all of these mechanisms. This standard therefore requires that location identifiers SHALL be prefixed with a [URN](docs/FMDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) namespace identifier.

**This standard therefore requires that:

1. **Location identifiers [SHALL](docs/FMDS_Definitions-and-Abbreviations_Interpretation.md#Interpretation) be prefixed with a URN (RFC 2141 Uniform Resource Name)[^URN]  namespace identifier, so that software systems can determine how to interpret each identifier,**

2.	**Acceptable URN namespaces for use in New Zealand location identifiers [SHALL](docs/FMDS_Definitions-and-Abbreviations_Interpretation.md#Interpretation) be:**
  * **urn:epc:id:sgln o**
  * **a nzl: registered location namespace.**

3.	**It [SHALL](docs/FMDS_Definitions-and-Abbreviations_Interpretation.md#Interpretation) be the responsibility of systems interacting with legacy software, databases, and devices to interpret interchanged animal identifiers to or from the form used by the legacy system.**

4.	**For specific interchanges agreed between two parties, the parties [MAY](docs/FMDS_Definitions-and-Abbreviations_Interpretation.md#Interpretation) agree to exchange identifiers within a single namespace only, and dispense with the namespace prefix.**

#### Spatial Attributes

Features with location attributes can be described by a set of geographic information. **When transferring data about physical farm features, the following Geographic Coordinates, Geographic Shape, and Feature Identifier [SHOULD](docs/FMDS_Definitions-and-Abbreviations_Interpretation.md#Interpretation) be interchanged with that data. Geographic coordinates and shape are applicable for each location feature so will not be replicated throughout the document.**

Attributes or Fields | Data Types | Notes
:------------------- | :--------- | :----
Geographic Coordinates | | Coordinates representing a location, using latitude and longitude, or a recognised coordinate system identified using the [European Petroleum Survey Group (EPSG) parameter registry guide](http://www.iogp.org/pubs/373-07-3.pdf).
Geographic Shape | | [OGC](docs/FMDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) Web Feature Service URL or string of embedded feature, using a recognised coordinate system identified using the [European Petroleum Survey Group (EPSG) parameter registry guide](http://www.iogp.org/pubs/373-07-3.pdf).
Feature Identifier | String | Identifier used to identify the feature.
Feature Name | String | Name used to identify the feature
validFrom | [ISO Date](docs/FMDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) | Date at which this spatial data object begins
validThrough | [ISO Date](docs/FMDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) | Date at which this spatial data object ends

#### Herd and Flock Identification
Distinct identification of flocks or herds as the primary unit of management of a group of animals is used for traceability purposes, access control and membership, and contemporary groups for genetic analysis. There are a number of systems in use within New Zealand, including:

* [NAIT](docs/FMDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) numbers;

* AHB herd numbers;

* Dairy Industry Herd Numbers (a combination of a location and a herd number) and Participant codes;

* Beef+Lamb NZ Genetics (formerly [SIL](docs/FMDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations)) flock code;

* EPCglobal serialised Global Trade Item Number (sGTIN)[^sGTIN].

This standard requires that herd identifiers shall be prefixed with a [URN](docs/FMDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) namespace identifier.

For specific interchanges agreed between two parties, the parties may agree to exchange identifiers within a single namespace only, and dispense with the namespace prefix.

#### Registration of Namespaces

This standard requires the addition of a namespace when exchanging an identifier. While some namespaces have been formally registered (RFC 5134 for EPC and RFC 5141 for [ISO](docs/FMDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations)), there has not previously been a method for registering other namespaces for use in animal recording.

A registry process for top-level namespaces is administered by IETF (the Internet Engineering Task Force), and the process for using this is defined in RFC 3406[^RFC3406].
New Zealand livestock and farm recording system identifiers [SHALL](docs/FMDS_Definitions-and-Abbreviations_Interpretation.md#Interpretation) be registered at www.farmdatastandards.org.nz, and issued with Namespace identifiers in the urn:nzl:farm: namespace (the NZ namespace was registered in RFC 4350[^RFC4350]). Each NZ farm recording namespace registered [SHALL](docs/FMDS_Definitions-and-Abbreviations_Interpretation.md#Interpretation) specify:

1.	The official name or description of the namespace;

2.	The organisation responsible for maintaining the namespace and issuing identifiers;

3.	Contact details for the organisation;

4.	A regular expression that may be used to determine if identifiers within the namespace are in the correct format (but not necessarily valid issued identifiers).


#### Footnotes

[^AgriBase]: [AgriBase](https://www.asurequality.com/our-solutions/agribase/), AsureQuality.

[^ECPglobal]: [EPCglobal SGLN and GLN](https://www.gs1.org/standards/id-keys/gln)

[^URN]: URN is defined in [RFC 2141](http://tools.ietf.org/html/rfc2141)

[^sGTIN]: [EPCglobal serialised Global Trade Item Number (sGTIN)](https://www.gs1.org/standards/id-keys/gtin).
  
[^RFC3406]: See [Uniform Resource Names (URN) Namespace Definition Mechanisms](http://www.ietf.org/rfc/rfc3406.txt)
  
[^RFC4350]: NZ Namespace for URN is defined in [RFC 4350](http://tools.ietf.org/html/rfc4250)
