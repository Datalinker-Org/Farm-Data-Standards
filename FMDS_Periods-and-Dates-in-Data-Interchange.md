### Periods and Dates in Data Interchange

Much of the data shown in the [Farm Data Entities](docs/FMDS_Farm-Data-Entities.md) section pertain to the state of a farm, or the activities and observations on a farm in a defined period. This may be a future period (for instance, the long term average of a farm used to model coming years of activity), or a distinct past period (for instance, 1 June 2013 to 31 May 2014). Different benchmarking systems may use different analysis periods (June-May for dairy, July-June for sheep and beef, for instance), and some farming businesses may use different periods to fit the financial reporting requirements of their owners.

This standard specifies:

1.	That the Opening Date and Closing Date or the Balance Period for which data is relevant [SHALL](docs/FMDS_Definitions-and-Abbreviations_Interpretation.md#Interpretation) be interchanged with that data. This [SHOULD](docs/FMDS_Definitions-and-Abbreviations_Interpretation.md#Interpretation) utilise [ISO 8601 dates](docs/FMDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) and durations.

2.	That data relating to specific activities or observations [SHALL](docs/FMDS_Definitions-and-Abbreviations_Interpretation.md#Interpretation) be accompanied by an Observation Date (see the [Animal Data Standard](docs/ADS_Portal.md) for details).
 