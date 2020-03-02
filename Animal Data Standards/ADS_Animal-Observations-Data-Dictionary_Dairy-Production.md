### Dairy Production Observations

Contents:
* [Milking](#Milking)
* [Milk Yield](#Milk-Yield)
* [Drying Off](#Drying-Off)
* [Milk Characteristics](#Milk-Characteristics)
* [Herd Test](#Herd-Test)

#### Milking

Records that an animal was present at milking and was milked.

Attribute | Data Type | Notes 
:-------- | :-------- | :----
Present at milking | Flag (True/False) |
Milked | Flag (True/False) |
	
#### Milk Yield

Records the yield of milk from an animal at a single milking.

Attribute | Data Type | Notes 
:-------- | :-------- | :----
Measurement Method | Enumeration |  Device or process used to measure milk yield. 
Yield Precision | Float | Degree of precision of the measurement.
Yield (Litres) | Float | Milk yield in litres. 
	
#### Drying Off

Also called “End Lactation”, this marks the point from which an animal will no longer be milked in the current lactation. It may also be accompanied by animal health treatments.

Attribute | Data Type | Notes 
:-------- | :-------- | :----
Drying Off Reason | Enumeration | See [Drying Off Reason](ASD_AppendixB_DairyProduction.md#Drying-Off-Reason).
Lactation End Date | Date |

#### Milk Characteristics

Captures characteristics of an animal’s milk (for instance, from a herd test or inline). Recorded against individuals.

Attribute | Data Type | Notes 
:-------- | :-------- | :----
Milk Measurement Method | Enumeration |
Sample Identifier | String | Identifier of sample sent away for processing.
Laboratory Identifier | String | Unique identifier for the laboratory that processed the sample.
Fat Percentage | Float | Percentage of fat in milk.
Protein Percentage | Float | Percentage of protein in milk.
Lactose Percentage | Float | Percentage of lactose in milk.
Somatic Cell Count | Float | Recorded in thousands of cells per ml of milk and is taken at each herd test (i.e., actual cell count divided by 1000).
Conductivity | Float | Conductivity of the milk in mS/cm.

#### Herd Test

Records that a milking monitored as part of an occasional (batch or DSM) herd test occurred. Must be recorded against individuals.

_Herd Test observations have been normalised against the requirements of the Dairy Herd Testing Standards (NZS8100) and the Dairy Industry Good Animal Database ([DIGAD](docs/ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations)), as NZ dairy herd testing is required to use this mechanism._

Attribute | Data Type | Notes 
:-------- | :-------- | :----
Milking Number | Integer | Indicates the number of the milking within the herd test (for instance, the first or second milking).
AM/PM Indicator | Enumeration | am, pm; Indicates whether the milking measured represents a morning or afternoon milking using traditional batch milking methodology.
Pretest Milking Date Stamp | [ISO](docs/ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) 8601 | Date (and time): the date and time of the immediate previous milking, in herd tests.
Milking Interval | Integer | In distributed milking systems the time between this observation and the previous milking; hours.
Herd Test Valid Indicator | Integer: | 0 = Valid <br> 1 = Not valid
Sample Regime Type Code | Integer: | 1 = Twice a day (am & pm) <br> 2 = Single sample-AM (>= 2 milkings) <br> 3 = Single sample-PM (>= 2 milkings) <br> 4 = Once a day
Average Number of Milkings | Float | Average number of times that an animal is milked expressed in terms of a 24-hour period at the time of the herd test sample milking.
Abnormal Test Type Code | Enumeration | See [Abnormal Dairy Herd Test Type Code](ASD_AppendixB_DairyProduction.md#Abnormal-Dairy-Herd-Test-Type-Code).
Sample Identifier | String | Identifier of sample sent away for processing.

##### Drying Off Reason

Drying Off Reason is used in the Drying Off observation in the Dairy Production category.

Valid values for Drying Off Reason |
:--------------------------------- |
eczema |
end lactation |
injured |
farm management |
mastitis |
other causes |
other diseases |
sick |
 
##### Abnormal Dairy Herd Test Type Code

Abnormal Test Code is used in the Herd test observation in the Dairy Production category.

Valid values for Abnormal Test Code:
Code | Description
:--- | :----------
1 | Insufficient sample
2 | Farm anomaly
3 | Animal in season
4 | Animal held milk
5 | Herd tester processing anomaly
6 | Irregular milk volume
7 | Animal running with calves
8 | Animal sick
9 | Contaminated sample
10 | Meter faulty
