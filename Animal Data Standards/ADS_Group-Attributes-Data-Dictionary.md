### Group Attributes Data Dictionary

See also [Groups of Animals](ADS_GroupsOfAnimals.md).

Attributes | Data Type | Description
:--------- | :-------- | :----------
Identification | [URN](ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) Identifier | A group may have 1..n identifications. 
Display Name | String | A non-unique name of the group.
Location | [URN](ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) location identifier | Location identifier to which the group belongs. An animal that is grazing off at another farm may have groups on both the owning and grazing farms.	
Species | Enumeration: Cattle, Deer, Goats, Sheep | Describes the species in common terms. 
Display Prefix | String | A short text prefix displayed in front of animals when listed in a breed society herd or flock book. 
Group Type | Enumeration: Herd, Mob, Session, Draft List, Comparison | Distinguishes between a physical management group (a mob of some sort) and other sorts of groupings such as a logical group of animals for analysis, or a planned group (a draft list).
Member Of | [URN](ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) Identifier | Identifier of a master group (for instance, mobs are members of a herd).
Group Members | [URN](ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) Identifier | identifiers of groups that are members of this group (for instance, mobs in a herd).
Animal Members | [URN](ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) Identifier | Identifiers of animals that are members of this group. 
Draft Gate | Integer | Gate number for use in a draft list. 
Criteria | String | Representation of the criteria used to generate a group	
Primary Sire Breed | Enumeration | There is no internationally recognised master list of livestock breeds. [ICAR](ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) mandates a list of codes for bovine semen straws<sup id="ICAR">[1](#f1)</sup>, and Oklahoma State University publishes a useful list of livestock breeds<sup id="OKSB">[2](#f2)</sup>. The UN Food and Agriculture Organisation (FAO) maintains a database of all domestic livestock breeds<sup id="FOADAD">[3](#f3)</sup>. We have developed an Animal Breed List based upon the existing breed lists mentioned [here](https://github.com/Datalinker-Org/Farm-Data-Standards/blob/master/Additional%20Value%20Lists/FarmDataStandards_Animal-Breed-List.md).
Primary Dam Breed | Enumeration | As for Primary Sire Breed. See [Animal Breed List](https://github.com/Datalinker-Org/Farm-Data-Standards/blob/master/FarmDataStandards_Animal-Breed-List.md).
Status | Enumeration: Active, Inactive | Status of the Group. 	
Primary Contact Details | XML, specified using EANCOM/GS1<sup id="GS1">[4](#f4)</sup>, EDIFACT<sup id="UN/EDIFACT">[5](#f5)</sup>, UBL<sup id="OASIS/UBL">[6](#f6)</sup>. | Name and contact information for the primary contact for the group.	

#### References

<b id="f1">1</b> [ICAR Guidelines 2012](https://interbull.org/ib/icarbreedcodes), Section 8 Annex 1, pp 479-481, Breed Codes on Bovine Semen Straws for International Trade assigned by ICAR Sub-committee Interbull, International Committee for Animal Recording. [↩](#ICAR)

<b id="f2">2</b> [Oklahoma State University Livestock Breeds](http://www.ansi.okstate.edu/breeds/).
 [↩](#OKSB)

<b id="f3">3</b> [FAO Domestic Animal Diversity Information System](http://www.fao.org/dad-is/en/). 
 [↩](#FAODAD)

<b id="f4">4</b> [GS1 standards for business messaging](http://www.gs1.org/gsmp/kc/ecom/eancom_overview) [↩](#GS1)

<b id="f5">5</b> [United Nations rules for Electronic Data Interchange for Administration, Commerce and Transport](http://www.unece.org/cefact/edifact/welcome.html). [↩](#UN/EDIFACT)

<b id="f6">6</b> [OASIS Universal Business Language](http://docs.oasis-open.org/ubl/os-UBL-2.1/UBL-2.1.html). [↩](#OASIS/UBL)
