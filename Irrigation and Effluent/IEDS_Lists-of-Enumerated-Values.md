
### Lists of Enumerated Values

Contents:
* [Geometry Type](#Geometry-Type)
* [Irrigation system type](#Irrigation-system-type)
* [Equipment Type](#Equipment-Type)
* [Irrigation Equipment Alert Type](#Irrigation-Equipment-Alert-Type)
* [Water Source](#Water-Source)
* [Source of Effluent](#Source-of-Effluent)
* [Soil Moisture Test Method](#Soil-Moisture-Test-Method)
* [Soil Texture](#Soil-Texture)
* [Device Type](#Device-Type)
* [Weather Metric](#Weather-Metric)

#### Geometry Type

Geometry Type may be used in spatial representations for geographic identification for a number of observation types. 

Valid values for Geometry Type are: |
:---------------------------------- |
Point |
LineString |
Polygon |
MultiPoint |
MultiLineString |
MultiPolygon |

#### Irrigation system type

Irrigation System Type is used in the Irrigation Equipment observation.

Valid values for Irrigation System Type are:|
:------------------------------------------ |
border-strip |
centre-pivot |
drip (point source) |
drip line | 
fixed boom (low pressure) |
fixed boom (medium pressure) | 
hand shift |
linear move |
micro sprinkler |
rotary boom |
side roll |
solid set sprinklers |
travelling gun |

#### Equipment Type

Equipment Type is used in the Irrigation Equipment Attributes, Irrigation Equipment Observations and Irrigation Equipment Alert observation.

Values for Equipment Type include: |
:--------------------------------- |
irrigation pump |
transfer pump |
greenwash pump |
agitator pump |
vat |
water tank |
water trough |
pond |
data logger |
transmitter |

#### Irrigation Equipment Alert Type

Irrigation Equipment Alert Type is used in the Irrigation Equipment Alert observation.

Valid values for Irrigation Equipment Alert Type are:|
:--------------------------------------------------- |
low pressure |
high pressure | 
no pressure |
no movement |
movement too slow |
movement too fast |
end of travel |
high temperature |
high level |
low level | 
no signal |

#### Water Source

Water Source is used in the Water Supply observation. See the Farm Features and Attributes Data Standard [feature catalog](https://github.com/Datalinker-Org/Farm-Data-Standards/blob/master/Farm%20Features%20and%20Attributes/FFADS_Feature-Catalogue.md) for definitions of Watercourses and Waterways.

Valid values for Water Source are:|
:-------------------------------- |
confined aquifer (groundwater) |
water table aquifer (groundwater) |
run-of-river surface water | 
stored surface water |

#### Source of Effluent

Source of Effluent is used in the Effluent Production & Collection observation.

Valid values for Source of Effluent are:|
:-------------------------------------- |
dairy |
stand-off pad |
feed pad | 
winter barn | 
loafing pad	|
wintering pad | 

#### Soil Moisture Test Method

Soil Moisture Test Method is used in the Soil Moisture Characteristics observation.

Valid values for Soil Moisture Test Method are:|
:--------------------------------------------- |
capacitance probe |
electric resistance |
gravimetric | 
neutron thermalisation |
soil suction |
soil thermocouple psychrometers |
thermal dissipation methods |
time domain reflectometry |
time domain transmission |

#### Soil Texture

Soil Texture is used in the Soil Moisture Characteristics observation.

Valid values for Soil Texture are:|
:-------------------------------- |
unknown	clay |
clay loam |
loam |
loamy peat |
loamy sand |
peat |
peaty loam |
peaty sand | 
peaty sandy loam | 
peaty silt loam |
sand |
sandy clay |
sandy clay loam | 
sandy loam | 
sandy silt |
silt |
silt loam | 
silty clay |
silty clay loam	|
silty peat | 
silty sand | 

#### Device Type

Equipment Type is used in the Irrigation Equipment Observations.

Valid values for Device Type are:

Devices:|
:------ |
pump controller |
travelling irrigator monitor |
k-line irrigator monitor |
centre pivot irrigator monitor |

Field Senders:|
:------------ |
bore monitor |
flow monitor |
pond monitor |
vat monitor | 
soil monitor | 
sump monitor | 
magflow monitor | 
pimstop monitor | 
tank monitor | 

#### Weather Metric

Metric is used in the Weather observation to identify the variable concerned.

Valid values for Metric and associated units are:


Metric | Type | Units
:----- | :--- | :----
Rainfall | Integer | mm
Temperature	| Float | °C
Maximum Temperature | Float | °C
Minimum Temperature	| Float	°C
Soil Temperature | Float | °C
Wind speed | Float | Km/hour, m/s
Wind gust | Float | Km/hour, m/s
Wet days | Integer | Days
Relative humidity | Float | %
Barometric pressure | Float | [KPa](IEDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations), bar, [psi](IEDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations)
Potential evapotranspiration | Float | mm/day
Solar radiation | Float	| MJ/m2/day
Frost occurrence | Boolean | 
Day length | Float | hour

