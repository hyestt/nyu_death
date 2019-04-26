# nyu_death
Analyze the relationship between county, region, death rate and race in New York State


# Purpose and Target 
Annual Population Estimates for New York State and Counties: Beginning 1970
https://dev.socrata.com/foundry/data.ny.gov/krt9-ym2k
Vital Statistics Deaths by Resident County, Region, Place of Death: Beginning 2003
https://health.data.ny.gov/Health/Vital-Statistics-Deaths-by-Resident-County-Region-/v6zf-ydez

I want to analyze the relationship between county, region, death rate and race. However, the vital statistics dataset only contains death number. Therefore, I decide to merge the annual population dataset together so I can get the total population, which can be used as denominator while calculating the death rate. (Death rate  = Death number / Total Population )

# Data preprocessing and data cleaning
Before merging Annual Population and Vital Statistics Deaths dataset, I need to select the common part of both and make both data format the same.  I selected year 2003-2008, the year for which the population is calculated and delete the rows when race_ethnicity_description equal to ‘Total’ . 
Then I join the two datasets together at a county level. There are 62 counties in new York state. New York City, which includes the five counties of Bronx, Kings (Brooklyn), New York (Manhattan), Queens. According their geographic location, I separated them into 5 different clusters – NyCity, Mid, East, South ,and West. 



Descriptive Analysis and Finding
Between 2003 and 2008, Hispanic people accounted for 99.83 percent of deaths compared to other race. 
Between 2003 and 2008, there were 899,518 total deaths out of which 32.2% from New York city, 27.8% from South, 19.6% from West, 9.% from East and 10.6% were coming from Mid. 
The average death rate during 6 yeas was 0.79 percent. New York City had lowest death rate 0.68 perent compared to the highest death rate 0.95 percent in south area.  
In each year, the order of pupulation from highest to lowest remained the same: NyCity, South, West, Mid and East. New York City had the largest population as well as deaths number.
In 2003, Montgomery, Herkimer, and Greene were the counties with highest death rate. In 2008, Hamilton , Montgomery, and Chemung were the counties with highest death rate.  From 2004 to 2008, Hamilton and  Montgomery were the counties with highest death rate. 

# Result
In this project, I analyzed the relationship between population, deaths, geographic and race at a county level or a year level using SODA.api to combine two datasets from New York State Open Data. 
After analyzing the whole datasets, I learned lots of demographics information of New York State. One of the most astounding finding for me is the extremely high death rate of Hispanic people. I would try to dive deeper and find the reason behind the data. 
