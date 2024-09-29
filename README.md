Luwate Inda  
[**Tableau Dashboard**](https://public.tableau.com/app/profile/luwate.inda/viz/visualisations_17273113422640/CandidateAircraftDashboard?publish=yes)  
[**Github Repository**](https://github.com/Luwate/dsc-phase-1-project)  
[**Medium Article**](https://medium.com/@luwate)

# Overview 
Royal Air is a modern airliner, which takes a novel approach to airlines. Ditching the notion that an airline must either target the private or commercial space, Royal Air has carved a niche for itself by effectively serving both sets of clients. As a result of this, the airline has seen rapid growth and now seeks to grow its fleet of aircraft in order to scale operations.

# Business Objectives 
## Problem Statement  
Due to the growing demand Royal air has experienced, there is a need to acquire more aircraft, for both its commercial and private operations, in order to match this demand. This project aims to analyse accident data and through this, determine which aircraft would be the most appropriate option based on safety criteria.

## Expected Benefits
Through the successful completion of this project, Royal Air can expect to be able to make a data-driven decision when purchasing new aircraft which will be the most appropriate in terms of safety criteria.

## Business Success Criteria  
Success of the project will be evaluated through recommendation of the safest aircraft for the airline to purchase.

## Assessment 
The data available consists of aviation accidents between 1962 and 2023 collected by the National Transportation Safety Bureau (NTSB).  
The most prominent risk of this project would be the scope. This is because the recommendation will be based solely on aircraft safety and does not include other factors which may be important such as fuel consumption. In addition, the data does not contain all aircraft in service and instead only has aircraft that have been involved in accidents or incidents of some sort. Therefore, there is the possibility that the most appropriate aircraft is one that is not in the data as it may have not been involved in any event recorded by the NTSB. In order to mitigate this risk, further studies should be done to evaluate aircraft based on other metrics.

## Project Goals

* Clean data in order to remain with only relevant aircraft.  
* Analyse the data based on safety criteria  
* Identify the safest aircraft  
* Make final recommendations 

## Project Success Criteria 
The project will be considered a success upon completion of analysis of the data and two aircraft are selected to satisfy both commercial and private aviation sides of the business and recommendations made.

## Data Understanding

The data provided by the NTSB consists of 90348 rows and 31 columns. It contains features such as: Aircraft Make and Model, as well as information about casualties as a result of aircraft related Events (incidents or accidents). 

## Data Preparation  
The dataset is quite extensive with several features which are not relevant to the scope of this project, thus during the cleaning process, several of these columns will be ignored, however in the case that they contain a significant amount of null values. The columns dropped from the dataset include:  \['FAR.Description','Latitude', 'Longitude', 'Airport.Code', 'Airport.Name', 'Schedule', 'Air.carrier', 'Broad.phase.of.flight', 'Report.Status', 'Publication.Date'\].

Imputation has been done on the column: ‘Aircraft.Category’ column in order to remove missing values as about 65% of the values were missing. Usually, this may be better to drop, however as it contains important information, “Other” is imputed into missing values. In addition to this, all rows with values for ‘Aircraft.Category’ that are different from “Airplane”, “Unknown” and “Other” are dropped as they are not relevant to the study.

In addition, imputation is also done on the column, ‘Purpose.of.Flight’ as this is an important column to isolate the data for private and commercial flights. “Unknown” is placed in rows with missing values.

For the following columns with missing values, the median is impute into rows with missing values \[‘Total.Fatal.Injuries’, ‘Total.Serious.Injuries’, ‘Total.Minor.Injuries’, ‘Total.Uninjured’, ‘Number.of.Engines’\].

Using the columns: \[‘Total.Fatal.Injuries’, ‘Total.Serious.Injuries’, ‘Total.Minor.Injuries’, ‘Total.Uninjured’\], a new column ‘Total.Souls’ is created. This is used to calculate the total number of people onboard the aircraft during the Event.

   
## Recommendations 
With safety as the primary consideration, the airline should purchase a Boeing 757 for its commercial fleet. The aircraft has an average of zero fatalities and less serious injuries than its main competitor, the Airbus A320, over significantly more events. The aircraft is battle-proven and for these reasons, it is the most compelling option.

For the private aviation arm of the airline, a Dassault Falcon 900 should be acquired. This aircraft has not only never recorded a fatality as a result of an event, but it has never recorded a single injury as a result of an Event. This makes it an ideal choice when considering a private aircraft from a safety standpoint.

There could be aircraft which have had a large number of total souls and zero casualties. This could be considered safer than an aircraft that has been involved in numerous events, even though it may have identical survivability. Thus additional studies are strongly recommended.

	