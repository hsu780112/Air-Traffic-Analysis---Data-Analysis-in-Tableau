# Air-Traffic-Analysis---Data-Analysis-in-Tableau

In our previous project: Air-Traffic-Analysis---Data-Analysis-in-SQL we explored using SQL queries to generate insights from a real-world dataset stored in a relational database. For this project, we will create data visualizations using Tableau, allowing the user to interactively derive business insights from the same dataset without having to write code.

The work we started for BrainStation Mutual Fund will be continued here, working with the same Air Traffic data set. Our goal will be to address each question below with an appropriate visual or dashboard in Tableau and provide quantitative comments and actionable insights based on our findings. Finally, our charts will be organized into a Tableau Story to deliver our insights as a professional presentation using a consistent narrative.

## Data Description
We have been provided with a cleaned version of data originally sourced from the open data portal at the Bureau of Transportation Statistics:
https://www.transtats.bts.gov/DatabaseInfo.asp?QO_VQ=EFD&DB_URL=

To load the necessary data required for this project, we downloaded the data file from https://api.brainstation.io/content/link/1HyDA2lldNXHAu5nJLPY3Y1yBAt8n7zrR?instanceId=6208 and follow the below steps: in MySQL Workbench, go to Server > Data Import, select 'Import from Self-Contained File', and specify 'AirTraffic' as the 'Default Target Schema'. 

The database contains two tables, flights and airports. The flights table contains flight data for 2018 and 2019 from the three most traveled airlines. The airports table contains data for all origin and destination airports, including full name and location. Details of each are as follows:

Table 1: flights

| **Project Component**              | **Description**                                                                                                                                                  |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Objective                      | Support investment decisions for BrainStation Mutual Fund in one of three major airline stocks.                                                                  |
| Data Sources                   | Flight and airport data                                                                                                                                            |
| Goals                          | 1. Address business questions to uncover insights on airline performance, efficiency, and operational strengths. <br> 2. Demonstrate advanced SQL skills.       |
| Deliverables                   | Clear, data-backed insights to inform fund managers' investment choices; demonstration of SQL proficiency.                                                        |
| Approach                       | Analyze data using SQL queries to extract actionable insights, answering the fund managers' business questions and ensuring high data handling proficiency.        |
| Expected Outcomes              | 1. Insightful guidance on each airline's performance and strengths. <br> 2. A demonstration of technical rigor and SQL expertise.                                 |

Table 2: airports

| **Column**     | **Type** | **Description**                       |
|----------------|----------|---------------------------------------|
| AirportID      | int      | Unique airport code (Primary Key)     |
| AirportName    | string   | Full name of airport                  |
