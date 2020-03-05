### Irrigation Practices and Systems

The following table defines items in entities that summarise irrigation. See the Irrigation and Effluent Data Standard for the full [Data Dictionary on irrigation and effluent](https://github.com/Datalinker-Org/Farm-Data-Standards/blob/master/Irrigation%20and%20Effluent/IEDS_Irrigation-and-Effluent-Data-Dictionary.md).

#### Irrigation on a block or farm

Attributes | Data Types | Notes
:--------- | :--------- | :----
Average irrigation interval	| Integer | Time taken for irrigator to return to its starting point or days taken to irrigate farm, days.
Method of irrigation | Enumeration | See [Irrigation Equipment Observations](https://www.youtube.com/watch?v=vMMbeaJV4HM#Irrigation-Equipment-Observations) in the Irrigation & Effluent Data Standard.
Area irrigated | Integer | Area expressed in m2 (SI unit) or hectares (ha, accepted non-SI unit). Implementations must clearly specify which unit is used, and ensure consistent use. For spatial data interchange m2 should be used<sup id="INSPIRE">[1](#f1)</sup>. 
Days irrigated | Integer | Number of days of season irrigated.
Total metered water	| Integer | m3
Instantaneous flow rate	| Integer | l/sec/ha
Flow rate | Integer | Flow rate for bore/borderdyke, l/sec
Crop irrigated | Enumeration | See [Type of Feed](https://github.com/Datalinker-Org/Farm-Data-Standards/blob/master/Pasture%20Graze%20and%20Feed/PGFDS_Lists-of-Valid-Values.md#Feed-Type).
Months irrigated | Enumeration |

#### Footnotes

<b id="f1">1.</b> See section 6.1.3 of D2.8.I.2 Data Specification on Administrative Units – [Technical Guidelines](https://inspire.ec.europa.eu/id/document/tg/au). [↩](#INSPIRE)
