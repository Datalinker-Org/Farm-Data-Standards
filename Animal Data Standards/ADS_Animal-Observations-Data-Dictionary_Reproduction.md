### Reproduction Observations

Contents:
* [Run with Sires](#Run-with-Sires)
* [Observed Mating](#Observed-Mating)
* [Embryo Transfer](#Embryo-Transfer)
* [Egg Collection](#Egg-Collection)
* [Pregnancy Scan](#Pregnancy-Scan)
* [Semen Collection](#Semen-Collection)
* [Parturition](#Parturition)

#### Run with Sires

Records that a female (or group of females) was run with one or more sires for the purpose of mating, but is not an observation of actual mating. The observation date is the start of running the sires and dams together.	

Attribute | Data Type | Notes
:-------- | :-------- | :----
Sire Identifier(s) | [URN](ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) | A list of URN animal identifiers for the sires, if these are known.
Sire Tally | Integer | The number of sires.
Dam Tally | Integer | The number of dams.
Dam Ratio | Float | The ratio of dams per sire.
Teaser Used | Boolean | True if a teaser was used.
Intended Exit Date | [ISO](ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) 8601 | Date of intended separation of sires and dams.

#### Observed Mating

Record of a mating that was observed, which might include observed natural mating, artificial insemination, and AI with sexed semen (all differentiated by Mating Method).

Attribute | Data Type | Notes
:-------- | :-------- | :----
Mating Method | Enumeration | Natural, AI, Sexed Semen AI. 
Artificial Insemination Sire Identification | URN | Animal identifier of sire. May be called Bull Identification.
Straw Identifier | String | Identifier of the straw. [ICAR](ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) identifier preferred.

#### Embryo Transfer

The act of implanting a fertilised embryo, typically from another donor.

Attribute | Data Type | Notes
:-------- | :-------- | :----
Embryo Donor Identification | [URN](ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) | Animal identifier of the dam from whom oocytes were harvested.
Embryo Sire Identification | [URN](ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) | Animal identifier of the sire.
Embryo Recipient Identification | [URN](ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) | Animal identifier of the recipient dam.
Embryo Implant Serial Number | String | Identifier of the embryo.

#### Egg Collection

The act of collecting oocytes or eggs from a donor dam.	

Attribute | Data Type | Notes
:-------- | :-------- | :----
Collection Identifier | String | Collection identifier.
Collection Centre Identifier | String | Identifies the collection centre. 
Oestrous Day | Integer | Day within oestrous cycle.

#### Pregnancy Scan

Also called “scanning” (although that term could refer to other scans), this is the process of determining pregnancy, and possibly the number of foetuses and foetal age. In the case of sheep, short scanning identifies empty, single, and multiple, rather than counting all multiple embryos.

Attribute | Data Type | Notes
:-------- | :-------- | :----
Scan type | Enumeration | Short, Long. 
Equipment Model | String | Make and model of equipment used.
Foetus Count | Integer | Number of foetuses (may be zero).
Foetal age | Integer | Gestation age in days where estimated.

#### Semen Collection

The act of collecting semen from a sire.

Attribute | Data Type | Notes
:-------- | :-------- | :----
Collection Identifier | String | Collection identifier.
Collection Centre Identifier | String | Identifies the collection centre.
Semen pH | Float | Values between 3 and 9. 
Semen Volume | Float | The volume of semen in millilitres (ml).
Semen Motility | Float |
Forward Progression | String | Score from 0 to 4, with + or – postfix.
Semen Concentration | Float | Expressed as 106/ml.
Semen Morphology | Float | Percentage of sperm with normal morphology.
White Blood Cell Count | Float | Expressed as 106/ml. 

#### Parturition

Also called Birthing, this is a cross-species term for calving, lambing, or fawning.

Attribute | Data Type | Notes
:-------- | :-------- | :----
Parturition Actual Date Indicator | Enumeration | Actual, estimated.
Abnormal Birth Indicator | Enumeration | Aborted, induced, premature. 
Assistance Indicator | Enumeration | Not reported, reported no assistance, minor assistance, major assistance.
Number of Progeny | Integer | Count of progeny.
Progeny Number | Integer | Ascending number allocated to each progeny recorded within a parturition observation.
Fate of Progeny | Enumeration | See [Animal Fate Reasons](#Animal-Fate-Reasons) (for each progeny recorded within a parturition observation). 
Progeny Animal ID | [URN](ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) | Animal identification of each progeny where this has been recorded during a parturition observation.
Progeny Sex | Enumeration | Male, Female (for each progeny recorded within a parturition observation).
Progeny Comment | String | See [Progeny Comment](#Progeny-Comment).

##### Animal Fate Values

Animal Fate is specified in both the Change Fate observation (in Registration) and for progeny in the Parturition observation (in Reproduction). Some codes are specific to one of these observations. The relevant context for each code is given below.  

Valid values for Fate Code are:

Fate Value | Used in observation(s):
:--------- | :----------------------
Alive | Change Fate.
Culled | Change Fate; Parturition.
Dead | Change Fate; Parturition.
Grazing Off | Change Fate.
Grazing On | Change Fate.
Lost | Change Fate.
Sold | Change Fate; Parturition.
In Transit | Change Fate.
Reared | Parturition.
Bobbied | Parturition.

##### Progeny Comment (Dairy)
Progeny Comment is used in the Parturition observation in the Reproduction category.

Valid values for Progeny Comment |
:------------------------------- |
aborted |
born dead – birthing difficulty |
bowel or intestine abnormality |
brain damaged/retarded/spastic |
breathing difficulties |
cleft palate |
complex vertebral malformation | 
died after 4 days |
died not due to birthing |
died within 1-4 days |
difficult to rear won’t drink |
estimated birth date |
extra teats |
hernia |
induced |
malpresentation/breech |
mulefoot |
mummified |
other deformity – extra/missing limbs |
paralysed legs |
polled |
premature |
red factor |
scours |
short jaw |
spinal deformity |
still born | 
swollen joints |
tail deformity/no tail |
too large |
twisted feet |
weak and/or small |
