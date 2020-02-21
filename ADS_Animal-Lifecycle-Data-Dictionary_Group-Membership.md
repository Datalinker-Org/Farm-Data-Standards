### Group Membership
The following table defines Group Membership, which allows management or organisation of animals in groups. It is recommended that only current group memberships [SHOULD](docs/ADS_Definitions-And-Abbreviations_Interpretation.md#Interpretation) be interchanged as animal data, and that historical uses of groups (for instance, mobs) [SHOULD](docs/ADS_Definitions-And-Abbreviations_Interpretation.md#Interpretation) be reflected in animal observations and events.

_See also [Attributes of a Group](docs/ADS_Group-Attributes-Data-Dictionary.md)._

Attributes | Data Type | Description 
:--------- | :-------- | :----------
Group Location | Data type to be determined, most likely [NAIT](docs/ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) Location. | Location identifier to which the group belongs. An animal that is grazing off at another farm may have groups on both the owning and grazing farms. | 
Group Name | Text | Name of the group within the location.
Group Type | Enumeration: Physical, Logical, Planned | Distinguishes between a physical management group (a mob of some sort) and other sorts of groupings such as a logical group of animals for analysis, or a planned group (a draft list). 
