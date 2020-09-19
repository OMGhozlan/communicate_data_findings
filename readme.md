# 2020 Bay Wheels Ride Data Exploration and Visualization
## by Osama Ghozlan


## Dataset

[Bay Wheels](https://en.wikipedia.org/wiki/Bay_Wheels) (formerly known as Ford GoBike) is the first regional public large-scale bicycle sharing system in California's San Francisco Bay Area and on the West Coast of the United States. It was established as Bay Area Bike Share in August 2013. As of January 2018, the Bay Wheels system had over 2,600 bicycles in 262 stations across San Francisco, East Bay and San Jose. Each trip data is anonymously collected and includes details such trip duration, start/end Time and date and so on. The dataset used for this exploratory analysis consists of [monthly individual trip data](https://www.lyft.com/bikes/bay-wheels/system-data) from January 2020 to August 2020 in CSV format covering the greater San Francisco Bay area which are available [here](https://s3.amazonaws.com/baywheels-data/index.html).

##### Data wrangling process:
>* Setting multiple fields to the correct data type such as `start_time`, `end_time` were converted as datetime type, `user_type` set as a categorical data type and so on
>* Added features for analysis and exploration such as `started_at_hour`, `started_at_day`, `started_at_month` which were all derived from the `start_time` and `trip_distance` (in KMs) was calculated based on the coordinates of the start and end stations `start_lng`, `start_lat`, `end_lng` and `end_lat`
>* Filtered out outlier trip durations and distances from visual examination of the data and the statistical percentile
>* Made a day categorical type and cast `started_at_day` to that category data type
>* Made a month categorical type and cast `started_at_month` to that category data type


## Summary of Findings

The number of trips peaked around 7:00-9:00AM and 4:00-6:00PM with more trips being on work days (Monday-Friday) compared to weekends. Summar time was the most popular season of a year, likely due to the weather. The riding trips tend to be shorter on Monday through Friday compared to weekends. It indicates a pretty stable and efficient usage of the bike sharing system on normal work days, while more casual flexible use on weekends.

There is more subscriber usage in general than customers. The popular hours for the customers were around 11:00AM to 3:00PM which is rather strange given that this period of time is considered as the rush hour(s) however, this year was under different circumstances than the previous years as a result of COVID-19. Subscribers appear to use the bike system as a method of transportation to their jobs while customers uses it for leaisure/sport/activity. Subscriber usage was at the peak on rush hours (going to work and getting off work) which was very prevalent in the first three months (before the lock down) which reemphasized that their primary usage was for commuting unlike customers as stated earlier


## Key Insights for Presentation

The difference in the usage behaviour between the two user types is revealed from the exploration. Subscribers use the system heavily on work days whlist customers tend to ride more often on weekends, especially in the afternoon. The majority of trips concentrated around 7:00-9:00AM and 4:00-6:00PM on work days for subscribers, yet customers tend to use more in the late afternoon around 17pm Monday to Friday. The efficient/short period of usage for subscribers in addition to their high concentration on rush hours Monday through Friday, reaffirms that the bike usage is primarily for work commute. The more relaxing and flexible pattern of customer use shows that they're taking advantage of the bike sharing system quite differently from the subscribers, heavily over weekends and in the afternoon, for city tour or leisure purpose probably.