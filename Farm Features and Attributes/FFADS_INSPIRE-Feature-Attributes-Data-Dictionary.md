### INSPIRE Feature Attributes Data Dictionary (Informative)

This Appendix is Informative and describes the attributes deemed most relevant to New Zealand’s primary production systems. In all cases, these attributes derive from the INSPIRE Data Specification documents already referenced, and these documents remain the primary or Normative source.  

Feature | Attributes | Data Type | Notes
:------ | :--------- | :-------- | :----
[Cadastral](FFADS_Definitions-and-Abbreviations.md#Definitions-and-Abbreviations) Parcel | National [Cadastral](FFADS_Definitions-and-Abbreviations.md#Definitions-and-Abbreviations) Reference | String | National code of the [cadastral](FFADS_Definitions-and-Abbreviations.md#Definitions-and-Abbreviations) parcel as recorded by [LINZ](https://data.linz.govt.nz/layer/772-nz-primary-parcels/).
[Cadastral](FFADS_Definitions-and-Abbreviations.md#Definitions-and-Abbreviations) Parcel | Area Value | Float | m<sup>2</sup> Registered area value
Basic Property Unit	| National [Cadastral](FFADS_Definitions-and-Abbreviations.md#Definitions-and-Abbreviations) Reference | String | National code of the [cadastral](FFADS_Definitions-and-Abbreviations.md#Definitions-and-Abbreviations) parcel as recorded by [LINZ](https://data.linz.govt.nz/layer/772-nz-primary-parcels/).
Basic Property Unit	| Area Value | Float |  m<sup>2</sup> Registered area value
Holding | | | Additional Holding Attributes are defined in the [Farm and Model data standard](http://www.farmdatastandards.org.nz/wp-content/uploads/2016/03/DINDS-Farm-Model-Data-Discussion-2015-01-09.pdf) as ‘Farm Entity’.
Site | | | Additional Site Attributes are defined in the [Farm and Model data standard](http://www.farmdatastandards.org.nz/wp-content/uploads/2016/03/DINDS-Farm-Model-Data-Discussion-2015-01-09.pdf) as ‘Management Block’.
Plot | Plot Activity Value | Enumeration | See [Plot Activity](FFA_Enumeration-Lists.md#Plot-Activity-Value-Enumeration-List).
Plot | Area | Float |  m<sup>2</sup>
Drainage Basin | Area | Float | m<sup>2</sup>
Drainage Basin | Origin | Enumeration | natural, manMade
Management, Restriction or Regulation Zone | Competent Authority | String |  Description of the organisation(s) responsible for managing, restricting or regulating measures or activities within the zone.
Management, Restriction or Regulation Zone | Legal Basis | String | Reference to, or citation of the legislative instrument or document that required the establishment of a zone. 
Management, Restriction or Regulation Zone | Plan	| String | Reference to, or citation of a plan (management or action plan) that describes the environmental objectives and measures that shall be undertaken in the zone to protect the environment. 
Protected Site | Legal Foundation Date | [ISO](FFADS_Definitions-and-Abbreviations.md#Definitions-and-Abbreviations) DateTime | The data that the protected site was legally created.
Protected Site | Site Designation	| | 
Protected Site | Site Protection Classification | Enumeration | natureConservation, archaeological, cultural, ecological, landscape, environment, geological.
Watercourse | Length | Float | m
Watercourse | Width Range Upper | Float | The upper bound of width along its length.
Watercourse | Width Range Lower | Float | The lower bound of width along its length. 
Crossing | Crossing Type Value | Enumeration | aqueduct, bridge, culvert, siphon.
Utility Network | Utility Network Type | Enumeration | Electricity, oilGasChemical, sewer, water, thermal, telecommunications, crossTheme.
Tower | Tower Height | Float | m - The height of the tower.
Pole | Pole Height | Float | m - The height of the pole.
Pipe | Pipe Diameter | Float | m - Pipe outer diameter.
Pipe | Pressure | Float | Bar The maximum allowable operating pressure at which a product is conveyed through a pipe, commonly expressed in “bar”.
Duct | Duct Width | Float | m
Aerodrome Area | Aerodrome Type | Enumeration | aerodromeHeliport, aerodromeOnly,  heliportOnly, landingSite.
Aerodrome Area | Surface Composition Value | Enumeration | asphalt, concrete, grass
AgriBuilding | AgriBuilding Type | Enumeration | See [Types of AgriBuildings](FFA_Enumeration-Lists.md#Plot-Activity-Value-Enumeration-List) for valid values.
Installation | Description	| String | A description of the facility.
Water Management Installation | Water Quantity | Float | m<sup>3</sup> The quantity of water given by the water source.
Water Management Installation | Type of Water Source	| Enumeration | onFarmGroundWater, onFarmSurfaceWater, offFarmSurfaceWater, offFarmWaterFromCommonWaterSupplyNetworks, otherSources.
Contour Line | Contour Line Type | Enumeration | Master, ordinary, auxiliary.
Contour Line | Down Right | Boolean
