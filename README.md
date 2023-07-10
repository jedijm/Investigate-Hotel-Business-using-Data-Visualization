# Investigate Hotel Business using Data Visualization

Dataset : Provided by Rakamin Academy 
<br>
Tools : Jupyter Notebook 
<br>
Programming Language : Python
<br>
<br>

## Project Background
<div align="justify"> Business Performance Analysis is fundamental to understand the business current condition. It is performed to identify the advantages and disadvantages of the company and putting it into consideration in order to handle it. In hotel business, it is used to indetify customer behaviours. One way to perform it is using Data Visualization from historical data to gather insights that might be useful for the business team. These insights is gathered by doing Exploratory Data Analysis and visualize them into graphs and figures to make it easier to understand them. In this project, the focus will be in analyzing the key factors of booking cancellation of customer. </div>

## Data Pre-Processing
The dataset is consisted of 29 columns & 119390 rows. It is hotel business data from 2017-2019.

Table 1. Data Pre-Processing Treatment <br>
**No**  |     **Treatment**      |    **Findings**     |    **Actions**     |
:-----: |    ----------------    |    ------------     |--------------------|
1 |   Handling Missing Values    |    Null Values are identified in few features : <br> 1. `company` (112.593 rows) <br> 2. `agent` (16.340 rows) <br> 3. `city` (488 rows) <br> 4. `children` (4 rows)    |- Replacing Null with 0 in `company`, `agent`,  `children`, <br> - Replacing Null with _Undefined_ in `city`|
2 |   Replacing Irrelevant Values     |    _Undefined_ values are identified in `meal`, `market_segment`, `distribution_channel`|- Replacing _Undefined_ in `meal` with _No Meal_, <br> - Replacing with the mode values from each features in `market_segment`, `distribution_channel` |
3 |    Dropping Unnecesary Values    |    There are 180 rows of booking data with 0 guest (`adult` + `children` + `babies` = 0)|Dropping the rows with 0 guest|

## Data Analysis
### Monthly Hotel Booking Analysis Based on Hotel Type
This analysis is performed to understand the booking pattern based on hotel type. The increase of booking will also increase potential income for the company. Thus, it is very important to understand the pattern.

![booking](assets/booking_order.png)
<div align="center"> Fig 1. Monthly Booking Order </div>
<div align="justify">Fig 1. shows that both hotel have a similar pattern, which increase in National Holiday Season (Mid Season & Year End). Mid Season is in May-July when the student at school and college is having semester break and also Ramadhan month for the Moslem. Meanwhile, Year End is in November-December which are Christmas and New Year holiday to gather with the family. Both hotel lowest month is in March. Throughout the year, City Hotel has a much bigger booking than Resort Hotel. Conversely, February & March is the lowest month where the number of holiday is less than other months. </div>
<br>

### Impact Analysis of Stay Duration on Hotel Bookings Cancellation Rate

<p align="center">
  <img src= "https://github.com/jedijm/Investigate-Hotel-Business-using-Data-Visualization/blob/main/assets/city_ratio.png"> <br>
Fig 2. City Hotel Bookings Cancellation Ratio
</p>
<p align="center">
  <img src= "https://github.com/jedijm/Investigate-Hotel-Business-using-Data-Visualization/blob/main/assets/resort_ratio.png"> <br>
Fig 3. Resort Hotel Bookings Cancellation Ratio 
</p>

<div align="justify"> Fig 2 & Fig 3 describe the cancellation ratio based on hotel. Both hotel show the cancellation percentage is lower than 50%. Resort hotel cancellation rate is 27.8% and City Hotel is higher at 41.8% which is considered high. The high cancellation rate in City Hotel is caused by high number of bookings also. Due to the close location from the residential area in the city, customer tends to book in City Hotel without long preparation and planning. On the opposite, Resort Hotel booking is usually planned well because of the distance to travel. </div>

![staying](assets/staying_duration.png)
<div align="center"> Fig 4. Staying Duration Impact to Booking Cancellation Rate </div>

<div align="justify"> Fig 4 shows the impact of staying duration to the booking cancellation rate based on each hotel types. Staying duration is categorized into 5 categories. Both hotels shows a similar pattern which is the longer stay duration, the higher cancellation rate. Except for the Resort Hotel with >4 weeks staying duration that has lower cancellation rate. The staying duration for <1 week is the least cancellation rate in both Hotels. City Hotel customer with >4 weeks staying duration has the highest cancellation rate for 90.9% which needs to be analyzed more to find the causing factors. The cancellation rate is highly influential to the business, thus it is necessary to improve this matter. </div> 
<br>

## Impact Analysis of Lead Time on Hotel Bookings Cancellation Rates

<p align="center">
  <img src= "https://github.com/jedijm/Investigate-Hotel-Business-using-Data-Visualization/blob/main/assets/lead_time.png"> <br>
Fig 5. Lead Time Impact on Hotel Bookings Cancellation Rate
</p>

<div align="justify">
  This analysis is done to understand the impact of Lead Time to bookings cancellation rate based on each hotels. Lead Time is the time interval between the booking and the time guest arrived. Lead time is categorized into months. City Hotel shows a significant increase of booking cancellation rate along with higher lead time with its peak at 12 months for more than 80%. This issue might be caused of the high activity of customers in the city, which caused unpredictable schedule especially in higher lead time. Meanwhile Resort Hotel does not show any significant influence due to lead time, it varies and peaked at 9 months for 50%. The best lead time shown is under 1 month for both hotels lower than 20%. Overall, lead time is more influential in City Hotel.
</div>

# Summary
<div align="justify">
  - Both hotels have a similar monthly booking pattern which increases in May-July (Mid Season) & November-December (Year End) that related to National Holiday Season. City Hotel booking order is higher than Resort Hotel's throughout the year. <br>
  - Staying duration and booking cancellation rate have a positive relation in both hotels except for Resort Hotel which has less cancellation in booking with more than 4 weeks duration. <br>
  - Lead time has a positive trend of booking cancellation rate for City Hotel with the peak at 12 months for more than 80%. Conversely, Lead time shows no significant influence to the booking cancellation rate of Resort Hotel because it varies without consistent pattern. 
</div>
