# General Assembly Project 1

## Problem Statement
***This project aims to see whether can we rely on Singapore's weather climate alone to successfully grow our own vegetables throughout the whole year?***

## Background
Malaysia accounts for 42% of the vegetables imports for Singapore (https://www.channelnewsasia.com/singapore/cna-explains-where-does-singapore-get-its-food-2709161). With the recent closure of the borders between Malaysia and Singapore due to the Covid-19 pandemic, and with the recent increase in the prices of vegetables in Malaysia due to the monsoon seasons, Singapore government is finding ways to increase our self-sustainability in producing our own vegetables (https://www.ura.gov.sg/Corporate/Resources/Ideas-and-Trends/feeding-the-city-growth-of-urban-agriculture). This is to reduce our heavy reliance on our neighbor for vegetables in the event of border closures or sudden increase in pricing of the vegetables.

According to the [Meteorological Services Singapore](http://www.weather.gov.sg/climate-climate-of-singapore/#:~:text=Singapore%20is%20situated%20near%20the,month%2Dto%2Dmonth%20variation.), Singapore has typical tropical climate with adundant rainfall, high and uniform temperatures and high humidity all year round, since its situated near the equator. There are many factors that help us understand the climate of a country and in this project we are going to look into a few, especially rainfall.

Singapore’s climate is characterised by two main monsoon seasons separated by inter-monsoonal periods.  The **Northeast Monsoon** occurs from December to early March, and the **Southwest Monsoon** from June to September.

## DataSets
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

## EDA (Exploratory and Data Analysis)
1) Check the summary statistics of the dataframe sg_climate.
![image](https://user-images.githubusercontent.com/120021810/211339471-3daa7082-bca8-47d5-a71a-325c8b47ce0f.png)

2) Creating a dictionary comprehension to apply standard deviation to each numeric column in the dataframe.
![image](https://user-images.githubusercontent.com/120021810/211341342-f1525e80-9bc9-416c-806d-6e9e3752198f.png)

3) Investigative trends using sort/mask (with .head():
 - September and February has the highest and lowest total rainfall for year 1990 respectively.
   November and September has the highest and lowest total rainfall for year 2000 respectively.
   July and February has the highest and lowest total rainfall for year 2010 respectively.
   May and February has the highest and lowest total rainfall for year 2020 respectively.
- Year 2006 and 2014 has the highest and lowest total rainfall for the date range of analysis
- For the year 1990, September and November have the same highest number of rainy days, whereas March has the lowest number of rainy days.
For the year 2000, November and May has the highest and lowest number of rainy days respectively.
For the year 2010, November and February has the highest and lowest number of rainy days respectively.
For the year 2020, July and January has the highest and lowest number of rainy days respectively.
- Year 2018 and 2014 has the highest and lowest number of rainy days for the date range of analysis.
- The outlier months for total rainfall for date range analysis are: Dec-1982, Feb-1984, Jan-1987, Nov-1989, Dec-1991, Nov-1992, Dec-1992, December-2001, Jan-2004, Dec-2006, Dec-2007, Jan-2011, Jan-2021. The outlier months for total rainfall for date range analysis are: Feb-1982, Feb-1987, Feb-2005, Feb-2019. There are no outliers for number of rainy days data.

## Conclusions
The Average Daily Mean Sunshine by Month barplot shows only February, March, April and July have Daily Mean Sunshine hours of at least 6 hours for proper vegetable farming, while the rest of the year has less than 6 hours of sunshine.

The Occurrences barplot shows that occurrences of a good conducive month within the date range of analysis is significantly  lower to that of not conducive month.

The Mean No. of Rainy Days by Month barplot shows that only February and March have Daily Mean Sunshine of at least 6 hours, wheares the rest of the year have less than 6 hours of Daily Mean Sunshine.

From the above points, it can be seen that only February and March are the conducive months to grow vegetables. We cannot grow vegeatbles constantly throughput the whole year. This is not effective in increasing our own vegetable production. 

In addition, from the Occurences Barplot, the occurrences of good conducive February and March are much lesser than that of the not conducive Febraury and March for the whote date range of analysis. So there is a high probablity February and March can also become not conducive for vegetable farming.

Moreover, only 2 out of 12 months are good for vegetables farming. Some vegetables require more than 3 months to grow successfully.

It is therefore reasonable to conclude that we **CANNOT** rely on Singapore Weather alone to successfully grow our own vegetables throughout the whole year.

## Recommendations
Proper UV lighting system installation is required to provide constant amount (6-8 hours) of daily sunshine hours throughout the whole year. 

There is a need to erect proper irrigation and reservoir systems. The reservoir will stored the rain water from those months with high number of rainy days or total rainfall. In turn, the reservoir will use the irrigation system to supply water to the vegetables. 

A proper drainage system is also required for months that have a high number of rainy days or total rainfall. Poor drainage can affect the growth of vegetables. [(source)](https://indiaagronet.com/indiaagronet/water_management/CONTENTS/Excess%20Water.htm)



 

