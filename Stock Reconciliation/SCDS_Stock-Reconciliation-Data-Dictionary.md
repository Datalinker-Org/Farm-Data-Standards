### Stock Reconciliation Data Dictionary (Normative)

1. [Enterprise](#Enterprise)
2. [Class Attributes](#Class-Attributes)
3. [Transaction](#Transaction)
4. [Identifiers](#Identifiers)

#### Enterprise

This item describes the attributes of an enterprise.

Attributes or Fields | Data Types | Notes
:------------------- | :--------- | :----
Type | Enumeration | Describes the type of enterprise the animals belong to; Own Stock, Finishing, Contract Grazing.
Date | [ISO 8601 Date](SCDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) | Date.
Use | Enumeration | Describes the use of the enterprise the animals belong to; Stud, Commercial.
Owner | String | Describes the person who owns the animals and/or the enterprise.

#### Class Attributes

This item describes the attributes expected of animals in this stock class. Each of the elements are optional, with Species, Sex, and Birth Date most commonly used.	

Attributes or Fields | Data Types | Notes
:------------------- | :--------- | :----
Date | [ISO 8601](SCDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) Date | Date.
Species Binomial Name | String | See [Species](SCDS_Lists-of-Valid-Values.md#Species).
Species Simple Name | Enumeration | Describes the species in common terms; see [Species](SCDS_Lists-of-Valid-Values.md#Species).
Breed Assessed | String | Description of a genetic package
Breed Class | Enumeration | Describes the purpose for the identified species; Dual Purpose, Fine Wool, Meat/Terminal. 
Birth Date | [ISO 8601 Date](SCDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) | Date: Describes the date on which an animal was born; 
Birth Date Confidence | String | As birth date may not be known with absolute precision, this indicator specifies the confidence with which the date is known. This standard uses a variation on the Date Accuracy Indicator used by the Australian Institute of Health and Welfare<sup id="DAI">[1](#f1)</sup>, adjusted to match the format of ISO dates ([YMD](SCDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations)); 3 character string with positional characters representing Year, Month, and Day ([YMD](SCDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations)). Character values = A (accurate), E (estimated), U (unknown) (e.g. “AEU”)
Sex	| Enumeration | Describes the gender or sex of the animal; Male, Female.
Reproductive Status | Enumeration | Describes whether an animal is pregnant at the time of stock reconciliation; see [Reproductive Status](SCDS_Lists-of-Valid-Values.md#Reproductive-Status).
Fertility Status | Enumeration | Describes whether an animal is known to be fertile or not, or whether it has been partly or fully neutered;  see [Fertility Status](SCDS_Lists-of-Valid-Values.md#Fertility-Status).

#### Transaction

This section describes the types of transactions related to stock reconciliation and the details of those transactions.

Attributes or Fields | Data Types | Notes
:------------------- | :--------- | :----
Transaction Category | Enumeration | Describes the category of stock reconciliation transaction; see [Transaction Category and Type](SCDS_Lists-of-Valid-Values.md#Transaction-Category-and-Transaction-Type).
Transaction Type | Enumeration | Describes the sub-type of stock reconciliation transaction; see [Transaction Category and Type](SCDS_Lists-of-Valid-Values.md#Transaction-Category-and-Transaction-Type).
Date of transaction	Date | [ISO 8601](SCDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) Date | Transaction date, Balance date or Opening date of the transaction period depending on Transaction Category
Closing Date | [ISO 8601](SCDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) Date| Date: Closing Date of the transaction period (if relevant)
Quantity | Integer | Describes the number of stock units in a transaction.
Value | Float | Describes the monetary value of stock. $/unit, $/head, total $

#### Identifiers

This section describes the identifiers for transactions and stock classes. It identifies the other stock class when stock are transferred to or from a class.

Attributes or Fields | Data Types | Notes
:------------------- | :--------- | :----
Transaction Id |  | Holding place for an identifier for the transaction
Stock Class Id |  | Holding place for an application-specific stock class identifier
Stock Class Name |  | Application-specific stock class name
Other Stock Class Id |  | Stock class identifier for the stock class transferred to/from (e.g. for use in ageing)
Other Stock Class Name |  | Stock class name for the stock class transferred to/from

#### Footnotes

<b id="f1">1.</b> [Date Accuracy Indicator](http://meteor.aihw.gov.au/content/index.phtml/itemId/294429) – Australian Institute of Health and Welfare. [↩](#DAI)

