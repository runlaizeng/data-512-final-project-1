# Personized Hotel Recommendation ---- Final Project Plan

## Background
Online hotel reservation makes travel easier, But a large number of online hotel information also makes people become unable to follow. Planning a dream vacation or even a weekend escape can be an overwhelming affair. With hundreds, even thousands, of hotels to choose from at every destination, it's difficult to know which will suit our personal preferences. Should we go with an old standby with those pillow mints we like, or risk a new hotel with a trendy pool bar? 

A recommender system obviously can offer personalized suggestions by analyzing each user's preference by historical data from his/her account. However, the performance falls sharply when it encounters sparse data, especially meets a cold start user or the user just doesn't use an account. 

Since everyone would conduct the search action on the online reservation website, can we find a way to provide personalized hotel recommendations to travelers just based on the search action? Can we predict the hotel type customer will book? Can we calculate the probabilities that user will book a hotel or not? 

## Business Goals

This project has great benefits to both online hotel reservation companies and users.

For online hotel reservation companies:

- Gain complex insights into the customer and product bases. User behavior enables powerful analysis with business reports and dashboards generated on a regular basis. Such reports can predict possible problems so we can avoid them. 

- Increase the probability of discovering other interest. The result is increased loyalty and satisfaction of users with the web services. 

- Increase profits and conversion rate. Typically, users also interact with more hotels and this behavior leads to increased consumption and higher profits. Also, personalized recommendation encourage users to return, increase the frequency of visits by regular users, reduce churn and increase their lifetime value.

For users:

- Reduce the time required to find the hotel and significantly increase the effeciency of discovering other interest.

## Data Acquisition and Processing

### Data Acquisition

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

- is_mobile:	1 when a user connected from a mobile device, 0 otherwise	

- is_package:	1 if the click/booking was generated as a part of a package (i.e. combined with a flight), 0 otherwise

- channel:	ID of a marketing channel

- srch_ci:	Checkin date	

- srch_co:	Checkout date	

- srch_adults_cnt:	The number of adults specified in the hotel room

- srch_children_cnt:	The number of (extra occupancy) children specified in the hotel room	

- srch_rm_cnt:	The number of hotel rooms specified in the search	

- srch_destination_id:	ID of the destination where the hotel search was performed	

- srch_destination_type_id:	Type of destination	

- hotel_continent:	Hotel continent	

- hotel_country:	Hotel country	

- hotel_market:	Hotel market	

- is_booking:	1 if a booking, 0 if a click	

- cnt:	Numer of similar events in the context of the same user session

- hotel_cluster:	ID of a hotel cluster

### Hypothesis

We can analyze data using statistics method and machine learning method. Based on the variables above, some interesting problems and hypothesis we can go deep into are:

Using statistics method:
- Does booking result and hotel type result change by time?
- Do different destinations have impact on the final booking result?
- Will check-in date and check-out date influence the booking hotel type?
- Does Expedia has more mobile users or desktop users?
- Does user location influence the book result?
- If it's true that the more numer of similar events in the context of the same user session, the more possible that the user will book the hotel?

Using machine learning method:
- Can we predict the hotel type user will book?
- Can we predict the probability that user will book a certain type of hotels or not?

### Unknows and Dependencies

Since the data is a random selection from Expedia, so it is not representative of the overall statistics, some aggregation method like count and sum would make no sense.

We don't know how does Expedia form the hotel clusters. Expedia has in-house algorithms to form hotel clusters, where similar hotels for a search (based on historical price, customer star ratings, geographical locations relative to city center, etc) are grouped together. These hotel clusters serve as good identifiers to which types of hotels people are going to book, while avoiding outliers such as new hotels that don't have historical data.

Some user specific variables such as user gender, age, income may also have significant influence on the result, but we are lack of such data.

We can't evaluate the impact and performance of the model because companies pursue different goals and objectives. Many companies define and evaluate their key performance indicators (KPIs) on a regular basis simplifying the exact measurement of recommender impact. Such measurement is then realized by AB test, where personalized recommendations are provided to users in a group A whereas group B gets standard recommendations or best-selling content. But we are lack of such data.

## Human-Centered Aspects

- Terms of using datasets. Access to the dataset is subject to the [Kaggle Terms of Use](https://www.kaggle.com/terms) and [Rules](https://www.kaggle.com/c/expedia-hotel-recommendations/rules) of the competition.

- Privacy. Expedia has a privacy policy which informs the users about what information they collect from them, how they use the information, and with whom they will share the information. For details, please see [Expedia Privacy Policy](https://www.expedia.com/p/info-other/privacy-policy.htm).

- Bias of dataset. Since the data is a random selection from Expedia, so it is not representative of the overall statistics, and there would exist bias of the dataset.

- Algorithmic bias. Algorithmic bias would cause users reveiving recommendation of hotels they don't like.




