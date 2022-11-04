### Animal Identifiers used in New Zealand (Informative)

Contents:
* [Electronic Identifiers](#Electronic-Identifiers)
* [Official Recording Scheme Identifiers](#Official-Recording-Scheme-Identifiers)
* [Other Animal Identifiers](#Other-Animal-Identifiers)

#### Electronic Identifiers

Identifier | Example | Comments
:--------- | :------ | :-------
ISO 11784<sup id="ISO">[1](#f1)</sup> | 981-018285778231 | The [ISO](ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) 11784 codes are managed by the international committee for animal recording (ICAR<sup id="ICAR">[2](#f2)</sup>). There are several representations of the code: <ul><li>Hexadecimal, which includes the entire code including flag bits</li><li>Decimal, which generally just shows the country or manufacturer code and animal number.</li></ul>In New Zealand, we use manufacturer codes where animal numbers are maintained uniquely by manufacturers. This is in contrast to (for instance) Europe, where a country-code is used, and each country maintains the unique set of animal numbers.
GS1 SGTIN | urn:epc:id:sgtin:3.003700.00542.77346595 | Some trials with UHF RFID in deer<sup id="RFID">[3](#f3)</sup> have used an SGTIN (Serialised Global Trade Item Number) issued by global standards organisation GS1<sup id="GS1">[4](#f4)</sup>, which functions much like a barcode identifies a category of products, but with the addition of a unique item number as well.

#### Official Recording Scheme Identifiers

Identifier | Example | Comments
:--------- | :------ | :-------
AHB Birth ID | 1234567-12-123 | A tag issued by the Animal Health Board (AHB)<sup id="AHB">[5](#f5)</sup> that includes herd number (7 digits), year born (2 digits) and an animal number that is unique within herd and year. The Hereford Prime Hpid initiative, and Angus Pure Source and Trace use the AHB Birth ID.
AHB Sequence | No	1234567-3123 | A tag issued by AHB that includes just the herd and a sequence number within that herd.
Dairy Birth ID (MINDA) | ABDC-12-1234 | The Dairy Birth ID format is used by both CRV and [LIC](ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations), and includes a four-letter participant code, followed by a 2-digit year and then the animal number which is unique within the participant and year. This forms one of the Dairy Core Database fields defined in the herd testing standards<sup id="NZS">[6](#f6)</sup>.
NAIT AHB TRAKA | 981-018285778231-1234567 | [NAIT](ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations)-compatible “Traka” tag issued by AHB. Traka tags<sup id="Tracka">[7](#f7)</sup> are typically used for replacements or tagging existing animals.
NAIT Dairy Traka | 981-018285778231-ABDC | A [NAIT](ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) compatible Dairy “Traka” tag is the same format as that issued by AHB, but has the dairy participant code instead of the AHB number.
NAIT Dairy Management Tag | 981-018285778231-LMNO-123 | A [NAIT](ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) compatible Dairy Management Tag combines the current herd participant code, management number, and an ISO 11784 RFID number to make a unique identification for existing dairy cows, as an alternative to using Traka tags.
SIL (Sheep) | 12345.12738.2012 |SIL<sup id="SIL">[8](#f8)</sup> is the industry performance recording scheme for sheep other than Merinos in New Zealand, and is also used to operate Deer Select.  An official SIL identifier includes the flock code and tag (the latter a text string), and may optionally include the year born (by convention the year is often included in the tag number).
MerinoSelect | 502302-2009-090736 | Merino Select<sup id="Merino">[9](#f9)</sup> is the Australian Merino performance recording system, which is used by NZ Merino stud breeders. Animal identification is in the form flock code, year born (4 digits), and animal number.

#### Other Animal Identifiers

Identifier | Example | Comments
:--------- | :------ | :-------
Interbull | HOLNZLM000123456789 | [ICAR](ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations)’s Interbull<sup id="Interbull">[10](#f10)</sup> programme is used to compare bulls across multiple countries, and may be used to align national breeding schemes to allow comparison. The identifier contains: Breed (HOL, JEY, AYS…), Country (NZL, NDL), Sex (M), and a 12-character animal number.
Bull AB Code | 102271 | [LIC](ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) currently issues AB Codes (6-digit numbers) for bulls used in the dairy industry. These codes are shorter to use on straws, catalogues, and forms, and are unique within NZ dairy bulls.
LIA Identification | L2-123456-1980-123 | The LIA (Livestock Improvement Association) codes were used to identify dairy animals before 198525. The code consists of LIA region (2 characters), herd code (6 digits), year (4 digits), and animal number (6 character string).
Breed Society Pedigree No | 123456-JR |The dairy industry herd book ID25 for pedigree dairy animals born before 1985 consists of the herd book number (6 characters), and a breed society identifier (technically 6 character string, but two characters used). 

#### Footnotes

<b id="f1">1.</b> Specified in [ISO 11784:1996](http://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.htm?csnumber=25881) and referenced in [ISO 14223-2:2010](https://www.iso.org/standard/45364.html). [↩](#ISO) 

<b id="f2">2.</b> [International Committee for Animal Recording](https://www.icar.org/). [↩](#ICAR) 

<b id="f3">3.</b> [The Use of EPC RFID Standards for Livestock and Meat Traceability](http://www.rfid-pathfinder.org.nz/wp-content/uploads/2012/08/EPCIS-Final-Report5.pdf), Gary Hartley, NZ RFID Pathfinder Group, January 2013. [↩](#RFID) 

<b id="f4">4.</b> [GS1](http://www.gs1.org/epcglobal). [↩](#GS1)

<b id="f5">5.</b> [Animal Health Board](https://ospri.co.nz/) and [programme](https://www.ospri.co.nz/our-programmes/). [↩](#AHB)

<b id="f6">6.</b> NZS 8100, 2011 draft Herd Testing Standard (and earlier 2007 edition). [↩](#NZS)

<b id="f7">7.</b> For more about Traka tags, see the [NAIT Visual Tag guidelines](http://www.nait.co.nz/news-and-publications/nait-user-guides-and-fact-sheets/tagging-requirements/). [↩](#Tracka)

<b id="f8">8.</b> [SIL: Sheep Improvement Limited](https://www.sil.co.nz/) – a wholly owned subsidiary of Beef+Lamb NZ. [↩](#SIL)

<b id="f9">9.</b> [Merino Select](http://www.sheepgenetics.org.au/Breeding-services/MERINOSELECT-Home). [↩](#Merino)

<b id="f10">10.</b> [Interbull Guidelines](https://interbull.org/ib/nat_id_system). [↩](#Interbull)
