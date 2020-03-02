### Test (excluding Dairy Herd Tests) Observations

Contents:
* [Blood tests](#Blood-tests)
* [Liver Biopsy](#Liver-Biopsy)
* [CT-scan](#CT-scan)
* [MIR](#MIR)
* [Gene sample](#Gene-sample)


#### Blood tests

Records details of blood tests.

Attribute | Data Type | Notes 
:-------- | :-------- | :----
Blood Test Type | Enumeration | See [Blood Test Type](#Blood-Test-Type).
Blood Test Result | Floating |
Blood Test Units | Enumeration | %, x103/µL, x106/µL, x109/µL, mg/dL, g/dL, g/L

#### Liver Biopsy

Records details of liver tests.

Attribute | Data Type | Notes 
:-------- | :-------- | :----
Liver test type | Enumeration | See [Liver Test Type](#Liver-Test-Type).
Liver Test Result | Floating |
Liver Test Units | Enumeration | U/L, mg/dL, g/dL
	
#### CT-scan

Records details of CT-scan. Used to study fundamental vibrations and rotational-vibrational structures associated with them, typically using an infrared spectrometer.

Attribute | Data Type | Notes 
:-------- | :-------- | :----
CT-Scan Result | Array | 
	
#### MIR

Records details of MIR scan. Mid Infrared spectroscopy is used to evaluate analyse chemical data using electromagnetic spectrum as wavelengths between ~2.5 - 10µm.	

Attribute | Data Type | Notes 
:-------- | :-------- | :----
MIR Result | Array |
	
#### Gene sample

Records details of DNA tests.

Attribute | Data Type | Notes 
:-------- | :-------- | :----
DNA Test Type | Enumeration | See [DNA Tests](#DNA-Tests).
DNA Test Sample Type | Enumeration | See [DNA Tests](#DNA-Tests).
Recessive Gene condition | String |
DNA Test Result | String |

##### Blood Test Type

Blood Test Type is used in the Blood Tests observation in the Tests (excluding Herd Tests) category.

Valid values for Blood Test Type |
:------------------------------- |
β-hydroxybutyrate |
glucose |
non-esterified fatty acid |
urea-nitrogen |
albumin |
globulin |
magnesium |
inorganic phosphate |
copper |
GSHPx |
calcium |
thyroxine T4 |
vitamin A |
vitamin B12 |
vitamin E |
leptospira |
BVD |
IBR antibodies |
PII |

##### Liver Test Type

Liver Test Type is used in the Liver Biopsy observation in the Tests (excluding Herd Tests) category.

Valid values for Liver Test Type |
:------------------------------- |
alanine transaminase (ALT) |
aspartate transaminase (AST) |
alkaline phosphatase (ALKP) |
total bilirubin (Tot BILI) |
albumin (ALB) |
blood-urea-nitrogen (BUN) |
copper | 
cobalt |
selenium |

##### DNA Tests

The Gene Sample observation in the Tests (excluding Herd Tests) category uses the following:

Valid values for DNA Test Type |
:----------------------------- |
Carrier of Recessive Gene |
DNA match |
Identity |
marker-assisted selection |
Pedigree verification |
Sire/dam match |
 

Valid values for DNA Test Sample Type |
:------------------------------------ |
Blood |
Hair |
Milk |
Semen |