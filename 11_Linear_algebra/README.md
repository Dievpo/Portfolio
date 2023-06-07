# 11. Linear algebra
## Project description
- Develop this method of data transformation so that it is difficult to restore personal information on them..
- Protect the data so that when transforming the quality of machine learning models does not deteriorate
## Data Description
Protection of personal data of clients:  

**Features**
- Gender
- Age
- The salary of the insured
- Number of members of his family

**Target feature**  
Exited - The number of insurance payments to the client over the past 5 years
## Project Structure
1.  Data preparation  
    1.1  Import libraries  
    1.2  Loading and Exploring Data  
    1.3  Data preprocessing  
2.  Matrix multiplication
    2.1  Theoretical part
    2.1  Features are multiplied by an invertible matrix. Will the quality of linear regression change?
3.  Transforming algorithm  
4.  Checking the algorithm  
    4.1  Examine the quality of the model without transformation  
        4.1.1  With the original features
        4.1.2  With scaled features
    4.2  Examine the quality of the model with transformation   
        4.2.1  Model quality with the original features
        4.2.2  Model quality with scaled features
5.  Final conclusion  
## Results
The value of the metric f1 (on the test sample) that satisfies the technical task was obtained on the model **random forest**.  
Received scores:  
- Metric R2 for Linear regression 0.435228
- Metric R2 for Linear regression with scale 0.435228
- Metric R2 for Linear regression on transformed features 0.435228
- Metric R2 for Linear regression on transformed features with a scale of 0.435228
## Used tool stack
- python
- pandas
- numpy
- sklearn
