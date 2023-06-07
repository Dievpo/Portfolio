# 05. Introduction to machine learning
# Tariff recommendation
## Project description
The mobile operator "Megaline" found out that many customers use archival tariffs. They want to build a system that can analyze customer behavior and offer users a new tariff: "Smart" or "Ultra".
At the disposal of data on the behavior of customers who have already switched to these tariffs (from the draft course "Statistical Data Analysis"). You need to build a model for the classification problem that will select the appropriate rate.
Build a model with the highest possible accuracy. To pass the project successfully, you need to bring the percentage of correct answers to at least 0.75. Check accuracy on the test set.
## Data Description
Each object in the data set is information about the behavior of one user per month. Known:
Features:
- calls — number of calls,
- minutes — total duration of calls in minutes,
- messages — number of sms messages,
- mb_used - Internet traffic used in Mb,
Target:
- is_ultra - what tariff did you use during the month ("Ultra" - 1, "Smart" - 0).
## Project Structure
1.  Open and examine the file  
2.  Split the data into samples   
3.  Explore Models
    3.1 Decision tree
    3.2 Random forest 
    3.3 Logistic regression
    3.4 Conclusion
4.  Check the model on the test set
5 (bonus) Check models for adequacy 
## Results 
Model with the best accuracy:
- Model type RandomForestClassifier (Random Forest)
- The value of n_estimators = 26
- depth value = 7
- The value of accuracy in the test set = 0.8055987558320373
The model works quite well - it is able to correctly predict about 80% of the answers. We can consider that the goal of the project has been achieved.
## Used tool stack
- python
- pandas
- matplotlib
- sklearn
