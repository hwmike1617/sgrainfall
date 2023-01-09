# General Assembly Project 1

## Problem Statement
***This project aims to see whether can we rely on Singapore's weather climate alone to successfully grow our own vegetables?***

## Background
Malaysia accounts for 42% of the vegetables imports for Singapore (https://www.channelnewsasia.com/singapore/cna-explains-where-does-singapore-get-its-food-2709161). With the recent closure of the borders between Malaysia and Singapore due to the Covid-19 pandemic, and with the recent increase in the prices of vegetables in Malaysia due to the monsoon seasons, Singapore government is finding ways to increase our self-sustainability in producing our own vegetables (https://www.ura.gov.sg/Corporate/Resources/Ideas-and-Trends/feeding-the-city-growth-of-urban-agriculture). This is to reduce our heavy reliance on our neighbor for vegetables in the event of border closures or sudden increase in pricing of the vegetables.

According to the [Meteorological Services Singapore](http://www.weather.gov.sg/climate-climate-of-singapore/#:~:text=Singapore%20is%20situated%20near%20the,month%2Dto%2Dmonth%20variation.), Singapore has typical tropical climate with adundant rainfall, high and uniform temperatures and high humidity all year round, since its situated near the equator. There are many factors that help us understand the climate of a country and in this project we are going to look into a few, especially rainfall.

Singapore’s climate is characterised by two main monsoon seasons separated by inter-monsoonal periods.  The **Northeast Monsoon** occurs from December to early March, and the **Southwest Monsoon** from June to September.

## DataSet
1) rainfall-monthly-total.csv (provided by General Assembly).
This dataset shows the monthly total rainfall from Jan-1982 till Aug-2022.

2) rainfall-monthly-number-of rain-days.csv (provided by General Assembly).
This dataset shows the number of rainy days in a month from Jan-1982 till Aug-2022.
  
3) sunshine-duration-monthly-mean-daily-duration.csv (provided by NEA.gov.sg 
website https://data.gov.sg/dataset/sunshine-duration-monthly-mean-daily-duration).
This dataset shows the monthly mean daily sunshine duration(hours) from Jan-1982 till Nov-2022. 

## Outside Research
1) Singapore source of food. The article cited shows where a large supply of our vegetables come from.

   https://www.channelnewsasia.com/singapore/cna-explains-where-does-singapore-get-its-food-2709161

2) Singapore urban farming to be more self-reliant. Singapore government is trying out rooftop farming with the help of residents to increase our vegetables production.

   https://www.ura.gov.sg/Corporate/Resources/Ideas-and-Trends/feeding-the-city-growth-of-urban-agriculture

3) Amount of water requirements. the article recommends an inch of water per week which roughly translates to 
   4inches (101.6mm) per month.
   
   https://www.creativevegetablegardener.com/watering-vegetable-garden/

4) Amount of Sunlight requirements. The article describes 6 to 8 hours of sunlight is recommended.

   https://www.gardenary.com/blog/how-much-sun-does-a-vegetable-garden-need
   
5) Number of days required to grow vegetables. The number of days to grow leafy vegetables ranges from 1.5 to 3 months.

   https://www.nparks.gov.sg/nparksbuzz/dec-issue-2021/gardening/growing-five-leafy-vegetables

## Data Import and Cleaning
1) Using pandas.read_csv to import each othe three datasets.
2) Check for null values in each of the three datasets.
3) Check for the info of each of the three datasets.
4) Pandas merge all three dataset into one single dataframe:-sg_climate.
5) Using pandas.to_datetime to spilt the month column into separate month and year columns.
5) Export the cleaned dataframe using pandas.to_csv to sg_climate_cleaned.csv

## Data Dictionary
#### Data Dictionary for the datasets chosen

|Feature|Type|Dataset|Description|
|---|---|---|---|
|total_rainfall|float|rainfall-monthly-total|Total rainfall in mm|
|no_of_rainy_days|int|rainfall-monthly-number-of-days|Total number of rainy days in a month|
|mean_sunshine_hours|float|sunshine-duration-monthly-mean-daily-duration|Monthly mean daily sunshine hours|


![heatmap](https://hwmike.w3spaces.com/sgrainfall/heatmap.jpg?bypass-cache=54808365)

![daily mean sunshine corr](https://hwmike.w3spaces.com/sgrainfall/daily_mean_sunshine_corr.jpg?bypass-cache=55469180)

## EDA (Exploratory and Data Analysis)
1) Check for any null values in the data


 

It has the following fields:

*1. Order_ID:*  This is the unique of the order made
*2. Pizza_name:* Name of the pizza
*3. Date:* Date of transaction

## Problem Statememt

e;ofiwu [owcugrpqeiov j'qeop po


## Data Engineering / Transformation
jksakljg ejrq hpqihj q'eroi 



*1. Descriptive*

df.describe
mean, max, min
value_counts

*2 Visualisation*
