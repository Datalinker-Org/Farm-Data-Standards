### Animal Lifecycle Data Dictionary (Normative)

Contents:
* [Animal Life](#Animal-Life).
* [Animal Parentage](#Animal-Parentage).
* [Animal State](#Animal-State).

#### Animal Life

The following table defines items categorised as Animal Life Data that typically do not change over the lifetime of the animal.

Attributes | Data Type | Description
:--------- | :-------- | :----------
Birth Date | [ISO](docs/ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) 8601 Date | The date on which an animal was born. See also: Birth Date Confidence, Birth Year, Birth Cohort. 
Birth Date Confidence | 3 character string with positional characters representing Year, Month, and Day (YMD) | As birth date may not be known with absolute precision, this indicator specifies the confidence with which the date is known. The Birth Date Confidence Indicator is a variation on the Date Accuracy Indicator used by the Australian Institute of Health and Welfare[^AIHW], adjusted to match the format of ISO dates (YMD). It is a 3 character string with positional characters representing Year, Month, and Day (YMD). Character values = A (accurate), E (estimated), U (unknown) (e.g. “AEU”).
Birth Rank | Positive Integer, 0 if NULL. | A value describing the number of progeny born to the same dam in the same birth event; values are 0 if NULL, 1 if the animal is a singleton, 2 if it is one of twins, etc.   Typical values are 0-5, or 0-2 for cattle.
Birth Cohort| Integer cohort number (2 digits) | The contemporary group or cohort that describes the season (spring/autumn) within the birth year into which animals are categorised. This is most likely derived or calculated from the birth date. As seasons vary around the world (including variations with 2, 4, 6, or 12 cohorts), a cohort number is used to interchange this data.|
Birth Year | Integer year (1900 to 2100 or a subset thereof). | The contemporary group or cohort for the year of birth into which animals are categorised. Known as Year Born in many systems. This is a derived field, calculated from the Birth Date where available. It is included here as some systems interchange this data. Note that in some occasional circumstances, this may be different by 1 from the year component of the birth date (e.g. an animal born early in the northern hemisphere or late in the southern hemisphere).
Pre Birth Mob | Integer | Mob ewe prior to lambing.
Post Birth Mob | Integer | Mob ewe post lambing.
Sex | Enumeration: Male, Female, NULL | The gender or sex of the animal. This may be combined with state information to indicate the fertility status of the animal. 
Breed Assessed | String based upon breed list. | A visual assessment of the animal’s primary or major breed. In many systems, this is simply called “Breed”.  There is no internationally recognised master list of livestock breeds. [ICAR](docs/ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) mandates a list of codes for bovine semen straws[^BovineSemen], and Oklahoma State University publishes a useful list of livestock breeds[^OKStateBreeds]. The UN Food and Agriculture Organisation (FAO) maintains a database of all domestic livestock breeds[^FAODAD]. Current [List of Breeds](http://www.farmdatastandards.org.nz/animal-breed-list/).
Breeds | Array of breed names and breed proportion (in terms relative to the Breed Distribution Denominator, “Sixteenths”, “Sixty-fourths”, or “Percentage”), e.g. Friesian 8, Jersey 8 | A two-dimensional matrix of breed identifiers and the proportion of each breed in the animal (calculated from its parent’s breed components). [SIL](docs/ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) currently uses percentages, and the NZ Dairy Databases use 16ths. We have also seen systems use 64ths. See also: Breed Assessed.
Breed Distribution Denominator | Enumeration: 16, 64, 100 | The basis for the proportion of each breed expressed in the Breed Distribution.
Breed SocSE Code | String | Breed Society Single Entry Code.
Breed Society Reg Status | Enumeration: N, R, NULL | Breed Society Registration Status.
Primary Breed Abbreviation | String | Primary breed of the animal in short form, i.e. “Rom” for Romney
Visual Colour | String | Visually assessed colour of the animal.
Species Binomial Name | String with common values. Only Genus is capitalised. | Combines Genus and Species (e.g. “Bos taurus” for cattle, “Ovis aries” for sheep, “Cervus elaphus” for red deer, “Cervus Canadensis” for elk wapiti, and “Capra aegagrus” for goats).
Species Common Name | Enumeration: Cattle, Deer, Goats, Sheep |  Describes the species in common terms (“Cattle”, “Deer”, “Goats”, “Sheep”).

#### Animal Parentage
The following table defines items categorised as Parentage, and which link animals genetically. As with animal characteristics, these do not change over the lifetime of the animal but may become better known (for instance, as the result of a DNA test).
Attributes | Data Type | Description
:--------- | :-------- | :----------
Parent Age | Null if unknown, or integer values 1 to 25 | The calculated age of the parent in years at the time at which the animal was born (based on the birth date or birth year of the animal and the birth date or birth year of the parent). This is used as “Age of Dam”, an adjustment factor in some systems.
Parent Type | Enumeration | This specifies the type of parentage that is claimed:<ul><li>Dam (natural dam)</li><li>ET Recipient Dam</li><li>ET Donor (Genetic) Dam</li><li>Rearing Dam (reared, but did not give birth to the progeny)</li><li>Sire (multiple sire records may be recorded, each with its own DNA probability if DNA testing indicates multiple matches)</li><li>Excluded Sire (unable to confirm the sire, but definitely not this animal).</li></ul>
Parentage Method | Enumeration: Observed, Associated, Derived, or DNA. | Documents how parentage was assessed: <ul><li>Observed (e.g. Dam observed giving birth to progeny)</li><li>Associated (e.g. Dam seen feeding progeny)</li><li>Derived (e.g. Sire derived from mating records)</li><li> DNA (the result of a DNA parentage test).</li></ul>
Survive to Weaning | Boolean: 0,1 | Used to determine whether the progeny was recorded as having survived through to weaning.
Birth Dam ID | Array: [URN](docs/ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) identifier of animal. | The Animal ID of the Dam as determined at birth, using the Animal identifiers outlined in [Animal Identification](docs/ADS_Identification-of-Animals-Herds-and-Locations.md#Animal-Identification) The parentage properties of an animal can be comprised of a set of elements, including the birth dam, genetic dam, rearing dam, and sireId.
Genetic Dam ID | Array: [URN](docs/ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) identifier of animal. | The Animal ID of the Dam as determined from Genetic evaluation, using the Animal identifiers outlined in [Animal Identification](docs/ADS_Identification-of-Animals-Herds-and-Locations.md#Animal-Identification) The parentage properties of an animal can be comprised of a set of elements, including the birth dam, genetic dam, rearing dam, and sireId.  
Rearing Dam ID | Array: [URN](docs/ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) identifier of animal. | The Animal ID of the Dam as determined from rearing, using the Animal identifiers outlined in [Animal Identification](docs/ADS_Identification-of-Animals-Herds-and-Locations.md#Animal-Identification) The parentage properties of an animal can be comprised of a set of elements, including the birth dam, genetic dam, rearing dam, and sireId. 
Sire ID | Array: [URN](docs/ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) identifier of animal.  | The Animal ID of the Sire, using the Animal identifiers outlined in [Animal Identification](docs/ADS_Identification-of-Animals-Herds-and-Locations.md#Animal-Identification) The parentage properties of an animal can be comprised of a set of elements, including the birth dam, genetic dam, rearing dam, and sireId.

#### Animal State

The following table defines Animal State items that may change over the lifetime of the animal. Some items change many times, while others may only change once. All animal states could be adequately represented as the result of a set of observations, and hence it would be technically possible to do without state information.

However, the ability to interchange state information is important because:

* Many systems, particularly field devices, need to display or act on state information, without having the storage space or processing power to manage all events that resulted in that state; and

* In some data sets (particularly older data), the actual observations that drove a state change are not available (for example, the date on which a male sheep was wethered is unknown), so the current state is the only available representation.  

Attributes | Data Type | Description 
:--------- | :-------- | :----------
Current Location | [URN](docs/ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) String | Location identifier that describes the current location at which the animal is living, or the last location at which it was alive, using a URN-based identification string which contains the namespace and unique identifier within that namespace. An example for the [MPI](docs/ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) Farms Online system might be “nzl:farm:farmsonline:WK-3284-0046”.
Disposal Method | Enumeration: Home Kill, Disposed at [NAIT](docs/ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) Location, Meat processor – human consumption, Meat processor – pet food, Rendering facility. | Indicates the disposal method for an animal that is dead. This may be Null if the animal is alive or disposal method is unknown.
Current Status | Enumeration: NULL, Alive, Dead, In Transit, Culled, Sold, Grazing Off, Grazing On, Lost, Reared, Bobbied | Also known as “fate”, this field is typically used to describe if the animal is Alive or Dead, sometimes with other variants such as Culled and Sold, although these may be more problematic if exchanging details between systems (for instance, sold on one system, but arriving and alive on another system). The reason for the Fate (for instance, culled) should be recorded as an observation.
Fertility Status | Enumeration: Unknown, Fertile, Infertile, Neutered, Cryptorchid | Indicates whether an animal is known to be fertile or note, or whether it has been partly or fully neutered. For instance, a neutered cattle male is a steer, a neutered sheep male is a wether. Females of both species can be spayed. An infertile male by comparison still has testes and responds as a male, and is frequently used as a “teaser”.
Lactating | Boolean: True or False, or may be Null if unknown. | Indicates whether the animal is lactating at the time of data transfer. Note that this state may change a number of times over an animal’s lifetime.
Rearing Rank | Integer: Null or values 0 to 12. | Rearing rank is used to indicate the number of progeny reared by the same dam during the same lactation as this has an influence on weights and growth rates. For example, an animal reared as a twin will have a rearing rank of 2. May be Null if unknown, or 0 if born dead.  
Reproductive Status | Enumeration: Unknown, Cycling, Not Cycling, Pregnant, Involuting. | Indicates whether the animal is pregnant at the time of data transfer. Note that this state may change a number of times over an animal’s lifetime. 
Status Date | [ISO](docs/ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) Date; May be Null | Date the status or fate last changed.
Stock Class Name | String | Name of the stock class the animal currently belongs to, e.g. R1 Bull, R2 Bull.
Withholding Date Meat | [ISO](docs/ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) Date; May be Null | Due to health treatments, the animal may not enter the food supply chain until this date. Derived from health treatment events.
Withholding Date Milk | [ISO](docs/ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) Date; May be Null | Due to health treatments, milk from the animal may not enter the food supply chain until this date. Derived from health treatment events.
Withholding Date Export | [ISO](docs/ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) Date; May be Null | Date resulting from export slaughter interval of a treatment.


#### Footnotes 

[^AIHW]: [Date Accuracy Indicator](http://meteor.aihw.gov.au/content/index.phtml/itemId/294429) – Australian Institute of Health and Welfare.  

[^BovineSemen]: [ICAR Guidelines 2012](https://interbull.org/ib/icarbreedcodes), Section 8 Annex 1, pp 479-481, Breed Codes on Bovine Semen Straws for International Trade assigned by ICAR Sub-committee Interbull, International Committee for Animal Recording.  .  

[^OKStateBreeds]: [Oklahoma State University Livestock Breeds](http://www.ansi.okstate.edu/breeds/).

[^FAODAD]: [FAO Domestic Animal Diversity Information System](http://www.fao.org/dad-is/data/en/).
