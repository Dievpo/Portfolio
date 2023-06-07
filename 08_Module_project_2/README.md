# 08. Supervised Learning
## Project description
The customer of this study is the chain of hotels "Kak v gostyach".
To attract customers, this hotel chain has added the ability to book a room without prepayment on its website. However, if the client canceled the booking, then the company suffered losses. Hotel staff could, for example, buy groceries for the guest's arrival, or simply not have time to find another client.
To solve this problem, you need to develop a system that predicts armor rejection. If the model shows that the booking will be cancelled, then the client is asked to make a deposit. The deposit is 80% of the cost of the room for one day and the cost of one-time cleaning. The money will be debited from the client's account if he still cancels the reservation.
## Business metric and other data
The main business metric for any hotel chain is its profit. The profit of the hotel is the difference between the cost of the room for all nights and the cost of service: both during the preparation of the room and during the stay of the guest.
The hotel has several types of rooms. Depending on the type of room, the cost is per night. There are also cleaning costs. If the client rented a room for a long time, then they are cleaned every two days.
Hotel room rates:
- category A: per night - 1,000, one-time service - 400;
- category B: per night - 800, one-time service - 350;
- category C: per night - 600, one-time service - 350;
- category D: per night - 550, one-time service - 150;
- category E: per night - 500, one-time service - 150;
- category F: per night - 450, one-time service - 150;
- category G: per night - 350, one-time service - 150.
The hotel's pricing policy uses seasonal coefficients: in spring and autumn, prices increase by 20%, in summer - by 40%.
The loss of the hotel in case of cancellation of the room reservation is the cost of one cleaning and one night, taking into account the seasonal factor.
A budget of 400,000 was allocated for the development of a forecasting system. At the same time, it should be taken into account that the implementation of the model should pay off during the test period. Development costs should be less than the revenue that the system will bring to the company.
## Data Description
The hotel_train and hotel_test tables contain the same columns: 
- id — record number;
- adults - the number of adult guests;
- arrival_date_year — year of arrival;
- arrival_date_month — month of arrival;
- arrival_date_week_number — arrival week;
- arrival_date_day_of_month — day of arrival;
- babies - number of babies;
- booking_changes — number of order parameter changes;
- children - the number of children from 3 to 14 years old;
- country - citizenship of the guest;
- customer_type - customer type:
- Contract — an agreement with a legal entity;
- Group — group check-in;
- Transient - not associated with a contract or a group ride;
- Transient-party - Not associated with a contract or group stay, but associated with a Transient booking.
- days_in_waiting_list - how many days the order was waiting for confirmation;
- distribution_channel — order distribution channel;
- is_canceled - order cancellation;
- is_repeated_guest - a sign that the guest is booking a room for the second time;
- lead_time - the number of days between the date of booking and the date of arrival;
- meal — order options:
  - SC - no additional options;
  - BB - breakfast included;
  - HB - includes breakfast and lunch;
  - FB - includes breakfast, lunch and dinner.
- previous_bookings_not_canceled — the number of confirmed bookings for the client;
- previous_cancellations - the number of canceled orders from the client;
- required_car_parking_spaces - the need for a place for a car;
- reserved_room_type — reserved room type;
- stays_in_weekend_nights - number of nights during the weekend;
- stays_in_week_nights - number of nights on weekdays;
- total_nights - total number of nights;
- total_of_special_requests - the number of special marks.
## Project Structure
1.  Open data files  
2.  Pre-processing and exploratory data analysis  
    2.1  Data analysis and preprocessing    
3.  Formulation of an ML task based on a business task  
    3.1  A bit of theory  
    3.2  Let's calculate the profit   
4.  ML model development
    4.1  Feature selection
    4.2  Divide data into features and target feature
    4.3  Scaling numerical features
    4.4  Fighting imbalance
    4.5  Train different models and evaluate their quality
    4.6  Estimate the profit that the selected model will bring in a year
5.  Describe the portrait of an "unreliable" client
## Results
The project was completed:
- analyzed 2 datasets
- found unnecessary gaps in the data
- data types changed
- built graphs of the dependence of the cancellation of the reservation on the other parameters
- profit function written
- analyzed 3 potential models
- best model found
- model trained
- predicted the profit of the hotel for the year after the implementation of this model
- profit turned out to be more than 400,000 (as per task)
- found a portrait of an "unreliable" client
## Used tool stack
- python
- pandas
- numpy
- matplotlib
- seaborn
- sklearn
