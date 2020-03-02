### Fibre Production Observations

Contents:
* [Shearing](#Shearing)
* [Fibre Measurements](#Fibre-Measurements)


#### Shearing

Record of the fact that an animal was shorn, and optionally, fleece weight and lab sample ID.

Attribute | Data Type | Notes 
:-------- | :-------- | :----
Fleece Weight | Float | Weight of the shorn fleece in kilograms.
Sample Identifier | String | Identifier of sample sent away for processing.

#### Fibre Measurements

Laboratory measured fibre characteristics.

Attribute | Data Type | Notes 
:-------- | :-------- | :----
Sample Identifier | String | Identifier of sample.
Laboratory Identifier | String | Unique identifier for the laboratory which processed a sample. 
Yield Percentage | Float | Yield of clean fibre.
Staple Length | Integer | The length of wool staple in mm from a wool laboratory test.
Mean Fibre Diameter | Float | Mean diameter of fibres in the sample in micrometres (microns).
Fibre Diameter Standard Deviation | Float | The standard deviation of diameter of fibres in the sample. 
Fibre Diameter Coefficient of Variation | Float | The coefficient of variation of diameter of fibres in the sample.
Spinning Fineness | Integer | Measure or score of the fineness of wool for spinning, from a lab test.
Prickle Factor | Integer | Measurement or score of the prickle factor of wool, from a lab test.
Comfort Factor | Integer | Score of the comfort level of a wool from a testing laboratory.
