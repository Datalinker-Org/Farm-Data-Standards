### Feed and Growth Observations

1. [Liveweight](#Liveweight)
2. [Weaning](#Weaning)
3. [Progeny Weaned](#Progeny-Weaned)
4. [Feed Regime Change](#Feed-Regime-Change)
5. [Change Paddock](#Change-Paddock)
6. [Draft](#Draft)
7. [Body Measurements](#Body-Measurements)

#### Liveweight

A weight recorded on a live animal (as opposed to dead weight). Abbreviated “Weight” in many on-farm tools. 

Attribute | Data Type | Notes 
:-------- | :-------- | :----
Weight | Float | Weight in kg.
Equipment Model | String | Make, model, version used.
Precision | Integer | ± %
Coefficient of Variation | Float | Percentage (for a group).
Maximum Weight | Float | Weight in kg (for a group).
Mean Weight | Float | Weight in kg (for a group).
Minimum Weight | Float | Weight in kg (for a group).
Standard Deviation | Float | in kg (for a group).
Time off feed | [ISO](docs/ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) 8601 | period (hours/minutes).

#### Weaning

The act of removing young animals from being able to access milk. This causes a change in diet.

Attribute | Data Type | Notes 
:-------- | :-------- | :----
Pre-weaning Group | [URN](docs/ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) String | Group identifier.
	
#### Progeny Weaned

Removing progeny from the dams causes a change in demand and feeding regime for the dams.

Attribute | Data Type | Notes 
:-------- | :-------- | :----
Pre-weaning Group | [URN](docs/ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) String | Group identified.
Number Weaned | Integer | Count of progeny weaned.

#### Feed Regime Change

Records a change in a feed regime (for instance, onto or off a forage, or use of a supplementary feed). Often recorded for a group of animals.	

Attribute | Data Type | Notes 
:-------- | :-------- | :----
Feed Category | Enumeration | From [Feed Types](#Feed-Types).
Feed Name | Enumeration | See [Feed Types](#Feed-Types).
Crude Protein | Float | amount of total protein which can be metabolised from consuming the feed; kg/kg DM.
Digestibility | Float | The percentage of feed that is able to be digested.
Metabolisable Energy | Float | MJ ME/kg DM.
Feed Allowance Per Head | Float | kg DM per head.

#### Change Paddock

Also called “internal move” or “grazing” by some systems, this is a record of movement of an animal or group from one internal farm location (a paddock) to another. This is often recorded for a group of animals.	

Attribute | Data Type | Notes 
:-------- | :-------- | :----
Source Paddock | String | Identifier of the paddock from which animals were being moved.
Residual Pasture Cover | Float | kg DM/hectare remaining in source paddock.
Destination Paddock | String | Identifier of the paddock into which animals were being placed.
Destination Pasture Cover | Float | kg DM/hectare in destination paddock when animals are changed.
Tally | Integer | Count of animals involved.

#### Draft

Records that an animal was drafted in a certain direction (out a gate) or moved to another group.

Attribute | Data Type | Notes 
:-------- | :-------- | :----
Gate or Group | |	

#### Body Measurements

Records miscellaneous measurements made on an animal.

Attribute | Data Type | Notes 
:-------- | :-------- | :----
Measurement Type | Enumeration | Hip Height, Scrotal Circumference.
Measurement | Floating |
Measurement Units | Enumeration | mm, cm, m.

##### Feed Types

Feed categories are used to group the Feed Types as used in the Feed Regime Change observation in the Feed and Growth category. This list aligns to the Feed Type list in [Feed Types](docs/PGFDS_Lists-of-Valid-Values.md#Feed-Types) section of the Pasture, Grazing, & Feed Data Standard.

Valid values for Feed Type are:

Category | Attributes
:------- | :---------
Grains | Barley grain <br> Maize grain <br>Oats grain <br>Pea <br> Soya Bean Meal <br>Triticale grain <br> Wheat grain	<br> 
Straws | Barley Straw <br> Corn stover <br> Oat straw <br> Pea Straw <br> Ryegrass straw <br> Wheat Straw <br>
Green feeds | Annual ryegrass <br> Japanese millet <br>Kale <br>Lucerne <br> Maize <br> greenfeed <br>Oats leafy <br> Oats milky dough <br> Pasture <br> Rape <br> Rye corn <br> Sorghum <br> Sulla <br> Swedes <br> Triticale <br> Turnips	<br>
Processed | Avonfeed <br> Bran <br> Broll <br> Brewers grain <br> Canola <br> Copra <br> Corn grits (Hominy) <br> Cottonseed meal <br> Fishmeal <br> Lucerne meal <br> Molasses <br> Palm Kernel Extract <br> Pollard <br> Proliq <br> Tallow <br> Tapioca <br> Urea
Silage | Baleagev <br> Barley milky dough silage <br> Cereal silage <br> Cereal silage <br> Lucerne silage <br> Maize silage <br> Pasture silage <br> Sweetcorn silage <br> Triticale silage
Vegetable/Fruit | Apple pomace <br> Apples <br> Cabbage <br> Carrots <br> Citrus pulp <br> Grape pomace <br> Kiwifruit <br> Onions <br> Potato <br> Squash
Hay | Lucerne hay <br> Pasture hay