# pandas_challenge

### ETL-Project - Project Repository for the ETL Group project

---------------------------------------------------------------
#### Making personal branch:
- clone repo to local
- nav to repo, type in: git checkout -b <your_branch>
- to switch branches: git checkout <branch_name> 
- to upload to repo: git add .  -->  git commit -m "<a descriptive message>" --> git push origin <your_branch>
- Please let Austin know when you've pushed, merging will happen after.

2 data sources

Sources of data we will extract from: 
1.	Data Soft – Covid-19 Pandemic -Worldwide.
This is the data for the 2019 Novel Coronavirus Visual Dashboard operated by the Johns Hopkins University Center for Systems Science and Engineering (JHU CSSE). Also, Supported by ESRI Living Atlas Team and the Johns Hopkins University Applied Physics Lab (JHU APL).

2.	https://www.kaggle.com/eng0mohamed0nabil/population-by-country-2020
a.	Drop Columns
b.	Joining on population 

World Population and top 20 Countries Live Clock. Population in the past, present, and future. Milestones. Global Growth Rate. World population by Region and by Religion. Population Density, Fertility Rate, Median Age, Migrants. All-time population total.

Transformation of the data:
Data Soft – Covid-19 Pandemic -Worldwide:
•	Sub Zone and Location columns will be removed. Keeping Date, Zone, and Count.
•	The table appears to be a running total, so we will be sorting data by date descending to have most recent date.
•	Original plan – extract data using JSON – Complications {…}
Kaggle - Population by Country 2020: 
•	Several columns will need to be removed as they are not needed. Keeping Country and Population only. 
•	Population Data will be obtained utilizing .csv

Type of final production database data is loaded into:
We used a relational database (PostgreSQL) to link the data by our common identifier, Country.
Final tables/collections that we used in the production database:
•	New final table with found values by country. 
•	Total population and most recent confirmed Covid 19 stats. Do we want to categorize Deaths, confirmed, and Recovered?
o	Which countries have the highest rate of Covid 19 cases? 
Team Members: Austin, Rob, Paul, and Nick

Postgres database 
Building data-model and schema
