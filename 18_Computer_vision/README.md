# 18. Computer vision
# Determining the approximate age of a person from a photograph
## Project description
Khleb-Sol supermarket introduces a computer vision system for processing customers' photos. 
Photo fixation in the checkout area will help determine the age of customers in order to:   
- Analyze purchases and offer products that may be of interest to buyers of this age group;  
- Control the conscientiousness of cashiers when selling alcohol.  
Build a model that will determine the approximate age of a person from a photograph. 
At your disposal is a set of photographs of people with age indication.
## Data description
- the sample consists of 7591 color photographs of various sizes;  
- the majority of people in the images are aged 20-30 years old, with peaks of 25 and 30 years old;  
## Project Structure
1. Exploratory data analysis   
	1.1 Sample size  
	1.2 Age distributions in the sample  
	1.3 Visual evaluation of photos  
	1.4 Conclusions  
2. Model Training  
	2.1 Loading the training set  
	2.2 Loading a test subsample  
	2.3 Model creation  
	2.4 Model run  
	2.5 Learning process  
	2.6 Conclusions  
3. Analysis of the trained model  
4. General conclusion  
## Results
The purpose of the study is fulfilled: the trained model demonstrates MAE = 6.99 without parameter tuning and data augmentation.
The model is better suited for solving a business problem - Analyze purchases and offer products that may be of interest to buyers of this age group, because the error of 6.99 years does not allow you to control the conscientiousness of cashiers when selling alcohol.
## Used tool stack
- python  
- pandas  
- numpy  
- seaborn  
- keras  
