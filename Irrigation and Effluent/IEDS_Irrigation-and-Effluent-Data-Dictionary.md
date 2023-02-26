### Irrigation and Effluent Data Dictionary (Normative)

Contents:
* [Irrigation Equipment Attributes](#Irrigation-Equipment-Attributes)
* [Irrigation Equipment Observations](#Irrigation-Equipment-Observations)
* [Irrigation Equipment Alert Observations](#Irrigation-Equipment-Alert-Observations)
* [Water Supply Attributes](#Water-Supply-Attributes)
* [Water Supply Observations](#Water-Supply-Observations)
* [Effluent Production and Collection Attributes](#Effluent-Production-and-Collection-Attributes)
* [Effluent Production and Collection Observations](#Effluent-Production-and-Collection-Observations)
* [Effluent Storage and Treatment Attributes](#Effluent-Storage-and-Treatment-Attributes)
* [Effluent Storage and Treatment Observations](#Effluent-Storage-and-Treatment-Observations)
* [Effluent Nutrient Observations](#Effluent-Nutrient-Observations)
* [Irrigation and Effluent Application Observations](#Irrigation-and-Effluent-Application-Observations)
* [Soil Moisture Attributes](#Soil-Moisture-Attributes)
* [Soil Moisture Observations](#Soil-Moisture-Observations)
* [Soil Nutrient Observations](#Soil-Nutrient-Observations)
* [Plants Use of Water](#Plants-Use-of-Water)
* [Climatic and Weather Observations](#Climatic-and-Weather-Observations)


#### Irrigation Equipment Attributes

This data dictionary [SHALL](IEDS_Definitions-and-Abbreviations_Interpretation.md#Interpretation) be used in developing messages for interchange of data concerned with attributes of the irrigation equipment.

Attributes | Data Types | Notes
:--------- | :--------- | :----
Equipment identifier | String | Name or identifier of equipment.
Equipment type | Enumeration See [Equipment Type](IEDS_Lists-of-Enumerated-Values.md#Equipment-Type). | Type of equipment or device.
Change in head | Float: [KPa](IEDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) | The effects of elevation and friction on the head, taken as the difference in pressure on the inlet vacuum gauge and the intake pressure.
Elevation change | Integer: m | The difference between the intake elevation and pump elevation.
Energy per unit volume | Float: [kW](IEDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) hour/m3 | Amount of energy used to deliver a volume of water.
Friction loss | Float: [KPa](IEDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) | Amount of pressure lost due to water movement and turbulence.
Full load motor efficiency | Float % | Efficiency of the irrigation pump motor when run at full load.
Headworks efficiency | Float: % |Pressure loss through intake structure, pump and headworks (excluding pump pressure and elevation differences).
Hydraulic efficiency | Float: % | Pressure lost between the delivery (mainline entry) and discharge points (machine entry, hydrant, or take-off in drip‑micro systems), excluding variations in elevation.
Intake elevation | Integer: m | Surface level of the water supply.
Intake pipe internal diameter | Integer: mm	| Internal diameter of the irrigator intake pipe.
Irrigation system type | Enumeration: see [Irrigation system type](IEDS_Lists-of-Enumerated-Values.md#Irrigation-system-type).| Enumeration: The irrigation system in use. 
Mainline entry elevation | Integer: m | Elevation at the exit point of the headworks.
Mainline entry pressure	| Float: [KPa](IEDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations), bar, [psi](IEDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) | Pressure at the exit of the headworks.
Mainline exit elevation | Integer: m | Elevation at the exit point of the mainline.
Mainline exit pressure | Float: [KPa](IEDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations), bar, [psi](IEDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) | Pressure at the exit of the mainline.
Mainline internal diameter | Integer: mm | Internal diameter of the irrigator mainline pipe.
Mainline length | Integer: m | Length of the mainline pipe from entry to exit.
Maximum flow rate | Float: litres/second (l/s), m3/hour	| Maximum speed at which water can be pumped through the irrigator.
Maximum velocity | Float: m/s | The standard maximum velocity in the mainline pipe under standard operating conditions.
Minimum flow rate | Float: litres/second (l/s), m3/hour | Minimum speed at which water can be pumped through the irrigator.
Overall pump efficiency | Float: %	| Energy efficiency of the irrigator pump. Also known as system pumping efficiency.
Pressure at irrigator | Float: bar, [psi](IEDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations), [KPa](IEDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) | Pressure at the sprinkler heads. Also known as operating pressure.
Pump inlet elevation | Integer: m | Relative to the water level at the intake.
Pumping rate | Integer: l/s or m3/hr)| Volume of water per unit time that a pump is designed to deliver at the design pressure.
Design travel speed	| Float: m/hour | Speed which the irrigation unit travels at.
System capacity	| Integer: l/s/ha or mm/d | Flow of water per unit of irrigated area on the basis of the system operating 24 hours per day.

#### Irrigation Equipment Observations

This data dictionary [SHALL](IEDS_Definitions-and-Abbreviations_Interpretation.md#Interpretation) be used in developing messages for interchange of data concerned with observations of the irrigation equipment.

Attributes | Data Types | Notes
:--------- | :--------- | :----
Equipment identifier | String | Name or identifier of equipment
Equipment type | Enumeration see [Equipment Type](IEDS_Lists-of-Enumerated-Values.md#Equipment-Type). | Type of equipment or device
Equipment location | String | A recognised coordinate system identified using the European Petroleum Survey Group (EPSG)<sup id="EPSG">[1](#f1)</sup> parameter registry code (e.g. EPSG::4326) or associated common name.
Device identifier | String | Identifier of device or field sender in equipment
Device type | Enumeration: see [Device Type](IEDS_Lists-of-Enumerated-Values.md##Device-Type). | Type of device.
Flow rate | Float: litres/second (l/s), litres/minute, m3/hour | Speed at which effluent or water is being pumped through the irrigator. Also known as system flow rate.
Fluid type | Enumeration | water, effluent, chemical, fertilizer Type of substance being sprayed.
Intake pipe velocity | Float: m/s | Velocity of the water in the intake pipe.
Mainline velocity | Float: m/s | Velocity of the water in the mainline pipe.
Pump inlet pressure | Float: [KPa](IEDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations), bar, [psi](IEDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) | Amount of pressure at the inlet of the irrigation pump.
Pressure operating | Float: [KPa](IEDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations), bar, [psi](IEDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) |
Calibration pressure | Float: [KPa](IEDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations), bar, [psi](IEDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) | Calibration level
Relative velocity | Float: m/s | The difference between the standard maximum velocity and mainline velocity.
Total flow rate	| Float: litres/second (l/s) | Total irrigator flow rate.
Unit travel speed | Float: m/hour | Speed which the irrigation unit is travelling at. 
Movement speed | Float: | seconds/revolution	Speed meter reading
Watering time | [ISO 8601](IEDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) Duration:  days, hours, minutes, seconds | Amount of time an irrigator is set to water for.
Sensor identifier | GUID | Unique identifier of sensor.
Sensor type	| String |
Equipment status | Boolean | Flag identifying the current status of the equipment. True means equipment is running.
Valve Status | Boolean | Indicates whether valve is on or off.
Battery voltage	| Float | v	
Signal strength	| Integer | Signal strength of received message.
Temperature	| Float: oC | Temperature in equipment.
Water level | Float: m | Water level in equipment.

#### Irrigation Equipment Alert Observations

This data dictionary [SHALL](IEDS_Definitions-and-Abbreviations_Interpretation.md#Interpretation) be used in developing messages for interchange of data concerned with observations of alerts from the irrigation equipment.

Attributes | Data Types | Notes
:--------- | :--------- | :----
Equipment identifier | String | Name or identifier of equipment.
Equipment type | String includes values in [Equipment Type](IEDS_Lists-of-Enumerated-Values.md#Equipment-Type). | Type of equipment or device
Alert type | Enumeration: see [Irrigation Equipment Alert Type](IEDS_Lists-of-Enumerated-Values.md#Irrigation-Equipment-Alert-Type). | Type of alert issued by the equipment or device.
Alert value	| Boolean:	

#### Water Supply Attributes

This data dictionary [SHALL](IEDS_Definitions-and-Abbreviations_Interpretation.md#Interpretation) be used in developing messages for interchange of data concerned with attributes of the water supply.

Attributes | Data Types | Notes
:--------- | :--------- | :----
Drainage index | Float: m3/ha/year | Volume of water draining through the area irrigated.
Drawdown | Float: m | Difference between the static and pumping water level. 
Flow rate | Float: m3/s | Flow rate of water from a pipe.
Maximum well flow rate	| Float: l/s | Highest flow rate which a well can be pumped at.
Pump type | Enumeration: Surface, submersible. | 
Intended pumping water level | Integer: m | Water level during pumping. Also known as dynamic water level.
Redistribution index | Float: m3/ha/year | Volume of water reaching the target area.
Typical water electrical conductivity | Float: decisiemens/metre (dS/m), | Salinity level of  irrigation water reported as electrical conductivity. 
Typical salinity | Float: mg/l, parts per million (ppm)	| Concentration of salts in the irrigation water reported as total dissolved solids.
Expected seasonal water use	| Float: mm/season | Amount of water used for irrigation in a season; 
Intended static water level	| Integer: m | Water level relative to the ground level when the well is not being pumped. Also known as standing water level.
Typical stream velocity | Float: m3/s | Velocity of the flow of water in a stream or channel. Also known as channel velocity.
Total storage volume | Float: m3 | Total volume of a reservoir or dam.
Typical water lost | Float: mm/season | Typical amount of water lost to drainage and runoff.
Water source | Enumeration: see [Water Source](IEDS_Lists-of-Enumerated-Values.md#Water-Source).
Water storage volume | Float: m3 | Amount of water naturally held by a reservoir.
Typical water use efficiency | Float:  mm tonne/DM	| Amount of water used in irrigation per tonne of dry matter produced.

#### Water Supply Observations

This data dictionary [SHALL](IEDS_Definitions-and-Abbreviations_Interpretation.md#Interpretation) be used in developing messages for interchange of data concerned with observations of the water supply.

Attributes | Data Types | Notes
:--------- | :--------- | :----
Pumping water level	| Integer: m | Water level during pumping. Also known as dynamic water level.
Redistribution index | Float: m3/ha/year | Volume of water reaching the target area.
Water electrical conductivity | Float: decisiemens/metre (dS/m). | Salinity level of irrigation water reported as electrical conductivity. 
Salinity | Float: mg/l, parts per million (ppm)	| Concentration of salts in the irrigation water reported as total dissolved solids.
Seasonal water use | Float:  mm/season | Amount of water used for irrigation in a season; 
Static water level | Integer: m	| Water level relative to the ground level when the well is not being pumped. Also known as standing water level.
Stream velocity | Float: m3/s | Velocity of the flow of water in a stream or channel. Also known as channel velocity.
Water lost | Float:  mm/season | Amount of water lost to drainage and runoff.
Water use efficiency | Float:  mm tonne/DM | Amount of water used in irrigation per tonne of dry matter produced.

#### Effluent Production and Collection Attributes

This data dictionary [SHALL](IEDS_Definitions-and-Abbreviations_Interpretation.md#Interpretation) be used in developing messages for interchange of data concerned with attributes of effluent production and collection.

Attributes | Data Types | Notes
:--------- | :--------- | :----
Depth of wash water	| Float: mm	| Depth of the water applied during wash-down.
Effluent removal method	| Enumeration: wash-down hoses, flood washing, scrapers.	| Method used to remove effluent from the area.
Effluent separation method | Enumeration: weeping wall, sludge bed, sump. | Method used to separate solid and liquid effluent.
Source of effluent | Enumeration: see [Source of Effluent](IEDS_Lists-of-Enumerated-Values.md#Source-of-Effluent). | Location where effluent is collected.
Effluent fluid state | Enumeration: Liquid, slurry, solid. | 
Wash water velocity | Float: m/s | Velocity at which the wash water is delivered.
Yard fall | Float: %, m/m | Slope of the wash-down area.
Yard area | Integer: m2 | Area of the wash-down area


#### Effluent Production and Collection Observations
This data dictionary [SHALL](IEDS_Definitions-and-Abbreviations_Interpretation.md#Interpretation) be used in developing messages for interchange of data concerned with observations of effluent production and collection.

Attributes | Data Types | Notes
:--------- | :--------- | :----
Hours spent on collection areas | Integer: hours | Number of hours each day that animals spend on effluent collection areas.
Animal species | Enumeration: see [Animal Life]([ADS_Animal-Lifecycle-Data-Dictionary.md#Animal-Life](https://github.com/Datalinker-Org/Farm-Data-Standards/blob/master/Animal%20Data%20Standards/ADS_Animal-Lifecycle-Data-Dictionary.md)) in the Animal Data Standard | Species binomial name or common name.
Number of animals | Integer | Number of animals of species. 
Effluent production rate | Float: m3/day, l/animal/day. | Amount of effluent produced in a time period.
Total daily water use | Integer: litres/day (l/day), m3/day. | Amount of water used to wash down surfaces which collect effluent
Total effluent solids | Integer: kg/animal/day. | Total amount of solid effluent produced by an animal over a time period.
Total effluent volume produced | Float: l/animal/day. | Volume of effluent produced by an animal over a time period.
Diluted effluent volume | Float: l/animal/day. | Volume of effluent which has been diluted with wash-water and other materials. 
Undiluted effluent volume | Float: l/animal/day. | Volume of undiluted effluent produced.
Wash-water volume | Float: l/animal/day	| Volume of wash-water used per animal per day.

#### Effluent Storage and Treatment Attributes

This data dictionary [SHALL](IEDS_Definitions-and-Abbreviations_Interpretation.md#Interpretation) be used in developing messages for interchange of data concerned with attributes of effluent storage and treatment.

Attributes | Data Types | Notes
:--------- | :--------- | :----
Batter angle |Float:  degrees, radians. | Angle between the top edge of the pond and the side of the pond.
Typical BOD5 | Float: kg/animal/day. | The biochemical oxygen demand of effluent over a 5-day period.
Primary nitrogen form | Enumeration: organic, nitrate, ammonia | Nature of the effluent. 
Effective liquid storage volume | Float: days, m3. | Storage capacity for liquid effluent, represented as volume or a timeframe.
Effective solids storage volume | Float: m3	| Storage capacity for solid effluent, represented as volume or a timeframe days.
Effluent storage type| Enumeration: sump, settling pond	| Type of storage used for effluent.
Loads per hectare | Integer: loads per hectare | Number of loads of effluent required to cover a hectare of land.
Percentage unpumpable | Float: % | Percentage of the total volume which makes up the unpumpable area.
Pond capacity | Float: m3 | Volume of the effluent treatment pond.
Pond depth | Integer: m	| Depth of the effluent treatment pond.
Pond floor size	| Float: m2	| The area of the floor of the effluent treatment pond.
Pond surface area per animal. | Float: m2/animal | Area of pond per animal producing the effluent. 
Storage volume | Float: litres/animal/day | Volume of effluent storage facilities
Top area | Float: m2 | Area of the top of the effluent pond.
Total loads	| Integer | Number of loads of effluent required to cover a specified area.
Total working volume | Float: m3 | Total working volume of the effluent pond.
Treatment method | Enumeration: land application, treatment pond, constructed wetlands, barrier ditches. | 
Unpumpable depth | Float: m	| Depth of the effluent pond which cannot be pumped due to build-up of solids.
Volume of unpumpable area | Float: m3 | Volume of the area of solids at the bottom of the pond.

#### Effluent Storage and Treatment Observations

This data dictionary [SHALL](IEDS_Definitions-and-Abbreviations_Interpretation.md#Interpretation) be used in developing messages for interchange of data concerned with observations of effluent storage and treatment.

Attributes | Data Types | Notes
:--------- | :--------- | :----
BOD5 | Float: kg/animal/day	| The biochemical oxygen demand of effluent over a 5-day period.
Limiting nutrient | Enumeration: nitrogen (N), phosphorus (P) or potassium (K). | The nutrient present in the highest quantity in effluent which will liit how much can be applied.
Limiting nutrient concentration	| Float: mg/l, g/m3. | Concentration of the limiting nutrient in the effluent.
Freeboard height | Integer: m | Distance between the top of the pond and the waterline.
Percentage Freeboard | Float: %	| Percentage of the total volume which makes up the freeboard.
Pond level % | Integer: % | Pond/tank level percentage.
Flag pond high level | Boolean | True = pond/ tank level is higher than high threshold.
Flag pond low level	Boolean | True = pond/ tank level is lower than low threshold.
Volume of Freeboard | Float: m3 | Volume of the area between the top of the pond and the waterline.
pH | Integer | A measure of the acidity or basicity of effluent.
Solid content of diluted effluent | Float: % by weight | Percentage of solids in diluted effluent.
Solid content of undiluted effluent	| Float: % by weight | Percentage of solids in undiluted effluent.
Storage period | Integer: days, months. | Period of time for which effluent has been stored between emptying events.

#### Effluent Nutrient Observations

This data dictionary [SHALL](IEDS_Definitions-and-Abbreviations_Interpretation.md#Interpretation) be used in developing messages for interchange of data concerned with observations of effluent nutrients.

Attributes | Data Types | Notes
:--------- | :--------- | :----
Nutrient | Enumeration: Nitrogen (N), phosphorus (P) or potassium (K).
Nutrient captured | Float: kg/cow/day of N, P or K.	| Amount of nutrient captured per animal per day.
Effluent Nutrient concentration	| Float: mg/l of N, P or K. | Concentration of a nutrient in effluent.
Nutrient produced | Float: kg/animal/day of N, P or K. | Amount of nutrient produced per animal per day.

#### Irrigation and Effluent Application Observations
This data dictionary [SHALL](IEDS_Definitions-and-Abbreviations_Interpretation.md#Interpretation) be used in developing messages for interchange of data concerned with observations for irrigation and effluent application.

Attributes | Data Types | Notes
:--------- | :--------- | :----
Application area | Float | Area of land which the substance is being applied to. Also known as area or surface area. Area in m2 (SI unit) or hectares (ha, accepted non-SI unit). Implementations must clearly specify which unit is used, and ensure consistent use. For spatial data interchange m2 should be used<sup id="INSPIRE">[2](#f2)</sup>.
Application depth | Float: mm | Depth of a substance applied to an area.
Application rate | Float: mm/hour | Rate at which the substance is applied. Also known as application intensity.
Distribution uniformity	| Float: % | Measure of how evenly a substance has been applied to an area.
Return interval | Integer: days, hours. | Interval between application events.
Maximum effective loading | Float: kg/ha/year | Maximum amount of the limiting nutrient which can be applied. Also known as maximum loading criteria.
Effluent Application Months | String | List of months in which effluent has been applied to areas.

#### Soil Moisture Attributes

This data dictionary [SHALL](IEDS_Definitions-and-Abbreviations_Interpretation.md#Interpretation) be used in developing messages for interchange of data concerned with attributes for soil moisture data relating to irrigation and effluent. See the [Farm Features and Attributes Data Standard](https://github.com/Datalinker-Org/Farm-Data-Standards/blob/master/Farm%20Features%20and%20Attributes/FFADS_Feature-Catalogue.md) for a definition of soil body and references to the [INSPIRE](https://inspire.ec.europa.eu/documents/Data_Specifications/INSPIRE_DataSpecification_SO_v3.0.pdf) and [ANZSoilML](http://anzsoil.org/doc/anzsoilml/html/2.0.0/) standards.

Attributes | Data Types | Notes
:--------- | :--------- | :----
Profile drainage class | Enumeration: Well, Moderately well, Imperfect, Poor, Very poor.
Hydrophobic condition | Enumeration: Rain always soaks in, Generally soaks in occasionally runs easily off slopes, Mostly runs off unless there is a long period of gentle rain.
Susceptibility to pugging | Enumeration: Rare, Occasional, Winter, Winter or rain. | 	Susceptibility to pugging or treading damage.
Drainage method | Enumeration: None, Mole/tile system, Other | Artificial drainage system
Percentage of block drained | Integer: % | 
Field capacity | Float: mm, millimetres per meter (mm/m). | Amount of water in the soil once drainage by gravity has stopped.
Infiltration rate | Float: mm/hour | Rate at which soil can absorb moisture.
Permanent wilting point	| Float: mm, millimetres of water per meter of soil (mm/m). | Soil moisture content at which a plant will die from drought stress; also known as stress point.
Available water	| Float: mm, millimetres of water per meter of soil (mm/m) | Amount of water plants can extract from the soil, the difference in moisture content between field capacity and permanent wilting point.
Readily available water	| Float: mm, millimetres of water per meter of soil (mm/m). | Amount of water plants can extract from the soil before growth is limited due to the difficulty of extracting water; the difference in moisture content between field capacity and the stress point. Also known as plant readily available water.
Refill point | Float: mm, millimetres of water per meter of soil (mm/m). | Point at which the soil water level needs to be topped up to avoid dropping to the permanent wilting point. Also known as trigger point. 
Saturation point | Float: mm, millimetres of water per meter of soil (mm/m). | Point at which the soil can no longer hold water.
Soil texture | Enumeration: see [Soil Texture](IEDS_Lists-of-Enumerated-Values.md#Soil-Texture)
Stone content of upper soil layer | Float: % | Percentage of the upper soil layer which is stone.
Water holding capacity | Float: mm, millimetres of water per meter of soil (mm/m). | Amount of water the soil can hold.

#### Soil Moisture Observations
This data dictionary [SHALL](IEDS_Definitions-and-Abbreviations_Interpretation.md#Interpretation) be used in developing messages for interchange of data concerned with observations for soil moisture data relating to irrigation and effluent.

Attributes | Data Types | Notes
:--------- | :--------- | :----
Critical deficit | Float: mm, millimetres of water per meter of soil (mm/m). | Difference between the current soil moisture content and the field capacity. Also known as soil moisture deficit.
Dry weight | Float:  mg | Dry weight of soil.
Soil moisture test method | Enumeration: type of test used to test soil moisture; see [Soil Moisture Test Method](IEDS_Lists-of-Enumerated-Values.md#Soil-Moisture-Test-Method).
Soil temperature | Float: oC | Observed temperature of the soil.
Soil water content | Float: mm, millimetres of water per meter of soil (mm/m). | Amount of water currently in the soil.
Volumetric soil moisture content | Float: V% | Percentage of the soil which is made up of water.
Wet weight | Float: mg | Wet weight of soil.

#### Soil Nutrient Observations
This data dictionary [SHALL](IEDS_Definitions-and-Abbreviations_Interpretation.md#Interpretation) be used in developing messages for interchange of data concerned with observations of soil nutrients.

Attributes | Data Types | Notes
:--------- | :--------- | :----
Nutrient | Enumeration: Nitrogen (N), phosphorus (P) or potassium (K), Sulphur (S).
Nutrient load | Float: kg of nutrient/ha. | Amount of a nutrient present in the soil.
Nutrient loss | Float: kg of nutrient/ha. | Amount of a nutrient which has been lost.

#### Plants Use of Water
This data dictionary [SHALL](IEDS_Definitions-and-Abbreviations_Interpretation.md#Interpretation) be used in developing messages for interchange of data concerned with plants use of water relating to irrigation and effluent application.

Attributes | Data Types | Notes
:--------- | :--------- | :----
Average daily crop water use | Float: l/day | Average amount of water consumed by crops.
Crop factor | Float: | The ratio of the water requirements of a particular crop to that of a reference crop (usually average grass pasture).
Estimated crop water use | Float: mm/day, mm/week. | Amount of water used by a crop over a time period.
Root depth | Float: mm, m | depth of soil profile that has enough rooting density for extraction of available water.ciency
Transpiration | Float: mm | Amount of water which is lost to transpiration through plant leaves.

#### Climatic and Weather Observations
This data dictionary [SHALL](IEDS_Definitions-and-Abbreviations_Interpretation.md#Interpretation) be used in developing messages for interchange of data concerned with climatic observations affecting irrigation and the spreading of effluent.

Attributes | Data Types | Notes
:--------- | :--------- | :----
Duration | [ISO 8601](IEDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) duration. | The period of the observation.
Metric | Enumeration: variable being measured; See [Weather Metric](IEDS_Lists-of-Enumerated-Values.md#Weather-Metric).
Aggregation	| Enumeration: total, mean, median, maximum, minimum.
Value | See [Weather Metric](IEDS_Lists-of-Enumerated-Values.md#Weather-Metric) for type and units.

This data dictionary [SHALL](IEDS_Definitions-and-Abbreviations_Interpretation.md#Interpretation) be used in developing messages for interchange of data concerned with weather observations affecting irrigation and the spreading of effluent.

Attributes | Data Types | Notes
:--------- | :--------- | :----
Barometric pressure | Float: KPa, bar, psi. | Air pressure of the Earth’s atmosphere. Also known as atmospheric pressure.
Daily rainfall | Integer: mm | Amount of rainfall for the observation day.
Potential Evapotranspiration  | Float: mm/day. | Rate of water loss from a combined surface of vegetation and soil. It includes evaporation of water from the soil surface, from free water on plants and transpiration by plants. Penman method.
Expected rainfall | Integer: mm	| Amount of rain expected.
Frost occurrence | Boolean	| If minimum air temperature less than 0.0°C
Maximum air temperature	| Integer: °C | Daily maximum air temperature.
Minimum air temperature	| Integer: °C | Daily minimum air temperature.
Probability of rainfall > 10mm	| Float: % | Probability that there will be more than 10mm of rain today.
Relative humidity | Float: % | The measure of water vapour content in the air at a given temperature.
Solar radiation	| Float: mega joules/m2/day (mJ/m2/day). | Amount of solar radiation over a period of time.
Temperature	| Integer: °C | Current ambient air temperature.
Wind speed | Float: km/hour, m/s.	

#### Footnotes

<b id="f1">1</b> [EPSG Geodetic Parameter Registry](http://www.epsg-registry.org/). [↩](#EPSG)

<b id="f2">2</b> See section 6.1.3 of D2.8.I.2 Data Specification on Administrative Units – [Technical Guidelines](https://inspire.ec.europa.eu/id/document/tg/au). [↩](#INSPIRE)

