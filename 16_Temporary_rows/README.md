# 16. Temporary rows
# Forecasting taxi orders
## Project description
The company "Chetenkoe Taxi" has collected historical data on taxi orders at airports. 
To attract more drivers during peak load, you need to predict the number of taxi orders for the next hour. 
Build a model for such a prediction.
The value of the RMSE metric in the test sample should be no more than 48.
## Data description
The data is in the taxi.csv file. The number of orders is in the num_orders column ("number of orders").
## Project Structure
1. Preparation
	1.1 Import of necessary libraries
	1.2 Loading data
	1.3 Checking for monotony of the date (index).
	1.4 Resampling data for 1 hour
	1.5 Output
2. Analysis
	2.1 Time series graph
	2.2 Moving Average
	2.3 Sliding standard deviation
	2.4 Trends and seasonality
	2.5 Output
3. Training
	3.1 Preparation of signs
	3.2 Creating subsamples
	3.3 Model training
		3.3.1 Linear regression
		3.3.2 DecisionTreeRegressor
		3.3.3 RandomForestRegressor
		3.3.4 CatBoost
		3.3.5 LightGBM
	3.4 Results
4. Testing
5. General conclusion
## Results
- According to the results of the test tests, the CatBoostRegressor model with a value of RMSE = 40.78 proved to be the best
- The data also show a noticeable seasonality - peak loads occur at 00 and 4-5 pm, while the minimum number of orders arrives in the early morning (6-7 am) and at 6 pm.
- Maximum number of orders on Mondays and Saturdays
- Minimum quantity on Tuesday and Sunday
- Based on these data, you can create a recommendation for an additional increase in the number of taxi crews during these hours and days.
- The goals and objectives of the study have been achieved
## Used tool stack
- python
- pandas
- seaborn
- numpy
- matplotlib
- sklearn
- statsmodels
- catboost
- lightgbm