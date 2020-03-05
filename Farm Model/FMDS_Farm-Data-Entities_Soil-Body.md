### Soil Body
The following table defines attributes of the soil zone for the farm. For entering the name, coordinates, and shape of the soil body, use the spatial attributes defined in [Spatial Attributes](FMDS_Identification-of-Locations-and-Herds.md#Spatial-Attributes). See the [Farm Features and Attributes Data Standard](https://github.com/Datalinker-Org/Farm-Data-Standards/blob/master/Farm%20Features%20and%20Attributes/FFADS_Feature-Catalogue.md) for a definition of soil body and references to the [INSPIRE](http://inspire.ec.europa.eu/documents/Data_Specifications/INSPIRE_DataSpecification_SO_v3.0.pdf) and [ANZSoilML](http://anzsoil.org/doc/anzsoilml/html/2.0.0/) standards.

#### Soil description and profile

Attributes | Data Types | Notes
:--------- | :--------- | :----
Soil group | Enumeration | Sedimentary, Volcanic, Pumice, Podzol, Sand, Peat, Recent/YGE/BGE
Soil order | Enumeration | Allophanic, Brown, Gley, Granular, Melanic, Organic, Oxidic, Pallic, Podzol, Pumice, Recent, Semiarid, Ultic
Top soil texture | Enumeration | See [Soil Texture](https://github.com/Datalinker-Org/Farm-Data-Standards/blob/master/Irrigation%20and%20Effluent/IEDS_Lists-of-Enumerated-Values.md#Soil-Texture) in the Irrigation & Effluent Data Standard.
Top soil stony | Boolean
Top soil compacted | Boolean
Maximum rooting depth | Integer | cm
Depth to impeded drainage layer | Integer | cm
Non-standard layer | Enumeration | Sandy, Stony, Stony matrix
Drainage class | Enumeration | Well, Moderately well, Imperfect, Poor, Very poor
Hydrophobic condition | Enumeration | Rain always soaks in, Generally soaks in, Mostly runs off
Susceptibility to pugging | Enumeration | Rare, Occasional, Winter, Winter or rain
Drainage method | Enumeration | None, Mole/tile system, Other

#### Representative Soil Test Results for effective area	

Attributes | Data Types 
:--------- | :--------- 
pH | Float
Olsen P | Integer
Quick Test Mg | Integer
Quick Test Potassium | Integer
Soil test sulphate | Integer
