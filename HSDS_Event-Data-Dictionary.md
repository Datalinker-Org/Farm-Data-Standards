### Event Data Dictionary

Contents:
* [Event Identification](#Event-Identification).
* [Event Attributes](#Event-Attributes).
* [Maintenance Event](#Maintenance-Event).
* [Inspection Event](#Inspection-Event).
* [Audit/Review](#Audit/Review).
* [Training](#Training).
* [Accident, Incident or Near Miss Event](#Accident,-Incident-or-Near-Miss-Event).
* [Event Details](#Event-Details).
* [Accident Description](#Accident-Description).
* [Preventative Action](#Preventative-Action).

An Event is used to describe a range of activities associated with the management of health and safety on farm. These events may be linked to people, locations, and features for which information is already recorded and is relevant to the event information. Note that the Notifiable event type is distinct from the Accident, Incident, or Near Miss Event in that the latter is for farm management purposes with no associated legal requirements or definitions. It is recommended that events [SHOULD](docs/HSDS_Definitions-and-Abbreviations_Interpretation.md#Interpretation) be recorded with a unique identifier to allow for the linking of events with other relevant farm data.

#### Event Identification

Attributes | Data Types | Notes
:--------- | :--------- | :----
Event Id | String | Unique identifier for the event.
Event Name | String | Name of the event.
Event Type | Enumeration | Audit/Review, Environmental, Maintenance, Inspection, Notifiable Event, ‘Accident, Incident or Near Miss, Training, Meeting, Report.
Event Date Time | [ISO 8601](docs/HSDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) | Date Time.
Event Location | URN Location Identifier | See [Location Identification](docs/ADS_Identification-of-Animals-Herds-and-Locations.md#Location-Identification).
Event Description | String | Description of the event.

#### Event Attributes

Attributes | Data Types | Notes
:--------- | :--------- | :----
Event Type | Attributes | Data Type and Notes

##### Maintenance Event	
Attributes | Data Types | Notes
:--------- | :--------- | :----
Feature ID | String | Identifier used to identify the feature. Refer Farm Features and Attributes Data Standard.
Feature Name | String | Name used to identify the feature. Refer Farm Features and Attributes Data Standard.
Asset Name | String | Name of the Asset (NOT required if Feature ID and/or Feature Name are used to identify the Asset).
Maintenance Due	| [ISO Date](docs/HSDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) | Maintenance Due Date.
Maintenance Organisation Name | String | 

##### Inspection Event
Attributes | Data Types | Notes
:--------- | :--------- | :----
Inspection Due | [ISO Date](docs/HSDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) | Maintenance Due Date.
Inspection Organisation Name | String

##### Audit/Review

Attributes | Data Types | Notes
:--------- | :--------- | :----
Review Organisation Name | String
Review Person | String |  Person ID or Name.
Review Note | String | 

##### Training

Attributes | Data Types | Notes
:--------- | :--------- | :----
Trainee | String | Person ID or Name.
Training Provider | String | Person ID, Person Name or Organisation.
Competent | Boolean | Describes if person is deemed competent in relevant activity after training.
Qualification Awarded | String | Name of Qualification Awarded.
Meeting	Attendees | String | Person IDs or Names in attendance.


#### Accident, Incident or Near Miss Event
These data fields relate to reports entered by a farmer as part of good health and safety management. They do not represent the information required of a legally Notifiable Event. See the SaferFarms Accident, Incident, or Near Miss report template for reference.

##### Event Details	

Attributes | Data Types | Notes
:--------- | :--------- | :----
Person ID | String | 
Person Name | String | 
Person Type | String | 
Time of Accident | [ISO 8601](docs/HSDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) | Date Time.
Date Reported | [ISO 8601](docs/HSDS_Definitions-and-Abbreviations_Interpretation.md#Definitions-and-Abbreviations) | Date 
Hours at Work | Integer | (Number of hours worked prior to accident / near miss).
Accident Location | String | 
Accident Severity | Enumeration | Near Miss, No Treatment, First Aid, Medical Treatment, Notifiable Event.

##### Accident Description

Attributes | Data Types | Notes
:--------- | :--------- | :----
Injury Type	| Enumeration | Strain/Sprain, Cut, Head Injury, Fracture/Break, Gradual Process, Bruising, Burns, Poison/Chemical, Multiple Injuries, No Injury.
Trained for Activity | Boolean | Is the person trained for task being performed.
Vehicle Involved | Boolean
Vehicle Type | String | Description of vehicle involved in accident.
Hazard Present | Boolean
Hazard Type | Enumeration | See [Location Identification](docs/ADS_Identification-of-Animals-Herds-and-Locations.md#Location-Identification).
Medical Needs Assessment | String |  Eg Able to continue full duties, Unable to work, Able to do light duties, Help available at home, Assistance required at home, Transport assistance needed.

##### Preventative Action

Attributes | Data Types | Notes
:--------- | :--------- | :----
Action Required	| String | Description of any preventative actions required.
