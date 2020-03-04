### Animal Life Data

When people talk about “life data” or “static data” for animals they mean information excluding trait, event, or observation data (such as measurements). Typically, this means unchanging or static attributes of the animals themselves. However, some of this data does change over time, so “static” data can be a misleading term, and the term “life data” is preferred as it has been well used and doesn’t have the same connotation of unchanging data.

In preparing this section of the Standard, the New Zealand Dairy Herd Test Regulations, Dairy Herd Testing Standard (NZS 8100:2007), Dairy Industry Good Animal Database ([DIGAD](ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations)) interchange specifications, [NAIT](ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) data model and interchange specifications, Beef + Lamb Genetics [SIL](ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) database, and FarmIQ animal attributes were reviewed. Additionally, the [ICAR](ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) Guidelines and Interbull standards were reviewed, as well as work carried out by Gallagher Group and Tru-Test on Animal Data Interchange [XML](ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations).

Life data of animals may be categorised as follows:

1. **[Animal Identification](ADS_Identification-of-Animals-Herds-and-Locations.md)** provides one or more identifiers for an animal

2. **[Animal Characteristics](ADS_Animal-Lifecycle-Data-Dictionary.md#Animal-life)** are non-changing attributes of an animal such as species and breed, which may be gathered over the lifetime of the animal. 

3. **[Animal Parentage](ADS_Animal-Lifecycle-Data-Dictionary.md#Animal-Parentage)** are the subset of animal characteristics that relate to the sire, dam, ET donor and recipient dam, and rearing dam of the animal.

4. **[Animal State](ADS_Animal-Lifecycle-Data-Dictionary.md#Animal-State)** is the set of information that changes in response to events or management activities carried out on the animal. There are a variety of animal states, including fate (whether the animal is dead or alive), pregnancy and lactation states, fertility status (which can change to neuter) and current location and health status. Some systems may choose not to interchange state explicitly but rather implicitly through a set of temporal observations.

5. **[Group Membership](ADS_Animal-Lifecycle-Data-Dictionary_Group-Membership.md)** describes management groups to which animals belong . 
The life data dictionary does not attempt to cover every possible application-specific field. For this reason, schemas that implement animal life data should allow for extensibility.

See [Animal Lifecycle Data Dictionary](ADS_Animal-Lifecycle-Data-Dictionary.md) or [Group Membership](ADS_Animal-Lifecycle-Data-Dictionary_Group-Membership.md) for more information.
