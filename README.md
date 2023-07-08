# Investigate Hotel Business using Data Visualization

Dataset : Provided by Rakamin Academy 
<br>
Tools : Jupyter Notebook 
<br>
Programming Language : Python
<br>
<br>

## Project Background
Business Performance Analysis is fundamental to understand the business current condition. It is performed to identify the advantages and disadvantages of the company and putting it into consideration in order to handle it. In hotel business, it is used to indetify customer behaviours. One way to perform it is using Data Visualization from historical data to gather insights that might be useful for the business team. These insights is gathered by doing Exploratory Data Analysis and visualize them into graphs and figures to make it easier to understand them. In this project, the focus will be in analyzing the key factors of booking cancellation of customer.   

## Data Pre-Processing
The dataset is consisted of 29 columns & 119390 rows.

Table 1. Data Pre-Processing Treatment <br>
**No**  |     **Treatment**      |    **Findings**     |    **Actions**     |
:-----: |    ----------------    |    ------------     |--------------------|
1 |   Handling Missing Values    |    Null Values is identified in few features : <br> 1. `company` (112.593 rows) <br> 2. `agent` (16.340 rows) <br> 3. `city` (488 rows) <br> 4. `children` (4 rows)    |- Replacing Null with 0 in `company`, `agent`,  `children`, <br> - Replacing Null with _Undefined_ in `city`|
2 |   Replacing Irrelevant Values     |    _Undefined_ values are identified in `meal`, `market_segment`, `distribution_channel`|- Replacing _Undefined_ in `meal` with _No Meal_, <br> - Replacing with the mode values from each features in `market_segment`, `distribution_channel` |
3 |    Dropping Unnecesary Values    |    There are 180 rows of booking data with 0 guest (`adult` + `children` + `babies` = 0)|Dropping the rows with 0 guest|

## Data Analysis
### Monthly Hotel Booking Analysis Based on Hotel Type
This analysis is performed to understand the booking pattern based on hotel type. It is used to understand the monthly booking 

