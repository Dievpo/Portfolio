# 10. Spark MLlib
## Project description
- To train a linear regression model on housing data in California in 1990
- To predict the median cost of a house in a residential array
- To assess the quality of the model, use the rmse, MAE and R2 metrics
## Data Description
Provided historical data on customer behavior:  

**Features**
- longitude 
- latitude 
- housing_median_age — median age of the inhabitants of the residential array
- total_rooms — total number of rooms in houses
- total_bedrooms — total number of bedrooms in houses
- population — number of people who live in a residential array
- households — number of households in the residential array
- median_income — median income of the inhabitants of the residential array
- ocean_proximity — proximity to the ocean

**Target feature**  
- median_house_value — median cost of a house in a residential array
## Project Structure
1.  Data preparation  
    1.1  Import libraries  
    1.2  Loading Data  
    1.3  Dataset analysis  
    1.4  Separation into samples  
    1.5  Transformation of categorical features  
    1.6  Transformation of numerical features  
    1.7  Collect transformed categorical and numerical signs using VectorAssembler 
2.  Model training  
    2.1  Model training
        2.1.1  Using all the data from the file   
        2.1.2  Using only numerical variables, excluding categorical 
    2.2  Prediction on the training sample  
        2.2.1  For all data  
        2.2.2  Only for numeric variables  
3.  Analysis of results  
        3.0.1  For all data  
        3.0.2  Only for numeric variables  
 
## Results
The value of the metric f1 (on the test sample) that satisfies the technical task was obtained on the model **random forest**.  
Received scores:
The model trained on all data (numerical and categorical) shows the best parameters:  
- The RMSE for the model is: 68791.573039
- The MAE for the model is: 50066.800849
- The r2 for the model is: 0.649826
## Used tool stack
- python
- pandas
- numpy
- pyspark
