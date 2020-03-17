### Identification of Animals, Herds, and Locations

* [Animal Identification](#Animal-Identification)
* [Location Identification](#Location-Identification)
* [Herd and Flock Identification](#Herd-and-Flock-Identification)
* [Registration of Namespaces](#Registration-of-Namespaces)

This section focuses on the identification of animals and other entities referenced in the interchange of animal information, specifically locations and enterprises (herds or flocks). 

#### Animal Identification

There are a number of official, semi-official, and ad-hoc forms of animal identification in use. This ranges from the regulated<sup id="NAIT">[1](#f1)</sup>  use of ISO 11784/11758 [RFID](ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) for cattle and deer, through current official recording and traceability programme identifiers (some regulated), to breeding and recording scheme identifiers that are no longer actively used but which provide useful data or linkages between animals that need to be retained for future analysis.

Identifiers fall into one of three broad categories:

1. **[Official recording scheme identifiers](ADS_Animal-Identifiers-NZ.md#Official-Recording-Scheme-Identifiers)** – lifetime identifiers allocated to animals by an official recording scheme, typically as part of a traceability or herd improvement programme.

2. **[Electronic identifiers](ADS_Animal-Identifiers-NZ.md#Electronic-Identifiers)** – unique numbers carried on a machine-readable tag or chip applied to animals, electronic identifiers are intended to be lifetime identifications (but may in fact be changed or replaced), and may also be required as part of a traceability or herd improvement programme. Electronic identifiers may in some cases also be official identifiers.

3. Management identifiers – these are typically short-form visual tags or marks applied to animals to make identification easy within a single management unit (herd or farm). There is no guarantee that these identifiers are truly unique within a farm, and they are almost certainly not unique temporally or nationally.

Complete list of [Animal Identifiers used in New Zealand](ADS_Animal-Identifiers-NZ.md).

A single clearly enunciated identifier type for all animals is not yet practical because of the need to support legacy data, recording devices and systems, and because there is often value for humans in being able to interpret parts of a human-readable identifier. 

Accordingly, this standard specifies:

1. **A single animal [MAY](ADS_Definitions-And-Abbreviations_Interpretation.md#Interpretation) have more than one identifier but [SHALL](ADS_Definitions-And-Abbreviations_Interpretation.md#Interpretation) have at least one identifier that is unique within its namespace;** 

2. **When interchanging data between systems, each animal identifier [SHALL](ADS_Definitions-And-Abbreviations_Interpretation.md#Interpretation) include a URN ([RFC](ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) 2141 Uniform Resource Name)<sup id="URN">[2](#f2)</sup>
  namespace identifier, so that software systems can determine how to interpret each identifier;**

3. **When interchanging data between systems, each animal identifier [SHOULD](ADS_Definitions-And-Abbreviations_Interpretation.md#Interpretation) also specify the type of identifier (Official, Management, and/or Electronic) so that a receiving system which is unable to interpret namespaces may use a generic method to interpret the identifier;  and**

4. **It [SHALL](ADS_Definitions-And-Abbreviations_Interpretation.md#Interpretation) be the responsibility of systems interacting with legacy software, databases, and devices to interpret interchanged animal identifiers to or from the form used by the legacy system.** 

5. **For specific interchanges agreed between two parties, the parties [MAY](ADS_Definitions-And-Abbreviations_Interpretation.md#Interpretation) agree to exchange identifiers within a single namespace only, and dispense with the namespace prefix.**

The following are examples of URN notation used for [ISO](ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) 11784 and [GS1](ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) SGTIN identifiers:

ID|
:---|
urn:epc:id:sgtin:3.003700.00542.77346595|
urn:iso:std:iso:11784:982.009104636715|

These are based on name space definitions for EPC (Electronic Product Code) defined in [RFC](ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) 5134<sup id="ECP">[3](#f3)</sup>  and for [ISO](ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) (International Standards Organisation) defined in RFC 5141<sup id="ISO">[4](#f4)</sup>. 

#### Location Identification

Distinct identification of locations is required in animal recording to support both traceability systems and identification of environmental contemporary groups for genetic analysis. 

A number of identifiers are accepted for property identification in New Zealand:

* Ministry for Primary Industries FarmsOnLine identifier;

* AgriBase<sup id="AgriBase">[5](#f5)</sup>  farm_id (based on a coordinate pair in lat/long, NZTM or NZMG coordinates)

* EPCglobal Serialised Global Location Number<sup id="ECPG">[6](#f6)</sup>  (as used by the NZ Business Number system); and

* Regulated Dairy Herd Testing Location identifier using the NZMS1 (1939 to 1975) map grid reference.

For historic reasons, it will be necessary to support the interchange of data utilising all of these mechanisms. This standard therefore requires that location identifiers [SHALL](ADS_Definitions-And-Abbreviations_Interpretation.md#Interpretation) be prefixed with a URN namespace identifier. 

**Acceptable URN namespaces for use in New Zealand location identifiers [SHALL](docs/ADS_Definitions-And-Abbreviations_Interpretation.md#Interpretation) be:**
* **urn:epc:id:sgln or**
* **a nzl: registered location namespace.**

**For specific interchanges agreed between two parties, the parties [MAY](docs/ADS_Definitions-And-Abbreviations_Interpretation.md#Interpretation) agree to exchange identifiers within a single namespace only, and dispense with the namespace prefix.**

#### Herd and Flock Identification

Distinct identification of flocks or herds as the primary unit of management of a group of animals is used for traceability purposes, access control and membership, and contemporary groups for genetic analysis. 

There are a number of systems in use within New Zealand, including:

* [NAIT](ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) numbers;

* AHB herd numbers;

* Dairy Industry Herd Numbers (a combination of a location and a herd number) and Participant codes;

* Beef+Lamb NZ Genetics (formerly [SIL](ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations)) flock code.

This standard requires that herd identifiers shall be prefixed with a URN namespace identifier. For specific interchanges agreed between two parties, the parties may agree to exchange identifiers within a single namespace only, and dispense with the namespace prefix.

#### Registration of Namespaces

This standard requires the addition of a namespace when exchanging an identifier. While some namespaces have been formally registered (RFC 5134 for EPC and RFC 5141 for [ISO](ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations)), there has not previously been a method for registering other namespaces for use in animal recording.

A registry process for top-level namespaces is administered by [IETF](ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) (the Internet Engineering Task Force), and the process for using this is defined in RFC 3406<sup id="URN/Def">[7](#f7)</sup>.

New Zealand livestock and farm recording system identifiers [SHALL](ADS_Definitions-And-Abbreviations_Interpretation.md#Interpretation) be registered at [Farm Data Standards](https://github.com/Datalinker-Org/Farm-Data-Standards/blob/master/Information%20for%20Customers/FarmDataStandards_Namespaces-for-Farm-Data-Identifiers.md#Registering%20your%20 Namespace%20Identifier), and issued with Namespace identifiers in the urn:nzl:farm: namespace (the NZ namespace was registered in RFC 4350<sup id="NZURN">[8](#f8)</sup>). Each NZ farm recording namespace registered [SHALL](ADS_Definitions-And-Abbreviations_Interpretation.md#Interpretation) specify:

1. The official name or description of the namespace;

2. The organisation responsible for maintaining the namespace and issuing identifiers;

3. Contact details for the organisation;

4. A regular expression that may be used to determine if identifiers within the namespace are in the correct format (but not necessarily valid issued identifiers).

##### Footnotes

<b id="f1">1</b> [NAIT Animal Identification and Tracing Act 2012](http://www.legislation.govt.nz/act/public/2012/0002/latest/DLM3430220.html). [↩](#NAIT)

<b id="f2">2</b> URN is defined in [RFC 2141](http://tools.ietf.org/html/rfc2141). [↩](#URN)

<b id="f3">3</b> EPC Namespace for URN is defined in [RFC 5134](http://tools.ietf.org/html/rfc5134). [↩](#ECP)

<b id="f4">4</b> ISO Namespace for URN is defined in [RFC 5141](http://tools.ietf.org/html/rfc5141). [↩](#ISO)

<b id="f5">5</b> [AgriBase, AsureQuality](https://www.asurequality.com/our-solutions/agribase/). [↩](#AgriBase)

<b id="f6">6</b> [EPCglobal SGLN and GLN](https://www.gs1.org/standards). [↩](#ECPG)

<b id="f7">7</b> [Uniform Resource Names (URN) Namespace Definition Mechanisms](http://www.ietf.org/rfc/rfc3406.txt). [↩](#URN/Def)

<b id="f8">8</b> NZ Namespace for URN is defined in [RFC 4350](http://tools.ietf.org/html/rfc4350). [↩](#NZURN)
