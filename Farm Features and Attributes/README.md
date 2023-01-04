## Farm Features and Attributes

Broad adoption of a common vocabulary and data dictionary for exchange of farm information will result in farmers and other industry parties entering data only once and having that data readily accessible for populating multiple decision-making systems. As a result, industry and individual farm businesses will be better placed to undertake systems analysis to inform management practice. More accurate and structured interchange of farm data will also support industry breeding objectives and other information system targets.

#### Scope and Application

This standard relates to Features that are useful at a farm scale, **which have a spatial representation and that are likely to be interchanged**. The standard builds on and complements existing data standards such as those developed by the Open Geospatial Consortium and the Infrastructure for Spatial Information in Europe.

The standard addresses:

* Identification of Farm Features using a feature catalogue.

* The attributes of the Farm Features and references to source documents using a Data Dictionary.

* Farm Emergency Locations

* Enumerations relating to Agricultural Buildings and activity values for land (Plot activity values).

### Topics

* [Location Identification](FFADS_Location-Identification_&_Spatial-Attributes.md#Location-Identification)
* [Spatial Attributes](FFADS_Location-Identification_&_Spatial-Attributes.md#Spatial-Attributes)
* [Feature Catalog](FFADS_Feature-Catalogue.md)
  * [Farm Features](FFADS_Feature-Catalogue.md#Farm-Features)
  * [Feature Hierarchy](FFADS_Feature-Catalogue.md#Feature-Hierarchy)
* [Feature Attributes Data Dictionary](FFADS_Feature-Attributes-Data-Dictionary.md)
  * [Plot Special Case](FFADS_Feature-Attributes-Data-Dictionary.md#Plot-Special-Case-Attributes)
  * [Riparian Zone](FFADS_Feature-Attributes-Data-Dictionary.md#Riparian-Zone-Attributes)
  * [Fence and Gate](FFADS_Feature-Attributes-Data-Dictionary.md#Fence-and-Gate-Attributes)
  * [Emergency Location](FFADS_Feature-Attributes-Data-Dictionary.md#Emergency-Location-Attributes)
* [Enumeration Lists](FFADS_Enumeration-Lists.md)
  * [Type of AgriBuilding](FFA_Enumeration-Lists.md#Type-of-AgriBuilding-Value-Enumeration-List)
  * [Plot Activity](FFA_Enumeration-Lists.md#Plot-Activity-Value-Enumeration-List)

For more information about revisions and version updates, or to make suggestions for improvement, please visit our [Wiki Management](FFADS_Wiki-Management.md) page.


#### Related Documents

Related standards documents on the Farm Data Standards website include:

* [Farm and Model Data Standard](https://github.com/Datalinker-Org/Farm-Data-Standards/blob/master/Farm%20Model/README.md)

* [Pasture Feed and Grazing Data Standard](https://github.com/Datalinker-Org/Farm-Data-Standards/blob/master/Pasture%20Graze%20and%20Feed/README.md)

* [Irrigation and Effluent Data Standard](https://github.com/Datalinker-Org/Farm-Data-Standards/blob/master/Irrigation%20and%20Effluent/README.md)

* [Land Application Data Standard](https://github.com/Datalinker-Org/Farm-Data-Standards/blob/master/Land%20Application%20Standard/README.md)

Particular reference should be made to the Farm and Model Data Standard which also includes data types with a spatial attribute. These have been referenced accordingly within this document.

#### Acknowledgements

This document is part of a work stream focusing on Data Standards for interchanging farm and land information. Development of this Data Standard began with a workshop of interested parties in November 2015, followed by consultation with a wider group. This draft document is now distributed for final consultation and feedback. 

Part funded by New Zealand dairy farmers through [DairyNZ](https://www.dairynz.co.nz/) and the [Ministry for Primary Industries](https://www.mpi.govt.nz/) through the [Primary Growth Partnership](https://www.mpi.govt.nz/funding-and-programmes/sustainable-food-and-fibre-futures/primary-growth-partnership/) funding to the [Transforming the Dairy Value Chain](https://www.mpi.govt.nz/funding-and-programmes/sustainable-food-and-fibre-futures/primary-growth-partnership/completed-pgp-programmes/transforming-the-dairy-value-chain/). Part funded also by the [Red Meat Profit Partnership](https://www.rmpp.co.nz/) through its Primary Growth Partnership with Ministry for Primary Industries, [Alliance Group](https://www.alliance.co.nz/), [ANZCO Foods](https://anzcofoods.com/), [ANZ Bank](https://www.anz.com), [Beef and Lamb New Zealand Limited](https://beeflambnz.com/) (representing sheep and beef farmers), [Blue Sky Meats](https://bluesky.co.nz/), [Greenlea Premier Meats](https://www.greenlea.co.nz/), [Progressive Meats](https://www.progressivemeats.co.nz/), [Rabobank](https://www.rabobank.com/en/home/index.html), and [Silver Fern Farms](https://www.silverfernfarms.com/). 

![DairyNZLogo](https://github.com/Datalinker-Org/Farm-Data-Standards/blob/master/Images/DairyNZ.png)
![RMPPLogo](https://github.com/Datalinker-Org/Farm-Data-Standards/blob/master/Images/RMPP.png)
![MPILogo](https://github.com/Datalinker-Org/Farm-Data-Standards/blob/master/Images/MPI.png)
![RezareSystemsLogo](https://github.com/Datalinker-Org/Farm-Data-Standards/blob/master/Images/RezareSystems.png)

#### Referenced Documents 

Open Geospatial Consortium - [OGC® WaterML](http://www.opengeospatial.org/standards/waterml).

Open Geospatial Consortium - [OGC Soil Data IE](http://www.opengeospatial.org/projects/initiatives/soildataie).

OVERSEER - [Best Practice Data Input Standards](https://www.waikatoregion.govt.nz/assets/WRC/Council/Policy-and-Plans/HR/ReadProposedPlan/Overseer.pdf).

International Organization for Standardization (ISO) - [ISO 19110](https://www.iso.org/obp/ui/#iso:std:iso:19110:ed-1:v1:en).

Dairy NZ - [Sustainable Dairy Water Accord](http://www.dairynz.co.nz/media/3286407/sustainable-dairying-water-accord-2015.pdf).

INSPIRE  Data Specification - [Agricultural and Aquaculture Facilities](http://inspire.ec.europa.eu/documents/Data_Specifications/INSPIRE_DataSpecification_AF_v3.0.pdf).

INSPIRE Data Specification – [Cadastral parcels](http://inspire.ec.europa.eu/documents/Data_Specifications/INSPIRE_DataSpecification_CP_v3.1.pdf).

INSPIRE Data Specification – [Geographical Grid Systems](http://inspire.ec.europa.eu/documents/Data_Specifications/INSPIRE_DataSpecification_GG_v3.1.pdf).

INSPIRE Data Specification – [Hydrography](http://inspire.ec.europa.eu/documents/Data_Specifications/INSPIRE_DataSpecification_HY_v3.1.pdf).

INSPIRE Data Specification – [Area Management/Restriction/Regulation Zones and Reporting Units](http://inspire.ec.europa.eu/documents/Data_Specifications/INSPIRE_DataSpecification_AM_v3.0.pdf).

INSPIRE Data Specification – [Soil](http://inspire.ec.europa.eu/documents/Data_Specifications/INSPIRE_DataSpecification_SO_v3.0.pdf).

INSPIRE Data Specification – [Protected Sites](http://inspire.ec.europa.eu/documents/Data_Specifications/INSPIRE_DataSpecification_PS_v3.2.pdf).

INSPIRE Data Specification – [Land Cover](http://inspire.ec.europa.eu/documents/Data_Specifications/INSPIRE_DataSpecification_LC_v3.0.pdf).

INSPIRE Data Specification – [Transport Networks](https://inspire.ec.europa.eu/file/1723/download?token=0GOYYbMF).

INSPIRE Data Specification – [Utility and Government services](https://inspire.ec.europa.eu/file/1518/download?token=sGDcVnQQ).

INSPIRE Data Specification – [Habitats and Biotopes](https://inspire.ec.europa.eu/file/1524/download?token=an0ToVBS).

INSPIRE Data Specification – [Elevation](https://inspire.ec.europa.eu/file/1530/download?token=pq85sbLG).

INSPIRE Data Specification – [Natural Risk Zones](https://inspire.ec.europa.eu/file/1541/download?token=MK-3mZr-).

European Petroleum Survey Group - [EPSG parameter registry guide](http://www.iogp.org/pubs/373-07-3.pdf).

Wolfert, S and Allen, J. Farming for the future: Towards better information-based decision-making and communication. 2011. A Report for the Centre of Excellence in Farm Business Management pp 27.

[INSPIRE Feature Concept Register](http://inspire.ec.europa.eu/featureconcept).

INSPIRE Data Specification on Administrative Units – [Technical Guidelines](https://inspire.ec.europa.eu/file/1727/download?token=ay7GNn1e).

[International System of Units](https://en.wikipedia.org/wiki/International_System_of_Units).
