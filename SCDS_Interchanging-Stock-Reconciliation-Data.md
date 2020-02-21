### Interchanging Stock Reconciliation Data

Contents:
* [Stock Class Names and Attributes](#Stock-Class-Names-and-Attributes)
* [Transaction Types](#Transaction-Types)

This standard defines names and data types for the fields that are used to interchange stock numbers information. This includes the use of period or balance dates to delineate a reporting period in a stock reconciliation, numbers of animals, and stock class names.

#### Stock Class Names and Attributes

In the past classes of livestock have been identified by name, and the names used have varied by region or business enterprise. 

This standard requires identification of each stock class through a unique combination of attributes that describe that stock class. Interchange of a stock class name is still supported, but organisations should expect to match data using the stock class attributes and only utilise the name if required for their application.

The attributes used to describe a stock class are those that would apply to animals in the stock class. Therefore the categorical definition of those attributes may be found in the [Animal Data Standard](docs/ADS_Animal-Lifecycle-Data-Dictionary.md#Animal-State). [Informative Stock Class Definitions](docs/SRDS_Portal.md#Topics) in this Standard list commonly used stock class names and show how they would be represented using the attributes of the animals in the stock class.

#### Transaction Types
This Standard requires that each transaction (including a simple representation of animals on hand) shall be identified with a transaction category and transaction type. The use of a transaction category allows systems receiving data to quickly differentiate between animals on-hand, arriving, and departing. The transaction type then describes more detail of the transaction (for instance, sent back from grazing, See [Transaction Category and Type](docs/SCD_Lists-of-Valid-Values.md#Transaction-Category-and-Transaction-Type)).
