# 12. Numerical_methods
# Determining the cost of cars
## Project description
Used car sales service "Not beaten, not painted" is developing an application to attract new customers. It will show you the market value of your car.
Build a model that knows how to determine it. At your disposal are data on the technical characteristics, equipment and prices of other vehicles.
Criteria that are important to the customer:
- prediction quality;
- model training time;
- model prediction time.
## Notes:
- To assess the quality of models, use the RMSE metric.
- The RMSE metric value must be less than 2500.
- Learn the LightGBM library on your own and use it to build gradient boosting models.
- The execution time of a Jupyter Notebook code cell can be obtained with a special command. Find her.
- The gradient boosting model can take a long time to train, so change only two or three parameters for it.
## Data Description
Features:
- DateCrawled - date of downloading the questionnaire from the database
- VehicleType - type of car body
- RegistrationYear — year of vehicle registration
- Gearbox - type of gearbox
- Power - power (hp)
- Model - car model
- Kilometer - mileage (km)
- RegistrationMonth - month of car registration
- FuelType — type of fuel
- Brand - car brand
- Repaired - was the car under repair or not
- DateCreated - date of creation of the questionnaire
- NumberOfPictures - the number of photos of the car
- PostalCode - postal code of the owner of the profile (user)
- LastSeen - date of last user activity
Target:
- Price - price (euro)
## Project Structure
1.  Data preparation
    1.1  Data exploration  
    1.2  Data preprocessing  
2.  Model training  
    2.1  LinearRegression  
    2.2  Decision Tree  
    2.3  CatBoost  
    2.4  LightGBM  
3.  Model Analysis    
4.  General conclusion
## Results
The project was completed:
- Data analysis was carried out, during which missing values were processed
- Some anomalies in the data were identified and removed
- Linear regression, random tree, and gradient boosting libraries CatBoost and LightGBM were compared
- Using cross-validation, the best parameters for CatBoostRegressor and LGBMRegressor were selected
- Regression using gradient boosting libraries can improve the prediction result compared to simpler algorithms, but they take longer to train
- CatBoost was more accurate:
   - Prediction time on test set: 0.2575809955596924
   - RMSE of CatBoostRegressor: 1639.5533386745817
## Used tool stack
- python
- pandas
- time
- matplotlib
- sklearn
- lightgbm
- catboost
