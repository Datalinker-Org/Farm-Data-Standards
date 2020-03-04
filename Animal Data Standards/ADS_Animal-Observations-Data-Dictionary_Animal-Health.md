### Animal Health Observations

Contents:
* [Diagnosis](#Diagnosis)
* [Treatment](#Treatment)
* [Farming Procedure](#Farming-Procedure)
* [Surgery](#Surgery)
* [Injury](#Injury)

#### Diagnosis

The diagnosis of a health condition. [ICAR](ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) provides a detailed document about diagnosis of health conditions.

Attribute | Data Type | Notes 
:-------- | :-------- | :----
Diagnosed By | String | Name of person.
Role Diagnosed By | Enumeration | Veterinarian, Farmer, Technician.
Affected Part | Enumeration | Body part or system affected, coded using [ICAR](ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) diagnosis coding system<sup id="IARP">[1](#f1)</sup>.
Disease Category | Enumeration | See [Animal Life](ADS_Animal-Lifecycle-Data-Dictionary.md#Animal-Life).
Disease | String | Name of the disease.
Disease Code | Enumeration | Using [ICAR](docs/ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) diagnosis coding system<sup id="ACVM">[2](#f2)</sup>, see [Animal Life](ADS_Animal-Lifecycle-Data-Dictionary.md#Animal-Life).
Disease Strain | String |

#### Treatment

A record of a health treatment applied (for instance, medication, vaccination, drenching or dipping). 

Attribute | Data Type | Notes 
:-------- | :-------- | :----
Treated By | String | Operator who applied the health treatment.
Health Product | String | Trade name of the health product.
Registration Number | String | [ACVM](ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) registration number of product.
[SKU](ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) | Integer | Stock keeping code (barcode).
Organic Approved Remedy | Boolean | True if organic approved – the default is False.
Treatment Method | Enumeration | See [Treatment Method](#Treatment-Method).
Batch Number | String | Batch number of product used.
Expiry Date | Date | Expiry date of batch. 
Dose Rate | Float | Dose that was administered.
Dose Units | Enumeration | ml, mg; units of the amount administered. 
Withholding Period Meat | Integer | Days. 
Hormone Indicator | Flag (True/False) | Indicates that the product applied contains a hormone growth promotant. 
	
#### Farming Procedure

A record of a routine farming procedure performed (for instance, dehorning, shearing, crutching, disbudding or castration).

Attribute | Data Type | Notes 
:-------- | :-------- | :----
Procedure Type | Enumeration | See [Procedure Type](#Procedure-Type).
Procedure Method | String |

#### Surgery

A record of surgery performed, especially for major surgery.

Attribute | Data Type | Notes 
:-------- | :-------- | :----
Surgery Procedure | Enumeration | See [ACVS](ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) list of Surgical Procedures<sup id="ACVS">[3](#f3)</sup>. 
Surgery Part | Enumeration | Body part or system affected, coded using the 2nd level of the [ICAR](ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) diagnosis coding system<sup id="ACVM">[2](#f2)</sup>.
Surgery Outcome | String |

#### Injury

Records an injury event.

Attribute | Data Type | Notes 
:-------- | :-------- | :----
Injury Type | Enumeration | Accident, Misadventure
Affected Part | Enumeration | Body part or system affected, coded using the 2nd level of the [ICAR](ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) diagnosis coding system<sup id="ACVM">[2](#f2)</sup>.
Injury Comment | String | Description of injury.

##### Animal Life

The following table defines items categorised as Animal Life Data that typically do not change over the lifetime of the animal.

Attributes | Data Type | Description
:--------- | :-------- | :----------
Birth Date | [ISO](ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) 8601 Date | The date on which an animal was born. See also: Birth Date Confidence, Birth Year, Birth Cohort. 
Birth Date Confidence | 3 character string with positional characters representing Year, Month, and Day (YMD) | As birth date may not be known with absolute precision, this indicator specifies the confidence with which the date is known. The Birth Date Confidence Indicator is a variation on the Date Accuracy Indicator used by the Australian Institute of Health and Welfare<sup id="AIHW">[4](#f4)</sup>, adjusted to match the format of ISO dates (YMD). It is a 3 character string with positional characters representing Year, Month, and Day (YMD). Character values = A (accurate), E (estimated), U (unknown) (e.g. “AEU”).
Birth Rank | Positive Integer, 0 if NULL. | A value describing the number of progeny born to the same dam in the same birth event; values are 0 if NULL, 1 if the animal is a singleton, 2 if it is one of twins, etc. Typical values are 0-5, or 0-2 for cattle.
Birth Cohort| Integer cohort number (2 digits) | The contemporary group or cohort that describes the season (spring/autumn) within the birth year into which animals are categorised. This is most likely derived or calculated from the birth date. As seasons vary around the world (including variations with 2, 4, 6, or 12 cohorts), a cohort number is used to interchange this data.|
Birth Year | Integer year (1900 to 2100 or a subset thereof). | The contemporary group or cohort for the year of birth into which animals are categorised. Known as Year Born in many systems. This is a derived field, calculated from the Birth Date where available. It is included here as some systems interchange this data. Note that in some occasional circumstances, this may be different by 1 from the year component of the birth date (e.g. an animal born early in the northern hemisphere or late in the southern hemisphere).
Pre-Birth Mob | Integer | Mob ewe prior to lambing.
Post Birth Mob | Integer | Mob ewe post lambing.
Sex | Enumeration: Male, Female, NULL | The gender or sex of the animal. This may be combined with state information to indicate the fertility status of the animal. 
Breed Assessed | String based upon breed list. | A visual assessment of the animal’s primary or major breed. In many systems, this is simply called “Breed”.  There is no internationally recognised master list of livestock breeds. [ICAR](ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) mandates a list of codes for bovine semen straws<sup id="ICAR">[5](#f5)</sup>, and Oklahoma State University publishes a useful list of livestock breeds<sup id="OKSB">[6](#f6)</sup>. The UN Food and Agriculture Organisation (FAO) maintains a database of all domestic livestock breeds<sup id="FAODAD">[7](#f7)</sup>. Current [List of Breeds](http://www.farmdatastandards.org.nz/animal-breed-list/).
Breeds | Array of breed names and breed proportion (in terms relative to the Breed Distribution Denominator, “Sixteenths”, “Sixty-fourths”, or “Percentage”), e.g. Friesian 8, Jersey 8 | A two-dimensional matrix of breed identifiers and the proportion of each breed in the animal (calculated from its parent’s breed components). [SIL](ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) currently uses percentages, and the NZ Dairy Databases use 16ths. We have also seen systems use 64ths. See also: Breed Assessed.
Breed Distribution Denominator | Enumeration: 16, 64, 100 | The basis for the proportion of each breed expressed in the Breed Distribution.
Breed SocSE Code | String | Breed Society Single Entry Code.
Breed Society Reg Status | Enumeration: N, R, NULL | Breed Society Registration Status.
Primary Breed Abbreviation | String | Primary breed of the animal in short form, i.e. “Rom” for Romney
Visual Colour | String | Visually assessed colour of the animal.
Species Binomial Name | String with common values. Only Genus is capitalised. | Combines Genus and Species (e.g. “Bos taurus” for cattle, “Ovis aries” for sheep, “Cervus elaphus” for red deer, “Cervus Canadensis” for elk wapiti, and “Capra aegagrus” for goats).
Species Common Name | Enumeration: Cattle, Deer, Goats, Sheep |  Describes the species in common terms (“Cattle”, “Deer”, “Goats”, “Sheep”).

#### Treatment Method
Treatment Method is used in the Treatment observation in the Animal Health category.

Valid values for Treatment Method |
:-------------------------------- |
Capsule|
Dip|
Oral Drench|
Feed additive|
Injection|
Pour-on|
Topical|
Tube|
Vaccine|

#### Procedure Type

Procedure Type is used in the Farming Procedure observation in the Animal Health category.

Valid values for Procedure Type |
:------------------------------ |
Branding |
Castration |
Crutching |
Cryptorchiding |
Dehorning |
Disbudding |
Shearing |
Tailing |


##### Footnotes

<b id="f1">1</b> [International Agreement of Recording Practices](https://www.icar.org/index.php/icar-recording-guidelines/), Guidelines approved by the General Assembly of the International Committee for Animal Recording – ICAR, June 2012.
 [↩](#IARP)
 
<b id="f2">2</b> [Search the ACVM Register](https://eatsafe.nzfsa.govt.nz/web/public/acvm-register) or view the [entire register](http://www.nzfsa.govt.nz/images/acvm/RegisteredRegistrations.csv),  Ministry for Primary Industries Online. [↩](#ACVM)

<b id="f3">3</b> [Surgical Procedures](https://www.acvs.org/sites/default/files/files/Residency/Procedures/LA_Surgical_Procedures_9_13_2018.pdf), American College of Veterinary Procedures, 2012. [↩](#ACVS)

<b id="f4">4</b> [Date Accuracy Indicator](http://meteor.aihw.gov.au/content/index.phtml/itemId/294429) – Australian Institute of Health and Welfare. [↩](#AIHW)

<b id="f5">5</b> [ICAR Guidelines 2012](https://interbull.org/ib/icarbreedcodes), Section 8 Annex 1, pp 479-481, Breed Codes on Bovine Semen Straws for International Trade assigned by ICAR Sub-committee Interbull, International Committee for Animal Recording.   [↩](#ICAR)

<b id="f6">6</b> [Oklahoma State University Livestock Breeds](http://www.ansi.okstate.edu/breeds/). [↩](#OKSB)

<b id="f7">7</b> [FAO Domestic Animal Diversity Information System](http://www.fao.org/dad-is/data/en/). [↩](#FAODAD)
