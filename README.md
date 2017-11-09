# Final Project Plan

## Background
Online hotel reservation makes travel easier, But a large number of online hotel information also makes people become unable to follow. Planning a dream vacation or even a weekend escape can be an overwhelming affair. With hundreds, even thousands, of hotels to choose from at every destination, it's difficult to know which will suit our personal preferences. Should we go with an old standby with those pillow mints we like, or risk a new hotel with a trendy pool bar? 

A recommender system obviously can offer personalized suggestions by analyzing each user's preference by historical data from his/her account. However, the performance falls sharply when it encounters sparse data, especially meets a cold start user or the user just doesn't use an account. 

Since everyone would conduct the search action on the online reservation website, can we find a way to provide personalized hotel recommendations to travelers just based on the search action? Can we predict the hotel type customer will book? Can we calculate the probabilities that user will book a hotel or not? If we can solve these problems, online hotel reservation websites can provide recommendations just based on the search conducts, which will significantly reduce the time cost of choosing a desirable hotel for users.

## Data Acquisition and Processing
The dataset I'm going to use is from [Expedia Hotel Recommendations Competition on Kaggle](https://www.kaggle.com/c/expedia-hotel-recommendations/data).

The dataset is the logs of customer search behavior from Expedia of year 2013 and 2014, including what customers searched for, how they interacted with search results (click/book), whether or not the search result was a travel package. The data is a random selection from Expedia and is not representative of the overall statistics.

The training dataset includes variables such as:

- date_time:	Timestamp	

- site_name:	ID of the Expedia point of sale (i.e. Expedia.com, Expedia.co.uk, Expedia.co.jp, ...)

- posa_continent:	ID of continent associated with site_name	

- user_location_country:	The ID of the country the customer is located	
- user_location_region:	The ID of the region the customer is located	
- user_location_city:	The ID of the city the customer is located	
- orig_destination_distance:	Physical distance between a hotel and a customer at the time of search. A null means the distance could not be calculated	
- user_id:	ID of user
- is_mobile	1 when a user connected from a mobile device, 0 otherwise	tinyint
- is_package	1 if the click/booking was generated as a part of a package (i.e. combined with a flight), 0 otherwise
- channel	ID of a marketing channel	int
- srch_ci	Checkin date	string
- srch_co	Checkout date	string
- srch_adults_cnt	The number of adults specified in the hotel room	int
- srch_children_cnt	The number of (extra occupancy) children specified in the hotel room	int
- srch_rm_cnt	The number of hotel rooms specified in the search	int
- srch_destination_id	ID of the destination where the hotel search was performed	int
- srch_destination_type_id	Type of destination	int
- hotel_continent	Hotel continent	int
- hotel_country	Hotel country	int
- hotel_market	Hotel market	int
- is_booking	1 if a booking, 0 if a click	tinyint
cnt	Numer of similar events in the context of the same user session	bigint
- hotel_cluster	ID of a hotel cluster

## Human-Centered Aspects
