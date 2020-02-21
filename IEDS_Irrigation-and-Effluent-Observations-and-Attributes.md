### Irrigation and Effluent Observations and Attributes

Contents:
* [Irrigation Equipment and Water Supply](#Irrigation-Equipment-and-Water-Supply)
* [Production, collection, storage, and treatment of effluent](#Production,-collection,-storage,-and-treatment-of-effluent)
* [Irrigation and effluent application](#Irrigation-and-effluent-application)
* [Soil attributes and observations](#Soil-attributes-and-observations)
* [Use of water by plants](#Use-of-water-by-plants)
* [Climatic and Weather Observations](#Climatic-and-Weather-Observations)


For the purpose of this Standard, an observation is the act or instance of viewing or noting a fact or occurrence for some scientific or other special purpose. Thus, an observation can include a note or record of an activity carried out, an event that has occurred, or a measurement taken.

An attribute is a characteristic or inherent part of something.  Some attributes will not change over time.  For example, characteristics of irrigation equipment are attributes.  The maximum flow rate of the equipment is an attribute whereas the flow rate is an observation – it is measured on a specific date and time.

#### Irrigation Equipment and Water Supply

This section of the standard is concerned with:

* The physical characteristics (attributes) and operational observations of the irrigation equipment

* Details of the irrigation water source and observations relating to use of water.

The identifier for these data may consist of the farm identifier and optionally an additional string naming the equipment or the water supply respectively and/or a spatial representation identifying its location.  Examples of irrigation equipment include the irrigator, irrigation pump, transfer pump, vat, water tank, agitator.  Alerts on the equipment are also identified, by the type of the alert.

Observations regarding continuous monitoring of Water Supply (for example, flow rates) SHALL be interchanged using the WaterML 2.0[^OCG] standard.

For the data dictionaries refer to [Irrigation Equipment Attributes](docs/IEDS_Irrigation-and-Effluent-Data-Dictionary.md#Irrigation-Equipment-Attributes), [Irrigation Equipment Observations](docs/IEDS_Irrigation-and-Effluent-Data-Dictionary.md#Irrigation-Equipment-Observations), [Irrigation Equipment Alert Observations](docs/IEDS_Irrigation-and-Effluent-Data-Dictionary.md#Irrigation-Equipment-Alert-Observations), [Water Supply Attributes](docs/IEDS_Irrigation-and-Effluent-Data-Dictionary.md#Water-Supply-Attributes) and [Water Supply Observations](docs/IEDS_Irrigation-and-Effluent-Data-Dictionary.md#Water-Supply-Observations).

#### Production, collection, storage, and treatment of effluent

The production and collection of effluent data defines the source of the effluent, the associated volumes, the methods of removal and separation and the washing down of surfaces. These data are identified by the farm identifier and optionally an additional string naming the storage facility and/or a spatial representation identifying its location.

The storage and treatment of the effluent includes the parameters of the storage pond, the level of nutrients involved and the treatment employed. 

For the data dictionaries refer to [Effluent Production and Collection](docs/IEDS_Irrigation-and-Effluent-Data-Dictionary.md#Effluent-Production-and-Collection-Attributes), [Effluent Storage and Treatment Attributes](docs/IEDS_Irrigation-and-Effluent-Data-Dictionary.md#Effluent-Production-and-Collection-Observations), [Effluent Storage and Treatment Attributes](docs/IEDS_Irrigation-and-Effluent-Data-Dictionary.md#Effluent-Storage-and-Treatment-Attributes), [Effluent Storage and Treatment Observations](docs/IEDS_Irrigation-and-Effluent-Data-Dictionary.md#Effluent-Storage-and-Treatment-Observations) and [Effluent Nutrient Observations](docs/IEDS_Irrigation-and-Effluent-Data-Dictionary.md#Effluent-Nutrient-Observations).

#### Irrigation and effluent application

Observations of irrigation and effluent application will be for a period or for a specific date.  These may identify the land where the substance is being applied and the rate at which it is applied.

The land areas affected may be identified by a farm identifier with optionally an additional string naming the block(s) or paddock(s) receiving the application.  Alternatively, a spatial representation may define the land areas.

For the data dictionary refer to [Irrigation and Effluent Application Observations](docs/IEDS_Irrigation-and-Effluent-Data-Dictionary.md#Irrigation-and-Effluent-Application-Observations).

#### Soil attributes and observations

Soil data fields in the standard are particularly concerned with characteristics affecting soil moisture.  These observations will be for a specific date.  Soil tests may be for a transect, block, paddock or geographic feature which may be identified by a farm identifier with optionally an additional string naming the area represented by the tests.  Alternatively, a spatial representation may define the area.

The data fields in [Soil Moisture Attributes](docs/IEDS_Irrigation-and-Effluent-Data-Dictionary.md#Soil-Moisture-Attributes) are considered a proxy for formal descriptions of the soil that will be able to be interchanged using the Australia-New Zealand Standard for Soils – SoilML.

For the data dictionaries refer to [Soil Moisture Attributes](docs/IEDS_Irrigation-and-Effluent-Data-Dictionary.md#Soil-Moisture-Attributes), [Soil Moisture Observations](docs/IEDS_Irrigation-and-Effluent-Data-Dictionary.md#Soil-Moisture-Observations) and [Soil Nutrient Observations](docs/IEDS_Irrigation-and-Effluent-Data-Dictionary.md#Soil-Nutrient-Observations).

#### Use of water by plants

This section of the standard concerns plants use of water.  The subject of these observations may be a transect, block, paddock or geographic feature which may be identified by a farm identifier with optionally an additional string naming the area represented by the tests.  Alternatively, a spatial representation may define the area.  For the data dictionary refer to [Plants Use of Water](docs/IEDS_Irrigation-and-Effluent-Data-Dictionary.md#Plants-Use-of-Water).

#### Climatic and Weather Observations

This section of the standard is for weather and climatic observations relevant to irrigation and the spreading of effluent.  Climatic observations are defined for a period and are expressed in a generalised form to provide for different quantitative summary measures (total, mean, median, minimum, maximum).  Weather observations are for the current day defined by the observation date.  The subject of these observations the identified location.

For the data dictionary refer to [Climatic and Weather observations](docs/IEDS_Irrigation-and-Effluent-Data-Dictionary.md#Climatic-and-Weather-Observations).

#### Footnotes

[^OCG]:  [OGC® WaterML](http://www.opengeospatial.org/standards/waterml)
