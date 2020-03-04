### Animal Observations

Contents:
* [Observations and Sampling](#Observations-and-Sampling)  
* [Observation Attributes](#Observation-Attributes)

#### Observations and Sampling

For the purpose of this Standard, an observation is the act or instance of viewing or noting a fact or occurrence for some scientific or other special purpose. Thus, an observation can include a note or record of an activity carried out, an event that has occurred, or a measurement taken.

The Open Geospatial Consortium describes observations<sup id="OGC">[1](#f1)</sup> as involving “sampling of an ultimate feature of interest”. In geographic terms, many features can only be “sampled”. However, with animals and particularly groups of animals, “sampling” is an important concept. It may be that only a sample of the animals in a mob is weighed, or that a device takes a sample of the fat or protein in milk at a moment in time.

An observation itself does not represent “state”. Instead an observation records sampling of the state of an animal at a point in time. As a result, an observation will not tell you when an animal lactated – only that at a point in time it was observed lactating, or that lactation was observed to begin or end. Changes to animal state ([Animal Life Data](ADS_Life-Data.md)) may be triggered by an observation, but the observation does not represent the state itself.

#### Observation Attributes

For the purposes of this Standard, the subject of an observation may be an individual animal, or a collective set of animals (such as a mob, herd, group, or session). 

For example, a weight may be recorded for an individual animal; a health treatment may be applied to an entire mob of animals (individually identified or not); or a movement may be recorded for a specific group of animals convened for that purpose (a session – see [Groups of Animals](ADS_Groups-of-Animals.md)). 

As a result, an essential part of recording and transmitting any observation must be an identification of the animal or animals to which it applies. This can be achieved through using the Animal ID attribute, described in [Animal Identification](ADS_Identification-of-Animals-Herds-and-Locations.md#Animal-Identification), or referencing the Herd or Flock as described in [Location Identification](ADS_Identification-of-Animals-Herds-and-Locations.md#Location-Identification).

The below items list the attributes relating to Animal Observations. All observations are observed or sampled at a point within time, so the record of an observation [SHALL](ADS_Definitions-And-Abbreviations_Interpretation.md#Interpretation) be accompanied by a date, or date and time, along with the Observation Category. The observation [SHOULD](ADS_Definitions-And-Abbreviations_Interpretation.md#Interpretation) also include a key, value, and label to define the observation item.

Attributes | Description | Cardinality | Type & Validation
:---| :----| :------ |:-----
Observation Category | The type of the observation recorded. | 1..n | Enumeration: Movement, Feed and Growth, Reproduction, Health, Test, Score
Observation Date | Date (and depending on observation, time) at which the observation was made. For some events, the time component of the observation is critical (for instance, a Milk Yield observation). For others, (such as condition score), the rate of change is slow enough that time is irrelevant. | 1 | [ISO](ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) 8601 date (and time)
Item Key | A key to identify the type of observation recorded, using the attributes listed under the Observation Category, i.e. Fate, Fate Reason. | 1 | String
Item Value | The value of the observation recorded. | 1 | Float
Item Label |A [URN](ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) string to list the internal label used to identify the observation or trait, i.e. BFATE for birth fate, or CS for condition score. | 1 | [URN](ADS_Definitions-And-Abbreviations_Interpretation.md#Definitions-And-Abbreviations) String

##### Footnotes

<b id="f1">1</b> OGC: [Observations and Measurements](https://www.opengeospatial.org/standards/om) [↩](#OGC)
