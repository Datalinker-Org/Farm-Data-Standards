### Livestock Enterprises (Herds)

Contents:
* [Enterprise Identification and Attributes](#Enterprise-Identification-and-Attributes)
* [Organisation Supply Details](#Organisation-Supply-Details)
* [Dairy Herd additional details](#Dairy-Herd-additional-details)
* [Sheep, beef, or deer additional details](#Sheep,-beef,-or-deer-additional-details)

The following table defines items in entities that apply to livestock **enterprises**. Enterprises may be further defined by a **Stock Reconciliation** for the entire period being evaluated, or a monthly stock reconciliation for each month of the period being evaluated.

#### Enterprise Identification and Attributes
([All enterprises](https://github.com/Datalinker-Org/Farm-Data-Standards/blob/master/Stock%20Reconciliation/README.md))

Attributes | Data Types | Notes
:--------- | :--------- | :----
Herd Name | String | Name of the enterprise within the farm.
Identifier(s) | [URN](FMDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) | One or more herd or flock identifiers using URN notation. See [Herd and Flock Identification](FMDS_Identification-of-Locations-and-Herds.md#Herd-and-Flock-Identification).
Species Binomial Name | String | Combines Genus and Species; “Bos taurus” - cattle, “Ovis aries” - sheep, “Cervus elaphus” - red deer, “Cervus Canadensis” - elk wapiti, “Capra aegagrus” - goats.
Species Simple Name | Enumeration | Describes the species in common terms; Cattle, Deer, Goats, Sheep.
Use	| Enumeration | Describes the purpose of the enterprise the animals belong to: Dairy, Stud, Grazing, Breeding, Finishing, Meat, Fibre, Velvet.
Breed Assessed | String | There is no internationally recognised master list of livestock breeds. [ICAR](FMDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) mandates a list of codes for bovine semen straws<sup id="Bovine">[1](#f1)</sup>, and Oklahoma State University publishes a useful list of livestock breeds<sup id="OKSB">[2](#f2)</sup>. The UN Food and Agriculture Organisation (FAO) maintains a database of all domestic livestock breeds<sup id="FAODAD">[3](#f3)</sup>. A list of breeds suitable for use with New Zealand farmed livestock will be maintained at [here](https://github.com/Datalinker-Org/Farm-Data-Standards/blob/master/FarmDataStandards_Animal-Breed-List.md).

#### Organisation Supply Details

(Repeated as necessary for all enterprises)	

Attributes | Data Types | Notes
:--------- | :--------- | :----
Customer Name | | Name of Dairy or Meat Processor.
Supply Type | Enumeration | Milk, Meat, Fibre, Other.
Supply Number(s) | Integer | One or more company-specific supply numbers as defined by [isicV4](http://unstats.un.org/unsd/cr/registry/isic-4.asp), e.g. meat co, 105 = dairy co, 131 = textile processor.

#### Dairy Herd additional details

Attributes | Data Types | Notes
:--------- | :--------- | :----
Dairy Business Model | Enumeration | Owner operator, 50-50 sharemilker, Variable order.
Calving season | Enumeration | Spring, Autumn, Spring and Autumn, Other.
Peak Cows Milked | Integer |
Herd Average Live Weight | Integer | kg
Herd Breeding Worth | Currency / % Reliability | The average Breeding Worth of the animals in the herd. Measures the ability to breed profitable replacements. Expresses the extra net farm income per year (per 5 tonnes of dry matter fed) relative to the current genetic base that will be passed on to progeny of the cows in the herd.  Reliability measures how much information has contributed to the trait evaluation for the animals.
Herd Production Worth | Currency / % Reliability | The average Production Worth of the animals in the herd. Measures the lifetime productive ability. Expresses the extra net farm income per year (per 5 tonnes of dry matter fed) relative to the current genetic base that will be produced by cows in this herd during their lifetime.  Reliability measures how much information has contributed to the trait evaluation for the animals.
Herd Lactation Worth | Currency / % Reliability | The average Lactation Worth of the animals in the herd. Measures the ability to convert feed into profit in the current season. Expresses the extra net farm income (per 5 tonnes of dry matter fed) that will be produced by this herd, relative to the current genetic base for the current season.  Reliability measures how much information has contributed to the trait evaluation for the animals.

#### Sheep, beef, or deer additional details

Attributes | Data Types | Notes
:--------- | :--------- | :----
Total RSU | Integer | Total revised stock units in this enterprise (having been calculated using the feed requirements of the animal numbers specified for the enterprise).
Breed Class	| Enumeration | Describes the purpose for the identified species; Dual Purpose, Fine Wool, Meat/Terminal, British, European.
Average Mature Weight | Float | Weight of mature breeding stock (cows, hinds, ewes) in kg.

#### Footnotes

<b id="f1">1.</b> [ICAR Guidelines 2012](https://interbull.org/ib/icarbreedcodes), Section 8 Annex 1, pp 479-481, Breed Codes on Bovine Semen Straws for International Trade assigned by ICAR Sub-committee Interbull, International Committee for Animal Recording. [↩](#Bovine)

<b id="f2">2.</b> [Oklahoma State University Livestock Breeds](http://www.ansi.okstate.edu/breeds/). [↩](#OKSB) 

<b id="f3">3.</b> [FAO Domestic Animal Diversity Information System](http://www.fao.org/dad-is/data/en/). [↩](#FAODAD) 
