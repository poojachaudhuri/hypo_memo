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

3. `zip_codes.ipynb` contains the code used to scrape [www.nycbynatives.com/](https://www.nycbynatives.com/nyc_info/new_york_city_zip_codes.php) for NYC zip codes.

* `docs:` This folder contains the parquet and csv files for the 311 data, census data and zip codes. The file used for statistical analysis is `data_cleaned_long.csv`.

