### Data Dictionary

Contents:
* [Actual Transactions](#Actual-Transactions)
  * [Transaction Elements](#Transaction-Elements)
  * [Transaction Line Elements](#Transaction-Line-Elements)
* [Aggregated and Budget Transactions](#Aggregated-and-Budget-Transactions)
* [Balance Sheet Items](#Balance-Sheet-Items)
* [Key Performance Indicators](#Key-Performance-Indicators)

#### Actual Transactions

This data dictionary [SHALL](FDS_Definitions-and-Abbreviations_Interpretation.md#Interpretation) be used in developing messages for interchange of actual financial transactions for benchmarking and analysis.

##### Transaction Elements

Attributes or Fields | Data Type | Notes
:------------------- | :-------- | :----
Transaction ID | Identifier | Unique identifier for the transaction in the source system.
Transaction Number | Number | A visual number or identifier for the transaction (typically bounded to farm/enterprise).
Transaction Date | [ISO 8601 Date](FDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) | The date of the transaction.
Posting Date | [ISO 8601 Date](FDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) | The date of financial posting (for instance invoice date may be later than the actual sale event).
Reference | String | A reference code such as an invoice number or purchase order number.
Other Party ID | Identifier | An identifier of another party within the source system.
Other Party Contact | String | Name, short form contact details of supplier/receiver. Only intended for reference, not e-commerce.
Created Date | [ISO 8601 Date](FDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) | The date in which the transaction was created, with time-zone information if required. May be used for synchronisation.
Updated Date | [ISO 8601 Date](FDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) | The date in which the transaction was updated, with time-zone information if required. May be used for synchronisation.
URL | URL | Link to a source document
Sub Total | Float | Sub-total of the item line amounts in the transaction.
Sub Total Tax | Float | Sub-total of the tax item line amounts in the transaction.

##### Transaction Line Elements

Attributes or Fields | Data Type | Notes
:------------------- | :-------- | :----
Line ID	| Identifier | Identifies the transaction line in the source system.
Line Number | Number | Provides a line number within the transaction.
Account ID | Identifier | Unique identifier of the account in the source system.
Account Code | String | Numeric or string account ledge code as defined in the source system for that farm or enterprise.
Industry Account Code | Enumeration | Industry standard account code (used for benchmarking/reporting). See [Industry standard account code](FDS_Industry-Standard-Account-Codes.md).
Category | String | Optional additional categorisation (source system or agreed between exchanging parties).
Net Amount | Float | The net amount for the transaction; positive for a debit and negative for a credit.
Tax Amount | Float | The amount of tax in the transaction.
Tax Type | Enumeration | The tax type. See [Tax Type](FDS_Lists-of-Enumerated-Values.md#Tax-Type-(Normative)).
Gross Amount | Float | The tax inclusive amount (Net Amount + Tax Amount).
Price Basis | Enumeration | Describes the pricing basis of the transaction. See [Pricing or Valuation Basis](FDS_Lists-of-Enumerated-Values.md#Pricing-or-Valuation-Basis).
Description | String | Description of the transaction.
Quantity | Float | Describes the number of units involved in the transaction.
Unit | Enumeration | Describes the unit of measure for the item in the transaction; See [Common Units](FDS_Lists-of-Enumerated-Values.md#Common-Units).
Net Unit Amount | Float | Describes the value of one unit (Net Amount / Quantity).
Currency | Enumeration | ISO 4217 International currency code.
URL | URL | Link to a source document.

#### Aggregated and Budget Transactions

This data dictionary [SHALL](FDS_Definitions-and-Abbreviations_Interpretation.md#Interpretation) be used in developing messages for interchange of budget or aggregated financial transactions for benchmarking and analysis.

Attributes or Fields | Data Type | Notes
:------------------- | :-------- | :----
Opening Date | [ISO 8601 Date](FDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) | The opening date/time of the reporting period.
Transaction Period | [ISO 8601 Duration](FDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) | The duration of a reporting period. For instance, “P1M” is the [ISO 8601](FDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) short form for one month.
Closing Date | [ISO 8601 Date](FDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) | Opening Date and Closing Date may be specified in place of Opening Date and Transaction Period.
Created Date | [ISO 8601 Date](FDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) | The date in which the transaction was created, with time-zone information if required. May be used for synchronisation.
Updated Date | [ISO 8601 Date](FDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) | The date in which the transaction was updated, with time-zone information if required. May be used for synchronisation.
Transaction Type | Enumeration | ‘Budget’ or ‘Aggregate’.
Account ID | Identifier	| Unique identifier of the account in the source system.
Account Code | String | Numeric or string account ledge code as defined in the source system for that farm or enterprise.
Industry Account Code | Enumeration	| Industry standard account code (used for benchmarking/reporting). See [Industry standard account code](FDS_Industry-Standard-Account-Codes.md).
Category | String | Optional additional categorisation (source system or agreed between exchanging parties).
Net Amount | Float | The net amount for the transaction; positive for a debit and negative for a credit.
Tax Amount | Float | The amount of tax in the transaction.
Tax Type | Enumeration | The tax type [Tax Type](FDS_Lists-of-Enumerated-Values.md#Tax-Type).
Gross Amount | Float | The tax inclusive amount (Net Amount + Tax Amount).
Price Basis | Enumeration | Describes the pricing basis of the transaction – see [Tax Type](FDS_Lists-of-Enumerated-Values.md#Tax-Type).
Description | String | Description of aggregated or budget transaction.
Quantity | Float | Describes the number of units involved in the transaction.
Unit | Enumeration | Describes the unit of measure for the item in the transaction; see [Common Units](docs/FDS_Lists-of-Enumerated-Values.md#Common-Units).
Net Unit Amount | Float | Describes the value of one unit (Net Amount / Quantity).
Currency | Enumeration | ISO 4217 International currency code.

#### Balance Sheet Items

This data dictionary [SHALL](FDS_Definitions-and-Abbreviations_Interpretation.md#Interpretation) be used in developing messages that describe opening or closing balances in assets, liabilities, and funding.

Attributes or Fields | Data Type | Notes
:------------------- | :-------- | :----
Opening Date | [ISO 8601 Date](FDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) | The opening date/time of the reporting period.
Balance Period | [ISO 8601](FDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) Duration | The duration of a reporting period. For instance, “P1M” is the [ISO 8601](FDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) short form for one month.
Closing Date | [ISO 8601 Date](FDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) | Opening Date and Closing Date may be specified in place of Opening Date and Transaction Period.
Created Date | [ISO 8601 Date](FDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) | The date in which the item was created, with time-zone information if required. May be used for synchronisation.
Updated Date | [ISO 8601 Date](FDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) | The date in which the item was updated, with time-zone information if required. May be used for synchronisation.
Account ID | Identifier | Unique identifier of the account in the source system.
Account Code | String | Numeric or string account ledge code as defined in the source system for that farm or enterprise.
Industry Account Code | Enumeration | Industry standard account code (used for benchmarking/reporting). See [Industry standard account code](FDS_Industry-Standard-Account-Codes.md).
Category | String | Optional additional categorisation (source system or agreed between exchanging parties).
Net Amount | Float | The net amount for the transaction; positive for a debit and negative for a credit.
Gross Amount | Float | The tax inclusive amount (Net Amount + Tax Amount).
Price Basis	| Enumeration | Describes the valuation basis of the item – see [Tax Type](FDS_Lists-of-Enumerated-Values.md#Tax-Type).
Description | String | Description of the item.
Quantity | Float | Describes the number of units involved in the item.
Unit | Enumeration | Describes the unit of measure for the item; see [Common Units](FDS_Lists-of-Enumerated-Values.md#Common-Units).
Net Unit Amount | Float | Describes the value of one unit (Net Amount / Quantity).
Currency | Enumeration | ISO 4217 International currency code.

#### Key Performance Indicators

This data dictionary [SHALL](FDS_Definitions-and-Abbreviations_Interpretation.md#Interpretation) be used in developing messages that describe key performance indicators that accompany financial reporting or are used in benchmarking.

Attributes or Fields | Data Type | Notes
:------------------- | :-------- | :----
Opening Date | [ISO 8601 Date](FDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) | The opening date/time of the reporting period.
Transaction Period | [ISO 8601 Duration](FDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) | The duration of a reporting period. For instance, “P1M” is the [ISO 8601](FDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) short form for one month.
Closing Date | [ISO 8601 Date](FDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) | Opening Date and Closing Date may be specified in place of Opening Date and Transaction Period.
Transaction Period | [ISO 8601](FDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) Duration | The financial reporting period (typically a month or year) of the transaction
Created Date | [ISO 8601 Date](FDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) | The date in which the transaction was created, with time-zone information if required. May be used for synchronisation.
Updated Date | [ISO 8601 Date](FDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) | The date in which the transaction was updated, with time-zone information if required. May be used for synchronisation.
[KPI](FDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) Measure | Enumeration | [KPI](FDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) measure being expressed. See [Key Performance Indicators](FDS_Key-Performance-Indicator-Lists.md#Key-Performance-Indicators).
[KPI](FDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) Denominator	| Enumeration | Denominator of the [KPI](FDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) (if any). Typical denominators include /ha, /[FTE](FDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations), /hd. See [Common Denominators](FDS_Key-Performance-Indicator-Lists.md#Common-Denominators).
[KPI](FDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) Amount | Float | Actual value of the [KPI](FDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations).
Unit | Enumeration | The units of the [KPI](FDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations).
Currency | Enumeration | ISO 4217 International currency code.
