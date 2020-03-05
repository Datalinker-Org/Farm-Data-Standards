### Derived Metrics

Contents:
* [Dairy Reproduction](#Dairy-Reproduction)
* [Sheep, Beef, or Deer Reproduction](#Sheep,-Beef,-or-Deer-Reproduction)
* [Dairy Mortality and Replacements](#Dairy-Mortality-and-Replacements)
* [Sheep, Beef, or Deer Mortality and Replacements](#Sheep,-Beef,-or-Deer-Mortality-and-Replacements)
* [Dairy Mastitis and Lameness](#Dairy-Mastitis-and-Lameness)
* [Milk Production](#Milk-Production)
* [Carcass Production](#Carcass-Production)
* [Wool and Velvet Production](#Wool-and-Velvet-Production)

Models and benchmarking applications frequently utilise enterprise or farm “attributes” that are in fact summarised or derived from actual observations of animals, mobs, or management actions. These vary by enterprise, so the table below is broken into sections by enterprise type and the sort of summary information concerned (for instance, reproduction, milk or meat production).

#### Dairy Reproduction	

Attributes | Data Types | Notes
:--------- | :--------- | :----
Start calving | [ISO Date](FMDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) | 
Number of cows calved | Integer
Date 50% calved	| [ISO Date](FMDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) | date when 50% of cows calved.
Number calves reared | Integer
Planned start of calving | [ISO Date](FMDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations)
Planned start of mating | [ISO Date](FMDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations)
Date AB finished | [ISO Date](FMDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations)
Date bull withdrawn	| [ISO Date](FMDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations)
Cows confirmed empty | Integer
Number cows calved at 21 days | Integer | Number cows calved 3 weeks from planned start of calving.
Number cows calved at 42 days | Integer | Number cows calved 6 weeks from planned start of calving.
Number |cNws calved at 63 days | Integer | Number cows calved 9 weeks from planned start of calving.
Number cows induced | Integer
Number cows submitted in 21 days from PSM | Integer | Number of cows submitted in 21 days from Planned Start of Mating.
Number cows treated for anoestrus | Integer
6 week in-calf rate | Integer | % of herd in calf at 6 weeks.

#### Sheep, Beef, or Deer Reproduction	

Attributes | Data Types | Notes
:--------- | :--------- | :----
Planned start of birthing | [ISO Date](FMDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) | Planned start of lambing or calving.
Start of birthing | [ISO Date](FMDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) | Actual start of lambing or calving.
Mean Birthing Date | [ISO Date](FMDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) | Mean lambing or calving date.
Mean Weaning Date | [ISO Date](FMDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) | 
Weaning weight | Float | Weight in kilograms.
Condition Score at Mating | Float | Average Condition Score (see Condition Score in the Animal Data Standard ).
Liveweight at Mating | Float | Average Liveweight
Hogget Liveweight at Mating	| Float | Average Liveweight of Hoggets mated.
Number Mated | Integer
Number Hoggets Mated | Integer
Number Pregnant	| Integer
Number Hoggets Pregnant	| Integer
Scanning Percentage	| Integer | %
Hogget Scanning Percentage | Integer | %
Birthing Percentage | Integer | % (calculated from number of live progeny / number of dams at mating).
Hogget Lambing Percentage | Integer | %
Weaning % | Integer | % (number of progeny weaned / number of dams at mating).
Number born | Integer
Number weaned | Integer

#### Dairy Mortality and Replacements	

Attributes | Data Types | Notes
:--------- | :--------- | :----
Number calves reared | Integer
Replacement Grazing	| Enumeration | Off-farm from weaning, Off-farm from 9 months, Always on farm
Replacement Rate | Integer | % annual replacement rate
Number cows start of season | Integer | Number of cows at start of season.
Number R2 heifers start of season | Integer |
Number R2 heifers end season | Integer | Number of R2 heifers at start of season and still in herd at end of season.
Number milking 1 Dec | Integer | Number of cows and R2 heifers milking at 1 Dec
Number replacement calves reared | Integer

#### Sheep, Beef, or Deer Mortality and Replacements

Attributes | Data Types | Notes
:--------- | :--------- | :----
Progeny Mortality | Float | %
Replacement Rate | Integer | % annual replacement rate in ewe flock or breeding cows


#### Dairy Mastitis and Lameness

Attributes | Data Types | Notes
:--------- | :--------- | :----
Cows lame | Integer | Number of cases of cows lame.
Cows treated mastitis | Integer | Number cows treated for mastitis in first 6 weeks from Planned Start of Calving.

#### Milk Production	

Attributes | Data Types | Notes
:--------- | :--------- | :----
Once-a-day milking | Enumeration | Never, Only at drying-off, Half of season, All season.
Winter milk | Boolean | Yes, No
Drying-off date | [ISO Date](FMDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations)
Days in milk per cow | Integer | Average days in milk for herd
Total milk solids | Integer | kg MS
Fat | Integer | Total fat, kg
Protein | Integer | Total protein, kg
Average bulk somatic cell count | Integer | Average bulk cell count for season.
Milk Volume | Integer | Total milk volume, litres.
Milk fed to calves | Integer | Total milk fed to calves, litres.
Discarded milk solids | Integer | kg
Peak daily milk solids | Integer | Average daily milk solids per cow for 10 days at peak, kg.
End of peak | ISO Date | Date of last day of 10 day peak.
Milk solids to 31 Dec | Integer | Milk solids to 31 Dec sold to factory, kg
Daily milk solids end Dec | Integer | Average daily milk solids per cow for last 10 days in Dec, kg

#### Carcass Production	

Attributes | Data Types | Notes
:--------- | :--------- | :----
Mean slaughter date | [ISO Date](FMDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations)
Mean slaughter age | Integer | days
Mean live weight at sale | Float | kg
Mean carcass weight	| Float | kg
Mean Dressing out % | Integer | %

#### Wool and Velvet Production	

Attributes | Data Types | Notes
:--------- | :--------- | :----
Velvet harvested | Integer | kg
Wool shorn | Integer | kg
