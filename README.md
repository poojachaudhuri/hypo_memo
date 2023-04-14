# 311 complaints related to heat and hot water

This project analyses 311 service requests related to heat and hot water from NYC Open Data. The time period for the data is 2020 to 2022. It explores the complaints on the zip code level. The data has been normalized by the zip code level population data gathered from U.S. Census Bureau.

## Guide to the repository ##

* `notebooks:` This folder contains all the python notebook. 

1. `census.ipynb` contains the code that was used make calls to the U.S. Census API.
Zip code level data on population, race, median income and percentage below poverty was collected for this project.
It must be noted that the U.S. Census Bureau releases estimates every year. It publishes American Community Survey (ACS) 5-year and 1-year data. 
ACS-5 released in the year 2020 and 2021 have been used for analysis. The data for 2022 is yet to be made available by the Bureau through the API. 
Therefore, 2021 data has been considered for 2022 in the analysis.

2. `exploratory.ipynb` contains the code used to run regression analysis to assess which variable causes a statistically significant change in the complaints.

3. `zip_codes.ipynb` contains the code used to scrape (www.nycbynatives.com/)[https://www.nycbynatives.com/nyc_info/new_york_city_zip_codes.php] for NYC zip codes.

* `docs:` This folder contains the parquet and csv files for the 311 data, census data and zip codes. 
 
* `images:` Contains all the images of the charts used in the html file. The images were generated using ai2html. 

## Findings ##

An analysis of the data revealed that the Bronx has the highest number of complaints boroughs in all the three years. In 2022, Bronx accounted for more than a third of the total complaints. Out of the top 10 addresses with the highest number of complaints in 2022, seven were in the Bronx. However, one address in Northwest Bronx - 2176 Tiebout Avenue - had a vastly outsized share, with over 3,000 complaints. This address accounts for a third of all the complaints from the Bronx zip code 10457. 

## Limitations ##

311 data may not give a picture of the ground reality. To infer that a certain zip code which has more complaints also has more violations related to heat and hot water can be misleading. There may be households that are not complaining despite facing issues, or some households may be complaining a lot of more than others. After speaking with a few residents of 2176 Tiebout Avenue, I found that the building has only 20 apartments. Over 3,000 complaints from a single building in a single years hints to the fact that there are households making multiple complaints. 311 data is not recorded at the apartment address level but building address level. 

Further ground reporting - which means talking to every resident of 2176 Tiebout Avenue - would give a clearer picture about the inflated number. 

