### Components of Land Application Data Interchange

Contents:
* [Application Information](#Application-Information)
* [Product Information](#Product-Information)

This standard addresses interchanges of data related to:

1.	Details supporting planning and ordering the application, or reporting on a completed application;

2.	Details of the products (to be) applied; and 

3.	Spatial representations of the geographic features affected by the application.

#### Application Information

[Application Information](docs/LADS_Land-Applications-Data-Dictionary.md#Application-Information) defines details of the order for an application of fertiliser, herbicide or pesticide and details about the spreading of the application. 

The order information identifies the customer and the planned and actual dates of the application.

The spreading information may identify the operator and the equipment used; information about the area spread and the distance covered while spreading; and the application rate. 

#### Product Information

One spreading job SHALL have one or more associated products.  A product [MAY](docs/LADS_Definitions-and-Abbreviations_Interpretation.md#Interpretation) be a mix or a standard stock-keeping unit ([SKU](docs/LADS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations)).

[Product Information](docs/LADS_Land-Applications-Data-Dictionary.md#Product-Information) defines each of the products planned or used, its application rate, the total quantity applied and the percentage of the product in the mix.

For fertiliser products, the nutrient concentrations [MAY](docs/LADS_Definitions-and-Abbreviations_Interpretation.md#Interpretation) be defined. 
