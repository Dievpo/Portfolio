# 06. Supervised Learning
## Project description
- Analyze historical data on the behavior of bank customers, termination of contracts. Predict the exit of the client from the bank.
- Build classification model, quality metric f1 (minimum value 0.59)
- Measure AUC-ROC, compare its value with f1-measure.
## Data Description
Provided historical data on customer behavior:  

**Features**
- RowNumber - row index in data
- CustomerId - unique customer identifier
- Surname
- CreditScore
- Geography - country of residence
- Gender
- Age
- Tenure - how many years a person has been a bank client
- Balance - account balance
- NumOfProducts - the number of bank products used by the client
- HasCrCard - the presence of a credit card
- IsActiveMember - client activity
- EstimatedSalary

**Target feature**  
Exited - the fact that the client
## Project Structure
1.  Data preparation  
    1.1  Import libraries  
    1.2  Loading and Exploring Data  
    1.3  Data preprocessing  
    1.4  Feature transformation  
    1.5  Divide the data into samples  
    1.6  Scaling numerical features  
2.  Problem research  
    2.1  Check class balance  
    2.2  Train the model without taking into account the imbalance  
        2.2.1  Decision tree  
        2.2.2  Random forest  
        2.2.3  Logistic regression  
    2.3  Build an ROC-curve and calculate the areas under this line  
3.  Struggling with imbalance  
    3.1  Class weighting  
    3.2  Upsampling  
    3.3  Downsampling  
4.  Model testing  
## Results
The value of the metric f1 (on the test sample) that satisfies the technical task was obtained on the model **random forest**.  
Received scores:  
- Accuracy = 0.8355
- f1_score = 0.624
- ROC-AUC = 0.8614539038267852
## Used tool stack
- python
- pandas
- matplotlib
- seaborn
- sklearn
