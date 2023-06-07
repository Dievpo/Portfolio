# 04. Statistical data analysis
## Project description
Megaline is a federal mobile operator. Clients are offered two tariff plans: "Smart" and "Ultra". To adjust the advertising budget, the commercial department wants to understand which tariff brings in more money.
It is necessary to make a preliminary analysis of tariffs on a small sample of customers. At your disposal are the data of 500 Megaline users: who they are, where they are from, what tariff they use, how many calls and messages each sent in 2018. It is necessary to analyze the behavior of customers and draw a conclusion - which tariff is better.
## Tariff Description
- Tariff "Smart"
1. Monthly fee: 550 rubles
2. Included 500 minutes of talk, 50 messages and 15 GB of internet traffic
3. The cost of services above the tariff package:
   3.1 Minute of conversation - 3 rubles. The number of minutes and megabytes used by Megaline always rounds up. If the user spoke for only 1 second, a whole minute is counted in the tariff.
   3.2 Message - 3 rubles.
   3.3 1 GB of Internet traffic - 200 rubles.
- Tariff "Ultra"
1. Monthly fee: 1950 rubles
2. Included 3000 minutes of calls, 1000 messages and 30 GB of internet traffic
3. The cost of services above the tariff package:
   3.1 Minute of conversation - 1 ruble.
   3.2 Message - 1 ruble.
   3.3 1 GB of Internet traffic: 150 rubles.
## Data Description
Table 'users' - information about users:
- user_id
- first_name
- last_name
- age — user's age (years)
- reg_date — tariff connection date (day, month, year)
- churn_date — date of termination of using the tariff (if the value is omitted, it means that the tariff was still valid at the time of uploading the data)
- city — user's city of residence
- tarif — tariff plan name

Table 'calls' - information about calls:
- id - unique call number
- call_date — call date
- duration — call duration in minutes
- user_id — identifier of the user who made the call

Table 'messages' - information about messages:
- id - unique call number
- message_date — message date
- user_id - ID of the user who sent the message

Table 'internet' - information about internet sessions:
- id — unique session number
- mb_used - the amount of Internet traffic spent per session (in megabytes)
- session_date — internet session date
- user_id - user ID

Table 'tariffs' — information about tariffs:
- tariff_name — tariff name
- rub_monthly_fee — monthly subscription fee in rubles
- minutes_included - the number of minutes of conversation per month included in the subscription fee
- messages_included - number of messages per month included in the subscription fee
- mb_per_month_included - the amount of Internet traffic included in the subscription fee (in megabytes)
- rub_per_minute - the cost of a minute of conversation in excess of the tariff package (for example, if the tariff includes 100 minutes of conversation per month, then a fee - will be charged from 101 minutes)
- rub_per_message - the cost of sending a message in excess of the tariff package
- rub_per_gb - the cost of an additional gigabyte of Internet traffic in excess of the tariff package (1 gigabyte = 1024 megabytes)

## Project Structure
1.  Open the data file and study the general information  
2.  Prepare the data   
3.  Data analysis and revenue calculation
4.  Hypothesis testing 
## Used tool stack
- python
- pandas
- numpy
- seaborn
- matplotlib
- scipy
