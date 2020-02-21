### People Data Dictionary

Contents:
* [Person Identification](#Person-Identification).
* [Person Attributes](#Person-Attributes).
  * [Staff Attributes (for Owner, Permanent and Casual Staff)](#Staff-Attributes-(for-Owner,-Permanent-and-Casual-Staff)).
  * [Visitor and Contractor Attributes](#Visitor-and-Contractor-Attributes).

This section allows for people to be assigned specific roles in relation to health and safety, and for events to be linked to people. For example, a Contractor is a visitor to the farm and may also be a ‘person conducting a business or undertaking’ ([PCBU](docs/HSDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations)) and each role carries a particular responsibility for health and safety on the farm. Those people may be associated with events, for example an induction briefing. It is recommended that people [SHOULD](docs/HSDS_Definitions-and-Abbreviations_Interpretation.md#Interpretation) be recorded with a unique identifier to allow for the linking of other relevant data to those people.

Many of the items in this table are based upon definitions at http://schema.org, which is an output of the W3C Semantic Web group, and is used by Google and Microsoft. Alternatives schemas can be found in the work of [OASIS](www.oasis-open.org) / [UBL](http://ubl.xml.org) and [UN/EDIFACT](www.unece.org/cefact/edifact). [INFORMATIVE](docs/HSDS_Definitions-and-Abbreviations_Interpretation.md#Interpretation) examples of person attributes can also be found in [Additional Person Attributes](docs/HSDS_Additional-Person-Attributes.md), referencing [schema.org/Employee](https://schema.org/EmployeeRole) Role attributes.

#### Person Identification

Attributes or Fields | Data Types | Notes
:--------------------------- | :--------- | :----
Person ID | String | Unique identifier for person or group.
Person Type | Enumeration | Owner, Permanent Staff, Casual Staff, Contractor, Farm Visitor, Recreation Visitor.
Person Roles | Enumeration | First Aid, Safety Rep, Fire Warden, [PICA](docs/HSDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations), [PCBU](docs/HSDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations).
Honorific Prefix | Enumeration | Miss, Ms, Mr, Sir, Mrs, Dr, Lady, Lord.
Name | String | Full Name.
Given Names | String | Typically the first name(s) of a person.
Family Name | String | Typically the last name of a person.
Telephone | String | An international format or country-specific format telephone number.
Mobile Number | String | An international format or country-specific format mobile telephone number.
Postal Address | | Postal Address specified using http://schema.org/postalAddress or as a formatted address string in the local format of the relevant country.
Work Location | | Physical Address specified using http://schema.org/postalAddress or as a formatted address string in the local format of the relevant country.

#### Person Attributes

##### Staff Attributes (for Owner, Permanent and Casual Staff)	

Attributes or Fields | Data Types | Notes
:--------------------------- | :--------- | :----
Farm role | | One or more of the roles in this enumeration: Property Owner, Lessee, Sharemilker, Farm Manager, Contract Milker, General Hand, Shepherd, Head Shepherd, Stock Manager, Herd Manager, Operations Manager, Tractor/Machinery Driver, Contact Person, Advisor, Partner, Accountant, First Aid, Safety Rep, Fire Warden, [PICA](docs/HSDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations), [PCBU](docs/HSDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations).
Staff From | [ISO Date](docs/HSDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) | All Staff [MUST](docs/HSDS_Definitions-and-Abbreviations_Interpretation.md#Interpretation) have a Staff From Date  [ISO 8601](docs/HSDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) Date Time.
Staff Through | [ISO Date](docs/HSDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) | Staff [MAY](docs/HSDS_Definitions-and-Abbreviations_Interpretation.md#Interpretation) have a Staff Through date which defines the last date on which the person is deemed to be a staff member. [ISO 8601](docs/HSDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) Date Time.
Paid | Boolean | Used to distinguish employees from owner-operators/family.
	

##### Visitor and Contractor Attributes

Attributes or Fields | Data Types | Notes
:--------------------------- | :--------- | :----
Weeks worked in year | Integer | Used to distinguish seasonal workers.
WorkHours | Integer | Used to distinguish part-time workers.
Visit Reason | String | Description of farm visit reason.
Time of Arrival	| [ISO 8601](docs/HSDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) | Date Time.
Time of Departure | [ISO 8601](docs/HSDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) | Date Time.
Number of Visitors | Integer | Used if two or more people visit for the same purpose at the same time.
Organisation Name | String | Organisation Name.
