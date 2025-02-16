# Gett Project
Insights from Failed Orders

## About
_This data project has been used as a take-home assignment in the recruitment process for the data science positions at Gett_.

Gett, previously known as GetTaxi, is an Israeli-developed technology platform solely focused on corporate Ground Transportation Management (GTM). They have an application where clients can order taxis, and drivers can accept their rides (offers). At the moment, when the client clicks the Order button in the application, the matching system searches for the most relevant drivers and offers them the order. In this task, we would like to investigate some matching metrics for orders that did not completed successfully, i.e., the customer didn't end up getting a car.

## Assignment
Please complete the following tasks.

1. Build up distribution of orders according to reasons for failure: cancellations before and after driver assignment, and reasons for order rejection. Analyse the resulting plot. Which category has the highest number of orders?
2. Plot the distribution of failed orders by hours. Is there a trend that certain hours have an abnormally high proportion of one category or another? What hours are the biggest fails? How can this be explained?
3. Plot the average time to cancellation with and without driver, by the hour. If there are any outliers in the data, it would be better to remove them. Can we draw any conclusions from this plot?
4. Plot the distribution of average ETA by hours. How can this plot be explained?

## Data Description
We have two data sets: **_data_orders_** and **_data_offers_**, both being stored in a CSV format. The **_data_orders_** data set contains the following columns:

- **_order_datetime_** - time of the order
- **_origin_longitude_** - longitude of the order
- **_origin_latitude_** - latitude of the order
- **_m_order_eta_** - time before order arrival
- **_order_gk_** - order number
- **_order_status_key_** - status, an enumeration consisting of the following mapping:
- **_4_** - cancelled by client,
- _**9**_ - cancelled by system, i.e., a reject
- **_is_driver_assigned_key_** - whether a driver has been assigned
- **_cancellation_time_in_seconds_** - how many seconds passed before cancellation
  
The **_data_offers_** data set is a simple map with 2 columns:

- **_order_gk_** - order number, associated with the same column from the orders data set
- **_offer_id_** - ID of an offer
