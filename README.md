# Air-Traffic-Analysis---Data-Analysis-in-Tableau

In our previous project: Air-Traffic-Analysis---Data-Analysis-in-SQL we explored using SQL queries to generate insights from a real-world dataset stored in a relational database. For this project, we will create data visualizations using Tableau, allowing the user to interactively derive business insights from the same dataset without having to write code.

The work we started for BrainStation Mutual Fund will be continued here, working with the same Air Traffic data set. Our goal will be to address each question below with an appropriate visual or dashboard in Tableau and provide quantitative comments and actionable insights based on our findings. Finally, our charts will be organized into a Tableau Story to deliver our insights as a professional presentation using a consistent narrative.

## Data Description
We have been provided with a cleaned version of data originally sourced from the open data portal at the Bureau of Transportation Statistics:
https://www.transtats.bts.gov/DatabaseInfo.asp?QO_VQ=EFD&DB_URL=

To load the necessary data required for this project, we downloaded the data file from https://api.brainstation.io/content/link/1HyDA2lldNXHAu5nJLPY3Y1yBAt8n7zrR?instanceId=6208 and follow the below steps: in MySQL Workbench, go to Server > Data Import, select 'Import from Self-Contained File', and specify 'AirTraffic' as the 'Default Target Schema'. 

The database contains two tables, flights and airports. The flights table contains flight data for 2018 and 2019 from the three most traveled airlines. The airports table contains data for all origin and destination airports, including full name and location. Details of each are as follows:

Table 1: flights

| **Column**                         | **Type**    | **Description**                                          |
|--------------------------------|--------|------------------------------------------------------|
| FlightID                      | int    | Unique ID number for each flight (Primary Key)      |
| FlightDate                    | date   | Date of flight departure                            |
| ReportingAirline              | string | DOT Unique Carrier Code                            |
| TailNumber                    | string | FAA Tail number identifying flight                 |
| FlightNumberReportingAirline  | string | Public flight number                               |
| OriginAirportID               | int    | Origin / departure airport code                   |
| DestAirportID                 | int    | Destination / arrival airport code                |
| CRSDepTime                    | string | Scheduled local departure time                    |
| DepTime                       | string | Actual local departure time                       |
| DepDelay                      | int    | Difference in minutes between scheduled and actual departure time |
| TaxiOut                       | int    | Taxi out time, in minutes                         |
| WheelsOff                     | string | Wheels off in local time                         |
| WheelsOn                      | string | Wheels on in local time                          |
| TaxiIn                        | int    | Taxi in time, in minutes                         |
| CRSArrTime                    | string | Scheduled arrival time                           |
| ArrTime                       | string | Actual arrival time                              |
| ArrDelay                      | int    | Difference in minutes between scheduled and actual arrival |
| Cancelled                     | int    | Cancelled indicator                              |
| Diverted                      | int    | Diverted indicator                               |
| AirTime                       | int    | Flight time (total time in the air) in minutes  |
| Distance                      | float  | Distance between airports in miles              |
| AirlineName                   | string | DOT full airline name                           |
| CancellationReason            | string | Reason for cancellation                         |

Table 2: airports

| **Column**     | **Type** | **Description**                       |
|----------------|----------|---------------------------------------|
| AirportID      | int      | Unique airport code (Primary Key)     |
| AirportName    | string   | Full name of airport                  |
