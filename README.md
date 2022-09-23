# Ford GoBike System Data Analysis
## by Ohiri Emeka Emmanuel


## Dataset

> This dataset was provided by Udacity for this project. Though, four datasets were provided with a choice to pick one among the four options and thus, I picked the **Ford Gobike Trip Data**. You can get the dataset on *https://video.udacity-data.com/topher/2020/October/5f91cf38_201902-fordgobike-tripdata/201902-fordgobike-tripdata.csv* or on kaggle.

> This data set includes information about individual rides made in a bike-sharing system covering the greater San Francisco Bay area and it is centered on 2019 only. This document explores a dataset containing about 183,000 bike records and 16 features that clearly show details of how bikes are shared amongst riders.

> There are two (2) columns that are of integer data type, seven (7) cloumns with a float data type and Seven (7) cloumns with an object data type. The data type of 2 columns with object data type was changed to date time as part of the quality issue. Another column named age was feature engineered from the member_birth_year column so as to get the age of riders (their respective years were substracted by the current year (2022).


> The analysis that follows is meant to find a trend or relationship among these features and then, find out what makes a rider likely want to share a bike.


## Summary of Findings


> The following features (duration_sec, member_gender, user_type, start_station_id, end_station_id, member_birth_year) are my features of interest which is meant to drive more insights on how they might likely affect a riders decision to share a bike. Feature engineering was done to create a new column (age, start_day and end_day) was were also added as part of my key features. Duration_sec when plot with the matplotlib hist plot was long tailed with few bars. Using a log scale plot, duration_sec was skewed to the right with higher peaks appearing between 500 - 1000k before a steady decline began to occur.

> A look at the member_birth_year, the histogram was skewed to the left with higher peaks on years around 2000. A feature engineering had to be done to determine why this frequency distribution was this way and so, *Age* column was created and thus, histogram distribution confirmed that persons of age between 20 - 30 years had more rides.

> A countplot was of start_day and end_day followed same distribution pattern. Thursday was seen to have more rides on both the start day and end day.

> In a bid to find out which user_type had the highest trip, a countplot was plotted and thus, subscriber users top the list of highest trips. A count plot of the member_gender was plotted to see the gender with higher trips, the plot showed the male gender topping the trips in the member category.

> Since we also had members who did not share their bike all through the trip, we plotted a count plot to see if those members who shared their bike had higher trips but we found out that they did not. A heatmap correlation plot was plotted to see the correlation between features but then, correlation amongst our interested features only saw one positive correlation between start_station_id and end_station_id. A negetive correlation was seen between member_birth_year and age (a negetive correlation of 100% which means the higher the age, the lower the year of birth. Correlation among features that weren't of interest was higher.

> The oldest rider was seen to be a female who did not share a bike and also in the customer user_type category who rode on Monday.




## Key Insights for Presentation


> Priority was given to riders that actually shared bike as we tried to understand why a rider would opt to share a bike during their trip. For the presentation, I focus on both the influence of the user_type and member_gender. I had earlier used countplot to see the pattern or spread of user types and gender on the entire dataset. I start by introducing the duration_sec variable, followed by the pattern in member_birth_year and age distribution, then plot the transformed scatterplot.

> Afterwards, I introduce each of the categorical variables one by one. To start, I use the box plots of duration and age on user_type, member_gender and bike_share_for_all_trip to see the spread. I'm only looking at the user_type and member_gender plot here since it's the clearest example of how the categorical columns affect riders decision to share a bike. The dataset was then split into two (shared_bike and shared_not).

> A seaborn facet grid was plotted with a scatter plot using the categorical columns (user_type and member_gender) as hue to determine the spread on each dataset after the split (share_bike and shared_not). This clearly showed the effect both categorical columns had on the analysis.

> Lastly, I wanted to see the distribution of duration_sec and age on bike_share_for_all_trip and so, I changed the datatype from object to column and use it as a hue on a scatter to see the relationship among them.