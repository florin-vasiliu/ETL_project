# ETL_Project

## OBJECTIVE
The purpose of our project was to extract two different data sets from two independent sources to understand the relationship (if any) between the average household income and the number of fast food restaurants throughout the United States. 


## EXTRACTION PROCESS:
We extracted the average household income from Census.gov and we retrieved the number of fast food restaurants from Data World.  In order to join these two data sets by a common key, a list of fips codes was obtained from a third data set from the FCC website using the given latitude and logitude for each fast-food restaurant.  See links below for our three data sets:

1) https://api.census.gov/data.html
2) https://data.world/datafiniti/fast-food-restaurants-across-america/workspace/file?filename=Datafiniti_Fast_Food_Restaurants.csv
3) https://geo.fcc.gov/api/census/#!/area/get_area

## TRANSFORM PROCESS:
After extracting all data sources, we then transformed the datasets in order to disguard the irrelevant data as follows:

1) We removed the duplicate header row, renamed columns, and reset the index and sorted by the State FIPS code from the Census data.  The State FIPS code was the unique primary key needed to join both data sets.

2) We selected 6 out of the total 21 columns from the restaurant data and renamed some of the columns.
