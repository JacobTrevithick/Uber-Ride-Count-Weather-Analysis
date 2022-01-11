# New York City Uber ride data analysis vs. weather patterns

## Description

This project analyzes New York City Uber ride data from 2014-2015 and attempts to prove if there are any statistically significant correlations between weather patterns and ride counts. Uber ride data is aggregated on a per hour basis using a Kaggle data set. This is correlated to weather reports in the same time frame using OpenWeatherAPI to get hour-by-hour weather reports including metrics such as: temperature, rain, snow, windspeed, etc. 

Our null hypothesis was that incliment weather would have no effect on ride count data. We could not safely reject the null hypothesis based on the findings.


## Initial data cleanup:

Uber data is cleaned and aggregated to generate ride count totals per hour so they can be correlated to weather reports (reported on an hourly basis). Uber data is given based on each individual ride with a given time stamp. This is converted to columns: Date and Hour (time) and grouped by the hour to give a total count per hour.

![Ride Count Dataframe](https://github.com/JacobTrevithick/Uber-Ride-Count-Weather-Analysis/blob/main/Images/Ride_count_df.png)

A similar process is done using the weather data retrieved from OpenWeatherAPI. This data is then combined with the ride count data to allow for analysis later on.

## Data Analysis and Findings:

### Should Uber focus their marketing, recruiting and pricing strategy based on weather?

Based on our findings, it does not seem like weather has much of an impact on ride count. We do not believe this would be a viable strategy for Uber to pursue. Correlations between ride counts and weather patterns were weak at best, and there is not sufficient data to determine if those correlations are directly related to weather patterns.

Additionally, other metrics may be more useful to track for marketing purposes than total ride count. The uber ride length or specific locations within New York City where the rides are starting may prove to be insightful metrics to track in maximizing profits.

### What are the underlying factors affecting ride count?

The three main underlying factors of our data that we explored were:
* The differences in rides experienced by time of day.
* The day of the week.
* And the differences from month to month.

The following 2014 heatmap gives a good overview of these factors as we started our exploration. 

![Heatmap 2014](https://github.com/JacobTrevithick/Uber-Ride-Count-Weather-Analysis/blob/main/Images/Heatmap_ridecount_over_day_and_hour_2014.png)

We were not surprised by the density in the afternoon, as that is a high traffic time in general; however the clustering during the weekdays was unexpected. It supports an idea that the primary use of Uber at the time was for traveling to and from work and not recreation (such as weekend drinks or tourists). Looking at the 2015 heatmap you can see a similar spread of rides, but you can see the recreation use may have increased with more density seen on the weekend in the “bar hours” (10pm - 2 am)

![Heatmap 2015](https://github.com/JacobTrevithick/Uber-Ride-Count-Weather-Analysis/blob/main/Images/Heatmap_ridecount_over_day_and_hour_2015.png)

Looking at the scale of rides the volume of rides increased dramatically over the year. The range between the years went from 250-2000 to 1000-60000. This change could also be seen by the following bar graphs showing the month to month growth Uber usage:

![Total Uber Pickups 2014 by month](https://github.com/JacobTrevithick/Uber-Ride-Count-Weather-Analysis/blob/main/Images/Total_Uberpickups_by_month_2014.png)

![Total Uber Pickups 2015 by month](https://github.com/JacobTrevithick/Uber-Ride-Count-Weather-Analysis/blob/main/Images/Total_Uberpickups_by_month_2015.png)

### What aspect of weather influences ride rate?

The initial outlook is that weather does not influence ride rate. Although there is a weak positive correlation between temperature and the number of ride counts, this is most likely due to Ubers increasing general popularity as a rideshare platform.

We also attempted to analyze how rain affected the ride rate. While the median ride count for rainy hours vs. sunny hours is slightly higher for 2014 and 2015, it is a minor difference and could be influenced by time of year and popularity of uber.

![Rides vs. temp daylight Hours 1pm](https://github.com/JacobTrevithick/Uber-Ride-Count-Weather-Analysis/blob/main/Images/Rides_vs_temp_1pm_2015.png)

![Rides vs. temp Saturdays 2015](https://github.com/JacobTrevithick/Uber-Ride-Count-Weather-Analysis/blob/main/Images/Rides_vs_temp_2015.png)

![Ride Counts in Sunny vs. Rainy Hours, 2014](https://github.com/JacobTrevithick/Uber-Ride-Count-Weather-Analysis/blob/main/Images/Ride_Counts_in_Sunny_vs_Rainy_hours_2014.png)

![Ride Counts in Sunny vs. Rainy Hours, 2015](https://github.com/JacobTrevithick/Uber-Ride-Count-Weather-Analysis/blob/main/Images/Ride_Counts_in_Sunny_vs_Rainy_hours_2015.png)


## Getting Started

### Technologies Used 

* Python
* Pandas
* Matplotlib
* Scipy

### Data Sources

* Kaggle Uber Ride Data: (https://www.kaggle.com/fivethirtyeight/uber-pickups-in-new-york-city?select=uber-raw-data-apr14.csv_) https://datasets.wri.org/dataset/globalpowerplantdatabase

* OpenWeather : https://home.openweathermap.org/history_bulks/new

## Authors

# Group:
Jacob Trevithick,
Marcus Potter,
Andrew Wilson,
Michael Bradberry

E: jacob.trevithick@gmail.com

Jacob's LinkedIn: [LinkedIn](https://www.linkedin.com/in/jacob-trevithick/)