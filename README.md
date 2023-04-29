# 1. Introduction
This analysis is based on the Kaggle **data on Airbnb listings in 10 European cities**.
The project is focused on data exploration and visualization. 
It includes analysis of the data structure, summary statistics across cities, factors influencing listing prices and ratings.

# 2. Dashboard on Tableau
I created a dashboard for the DataFrame on Tableau Public:
https://public.tableau.com/app/profile/sayana.bashkueva/viz/Airbnbproject_16825376650690/AirbnbEurope

# 3. Scope of the project
The project is divided in the following parts:
* Importing the data and preprocessing
* Initial data inspection including summary statistics and correlation matrix
* Price analysis across days of the week. Is it more expensive to rent on weekends?
* Correlation between price and distances from the city center and metro station.
* How does Superhost status affect ratings and prices?
* Does cleanliness rating affect overall satisfaction rating? Do higher ranked listings tend to be more expensive?
* Conclusion

# 4. Dataset
Link to the Kaggle dataset: https://www.kaggle.com/datasets/thedevastator/airbnb-prices-in-european-cities

The initial datasets include 20 .csv files for different cities and days of the week (weekdays and weekends).
All of them have the same variables:
* realSum: The total price of accommodation for two people and two nights in EUR (Numeric) 
* room_type (Entire home/apt / Private room / Shared room): The type of accommodation (Categorical)
* room_shared: Whether the room is shared or not (Boolean)
* room_private: Whether the room is private or not (Boolean)
* person_capacity: The maximum number of people that can stay in the room (Numeric)
* host_is_superhost: Whether the host is a superhost or not (Boolean)
* multi: Whether the listing belongs to hosts with 2-4 offers (Boolean)
* biz: Whether the the listing belongs to hosts with more than 4 offers (Boolean)
* cleanliness_rating: The cleanliness rating of the listing (Numeric)
* guest_satisfaction_overall: The overall guest satisfaction rating of the listing (Numeric)
* bedrooms: The number of bedrooms in the listing (Numeric)
* dist: The distance from the city center in km (Numeric)
* metro_dist: The distance from the nearest metro station in km (Numeric)
* attr_index: Attraction index of the listing location (Numeric)
* attr_index_norm: Normalized attraction index (0-100) (Numeric)
* rest_index: Restaurant index of the listing location (Numeric)
* attr_index_norm: Normalized restaurant index (0-100) (Numeric)
* lng: Longitude of the listing location (Numeric)
* lat: Latitude of the listing location (Numeric)

During analysis all files were concatenated into one DataFrame and the following variables were added:
* price: Price per night in EUR (Numeric)
* city (Categorical)
* country (Categorical)
* day (weekday / weekend) (Categorical)

# 5. Used Python libraries
* pandas
* pandas_profiling
* numpy
* matplotlib.pyplot
* seaborn
* plotly.express
* phik
* phik.report
