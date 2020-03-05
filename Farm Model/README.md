## Farm and Model Data Standard

Broad adoption of a common vocabulary and data dictionary for exchange of farm information will result in farmers and other industry parties entering data only once and having that data readily accessible for populating multiple decision-making systems. As a result, industry and individual farm businesses will be better placed to undertake systems analysis to inform management practice. More accurate and structured interchange of farm data will also support industry breeding objectives and other information system targets.

#### Scope and Application
This standard addresses data relating to the Farm entity, including farm description along with enterprise details, metrics, land application, and physical characteristics of land. This Standard relies on the OVERSEER Data Standards along with referencing other Farm Data Standards where applicable:

* Identification of farm feature characteristics, including management unit data.

* Organisational attributes, including business details, supply number, and personnel details. 

* Key Farm metrics as applicable to different enterprise types; including dairy, sheep and beef, and deer enterprises.

* Data relating to blocks of lands, termed as “Management Blocks”.

* Land application attributes, including feed, grazing, irrigation, and fertilizer.

* Climate zones and soil attributes.

### Topics

* [Identification of Locations and Herds](FMDS_Identification-of-Locations-and-Herds.md).
  * [Location Identification](FMDS_Identification-of-Locations-and-Herds.md#Location-Identification).
  * [Spatial Attributes](FMDS_Identification-of-Locations-and-Herds.md#Spatial-Attributes).
  * [Herd and Flock Identification](FMDS_Identification-of-Locations-and-Herds.md#Herd-and-Flock-Identification).
  * [Registration of Namespaces](FMDS_Identification-of-Locations-and-Herds.md#).
* [Periods and Dates in Data Interchange](FMDS_Periods-and-Dates-in-Data-Interchange.md).
* [Farm Data Entities](FMDS_Farm-Data-Entities.md).
  * [Farm Entity](FMDS_Farm-Data-Entities_Farm-Entity.md).
  * [Person and Organisations](FMDS_Farm-Data-Entities_Person-and-Organisations.md).
  * [Livestock Enterprises (Herds)](FMDS_Farm-Data-Entities_Livestock-Enterprises-(Herds).md).
  * [Derived Metrics](FMDS_Farm-Data-Entities_Derived-Metrics.md).
  * [Management Blocks](FMDS_Farm-Data-Entities_Management-Blocks.md).
  * [Feed & Grazing](FMDS_Farm-Data-Entities_Feed-&-Grazing.md).
  * [Irrigation Practices and Systems](FMDS_Farm-Data-Entities_Irrigation-Practices-and-Systems.md).
  * [Farm Structures](FMDS_Farm-Data-Entities_Farm-Structures.md).
  * [Inventory items for feeds and crops](FMDS_Farm-Data-Entities.md#Inventory-items-for-feeds-and-crops).
  * [Climate Zones](FMDS_Farm-Data-Entities.md#Climate-Zones).
  * [Soil Body](FMDS_Farm-Data-Entities_Soil-Body.md).
  * [Fertiliser Applications](FMDS_Farm-Data-Entities.md#Fertiliser-Applications).

#### Related Documents

Related standards documents published on the Farm Data Standards website include:

* [Animal Data Standard](https://github.com/Datalinker-Org/Farm-Data-Standards/blob/master/Animal%20Data%20Standards/README.md)

* [Stock Reconciliation Data Standard](https://github.com/Datalinker-Org/Farm-Data-Standards/blob/master/Stock%20Reconciliation/README.md)

* [Financial Data Standard](https://github.com/Datalinker-Org/Farm-Data-Standards/blob/master/Financial%20Data%20Standard/README.md)

* [Farm Features and Attributes Data Standard](https://github.com/Datalinker-Org/Farm-Data-Standards/blob/master/Farm%20Features%20and%20Attributes/README.md)

For more information about revisions and version updates, or to make suggestions for improvement, please visit our [Wiki Management](FMDS_Wiki-Management.md) page.

#### Acknowledgements

This document is part of a work stream focusing on Data Standards for interchanging farm and model data. Work on the overall programme commenced in late 2012.  A well-attended workshop on Farm and Model Data in September 2014 in Hamilton, New Zealand, defined the scope of this work, the entities that should be interchanged and the associated issues.

Part funded by New Zealand dairy farmers through [DairyNZ](https://www.dairynz.co.nz/) and the [Ministry for Primary Industries](https://www.mpi.govt.nz/) through the [Primary Growth Partnership](https://www.mpi.govt.nz/funding-and-programmes/sustainable-food-and-fibre-futures/primary-growth-partnership/) funding to the [Transforming the Dairy Value Chain](https://www.mpi.govt.nz/funding-and-programmes/sustainable-food-and-fibre-futures/primary-growth-partnership/completed-pgp-programmes/transforming-the-dairy-value-chain/). Part funded also by the [Red Meat Profit Partnership](https://www.rmpp.co.nz/) through its Primary Growth Partnership with Ministry for Primary Industries, [Alliance Group](https://www.alliance.co.nz/), [ANZCO Foods](https://anzcofoods.com/), [ANZ Bank](https://www.anz.com/), [Beef and Lamb New Zealand Limited](https://beeflambnz.com/) (representing sheep and beef farmers), [Blue Sky Meats](https://bluesky.co.nz/), [Greenlea Premier Meats](https://www.greenlea.co.nz/), [Progressive Meats](https://www.progressivemeats.co.nz/), [Rabobank](https://www.rabobank.com/), and [Silver Fern Farms](https://www.silverfernfarms.com/). 

![DairyNZLogo](https://github.com/Datalinker-Org/Farm-Data-Standards/blob/master/Images/DairyNZ_205x100.png)
![RMPPLogo](https://github.com/Datalinker-Org/Farm-Data-Standards/blob/master/Images/RMPP_1_75.png)
![MPILogo](https://github.com/Datalinker-Org/Farm-Data-Standards/blob/master/Images/MPI.png)
![FARMIQLogo](https://github.com/Datalinker-Org/Farm-Data-Standards/blob/master/Images/FarmIQ_240x50.png)
![RezareSystemsLogo](https://github.com/Datalinker-Org/Farm-Data-Standards/blob/master/Images/RezareSystems_180x110.png)

#### Referenced Documents

GS1 standards for business messaging, [EANCOM/GS1 XML](http://www.gs1.org/gsmp/kc/ecom/eancom_overview).

United Nations rules for Electronic Data Interchange for Administration, Commerce and Transport, [EDIFACT](http://www.unece.org/cefact/edifact/welcome.html).

OASIS Universal Business Language, [UBL](http://docs.oasis-open.org/ubl/os-UBL-2.1/UBL-2.1.html).

Core Business Vocabulary ([CBV](http://www.gs1.org/gsmp/kc/epcglobal/cbv)).

[Australian and New Zealand Standard Industrial Classification](http://www.abs.gov.au/AUSSTATS/abs@.nsf/DetailsPage/1292.02006%20(Revision%202.0)?OpenDocument) (ANZSIC) 2006 with revisions.

Feedipedia - [Forage Plants](http://www.overseer.org.nz/files/download/119b106220ef304)

OVERSEER – [Best Practice Data Input Standards](https://www.waikatoregion.govt.nz/assets/WRC/Council/Policy-and-Plans/HR/ReadProposedPlan/Overseer.pdf)

Schema.org - [Organisation](http://schema.org/Organization)

[INSPIRE Feature Concept Register](http://inspire.ec.europa.eu/featureconcept)

INSPIRE Data Specification on Administrative Units – [Technical Guidelines](https://inspire.ec.europa.eu/id/document/tg/au)

[International System of Units](https://en.wikipedia.org/wiki/International_System_of_Units)
