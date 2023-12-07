### Feature Attributes Data Dictionary (Normative)

Contents:
* [Plot Special Case Attributes](#Plot-Special-Case-Attributes)
* [Riparian Zone Attributes](#Riparian-Zone-Attributes)
* [Fence and Gate Attributes](#Fence-and-Gate-Attributes)
* [Emergency Location Attributes](#Emergency-Location-Attributes)

This section provides more detail on spatial features in the [Feature Catalogue](FFADS_Feature-Catalogue.md) that do not have a reference document, but are still considered as important features for spatial data on NZ farms. Note that each feature will have geographic coordinates and shape attributes and a Feature Identifier and/or Feature Name as described in [Spatial Attributes](FFADS_Location-Identification_&_Spatial-Attributes.md#Spatial-Attributes).

#### Plot Special Case Attributes

A Plot consists of geographical features with detailed information about the management activities performed on them, such as irrigation and drainage. The spatial blocks that a farmer uses to manage land may be different to those defined by land titles, soil, or climate zones. In New Zealand we use the term “Management Blocks” to define blocks that are managed differently, which is the equivalent of a Site in the INSPIRE framework.  Typically these differ in irrigation or effluent application, fertilisers applied, and types and numbers of stock grazed. A Site can be separated into plots, and then further into paddocks or fields, which define sub-sections of a Site/Management Block. Refer additional attributes relating to pastoral blocks and support blocks contained in the [Management Blocks](https://github.com/Datalinker-Org/Farm-Data-Standards/blob/master/Farm%20Model/FMDS_Farm-Data-Entities_Management-Blocks.md) section of the Farm Model Data Standard.

A Paddock describes the special case of a plot that is used specifically for grazing livestock. It is an individual area delineated by a boundary. The paddock attributes listed here have been defined specifically to reflect NZ pastoral farming and may be used in addition to the attributes of a Plot or Site. 

A Field describes the special case of a plot that is used specifically for arable cropping. It is an individual area delineated by a boundary. The field attributes listed here have been defined specifically to reflect the NZ arable cropping and may be used in addition to the attributes of a Plot or Site.

##### Plot

Attributes | Data Types | Notes
:--------- | :--------- | :----
Plot Type |	Enumeration | Field, Paddock
Plot Name | String | the name used to refer to the field or paddock within the farm.
Plot Activity Value | Enumeration | the type of vegetation grown here: e.g. permanent grassland.  For INSPIRE code list, see [Plot Activity Value Enumeration List](https://github.com/Datalinker-Org/Farm-Data-Standards/blob/master/Farm%20Features%20and%20Attributes/FFADS_Enumeration-Lists.md#Plot-Activity-Value).
Secondary Plot Activity Value | String | Description of any secondary values relevant to the plot, i.e. fodder beet section on grazing plot.
Pasture Type | Enumeration | Ryegrass/white clover, Browntop, Unimproved/tussock grasslands, SummerC4 (paspalum) pastures, C4 (kikuyu) pastures, Lucerne, Grass only (enumeration defined by Overseer<sup id="OVERSEER">[1](#f1)</sup>)
Pasture utilisation | Integer | %
Average pasture N Concentration | Integer | %
Total area | Float | Total plot area expressed in m<sup>2</sup> (SI unit) or hectares (ha, accepted non-SI unit). Implementations must clearly specify which unit is used, and ensure consistent use. For spatial data interchange m<sup>2</sup> should be used<sup id="INSPIRE">[2](#f2)</sup>.
Effective Area | Float | Effective area of the plot taking into account slope. Valid units for expressing area are m<sup>2</sup> (SI unit) or hectares (ha, accepted non-SI unit). Implementations must clearly specify which unit is used, and ensure consistent use. For spatial data interchange m<sup>2</sup> should be used<sup id="INSPIRE1">[2](#f2)</sup>..
Cultivable Area | Float | Effective area of the plot for cultivation (cropping) purposes. Valid units for expressing area are m<sup>2</sup> (SI unit) or hectares (ha, accepted non-SI unit). Implementations must clearly specify which unit is used, and ensure consistent use. For spatial data interchange m<sup>2</sup> should be used.
Grazeable Area | Float | The area of the plot that may be grazed by livestock, in m<sup>2</sup> (SI unit) or hectares (ha, accepted non-SI unit). Implementations must clearly specify which unit is used, and ensure consistent use. For spatial data interchange m<sup>2</sup> should be used<sup id="INSPIRE2">[2](#f2)</sup>.. 
Ownership | Enumeration | Owned, Leased
Topography | Enumeration | Flat, Rolling, Easy hill, Steep hill (this enumeration is defined by OVERSEER<sup id="OVERSEER1">[1](#f1)</sup>)
Date Start | ISO 8601 Date | Date started operating for specific paddock type.
Date End | ISO 8601 Date | Date ended(ceased) operating for specific paddock type.

#### Riparian Zone Attributes

The riparian zone is a special case of the management restriction or regulation zone, describing the interface between land a river or stream. A riparian zone is considered a terrestrial biome in its own right and plays a considerable role in ecology, environmental management, and soil conservation. This term is used predominantly in the New Zealand dairy industry context, closely tied to riparian management plans which include riparian planting, fencing, and exclusion of stock from waterways. The Sustainable Dairy Water Accord ([SDWA](http://www.dairynz.co.nz/media/3286407/sustainable-dairying-water-accord-2015.pdf)) describes the attributes contained here.

Attributes | Data Types | Notes
:--------- | :--------- | :----
Riparian Zone Type | Enumeration | Waterway, Drain, Wetland, Other (Definitions used in [SDWA](http://www.dairynz.co.nz/media/3286407/sustainable-dairying-water-accord-2015.pdf))
Riparian Zone Name | String | Identification or description of the Riparian Zone.
SDWA Management | Boolean | Describes if this feature is subject to [SDWA](http://www.dairynz.co.nz/media/3286407/sustainable-dairying-water-accord-2015.pdf) Management requirements
SDWA Compliant | Boolean | Describes if the feature is compliant with the [SDWA](http://www.dairynz.co.nz/media/3286407/sustainable-dairying-water-accord-2015.pdf)
SDWA Dispensation | Boolean | Describes if a [SDWA](http://www.dairynz.co.nz/media/3286407/sustainable-dairying-water-accord-2015.pdf) dispensation is granted for this feature
Fenced | Integer | % - Percentage of feature fenced to exclude stock as defined in the [SDWA](http://www.dairynz.co.nz/media/3286407/sustainable-dairying-water-accord-2015.pdf)
Riparian Management Planting | Integer | % - Percentage of Riparian planting as detailed in the Riparian Management Plan which is complete for this feature
Regular Stock Crossing Point | Boolean | As defined in the [SDWA](http://www.dairynz.co.nz/media/3286407/sustainable-dairying-water-accord-2015.pdf)
Related Zone | String | Reference to a related riparian zone/s.
Plan | String | Reference to, or citation of a plan (management or action plan) that describes the environmental objectives and measures that shall be undertaken in the zone to protect the environment.

#### Fence and Gate Attributes

##### Fence

Attributes | Data Types | Notes
:--------- | :--------- | :----
Fence Type | Enumeration | Wire, Post and rail, Other
Batten Distance | Float | m Distance between battens
Wires/Rail Distance | Float | m Distance between wires or rails
Number of Wires/Rails | Integer | Number of wires or rails
Electric Wire Number | Integer | Number of wires electrified
Planned Life | Enumeration | permanent, temporary, moveable.
    
##### Gate

Attributes | Data Types | Notes
:--------- | :--------- | :----
Gate Type | Enumeration | Metal, Wooden, Other
Latch Type | String | 


#### Emergency Location Attributes

Feature	| Attributes | Data Types | Notes
:------ | :--------- | :--------- | :----
Emergency Location | Emergency Location Type | Enumeration | First Aid Point, Evacuation Point, Emergency Vehicle Access Point, Ingress Point, Sign-in Point, Aerodrome Area.

#### Footnotes

<b id="f1">1</b> OVERSEER is a trademark and a computer software model: See [www.overseer.org.nz](https://www.overseer.org.nz/) for more information. Parameters should be collected in line with the [OVERSEER Best Practice Data Input Standards](https://www.waikatoregion.govt.nz/assets/WRC/Council/Policy-and-Plans/HR/ReadProposedPlan/Overseer.pdf). [↩](#OVERSEER) [↩](#OVERSEER1)

<b id="f1">1</b> See section 6.1.3 of INSPIRE Data Specification on Administrative Units – [Technical Guidelines](https://inspire.ec.europa.eu/id/document/tg/au) [↩](#INSPIRE) [↩](#INSPIRE1) [↩](#INSPIRE2)
