# 17. Machine learning for texts
# Toxic comments detection
## Project description
Wikishop online store launches a new service. 
Now users can edit and supplement product descriptions, as in wiki communities. 
That is, clients offer their edits and comment on the changes of others. 
The store needs a tool that will search for toxic comments and send them for moderation.
Train the model to classify comments into positive and negative. 
At your disposal is a data set with markup on the toxicity of edits.
Build a model with an F1 quality metric value of at least 0.75.
## Data description
The data is in the file /datasets/toxic_comments.csv.
The text column in it contains the comment text, and toxic is the target attribute.
## Project Structure
1. Preparation
	1.1 Import libraries
	1.2 Reading a file and examining data
	1.3 Data analysis
	1.4 Data preprocessing
		1.4.1 Lemmatization
		1.4.2 Regular expressions
		1.4.3 Stop words
		1.4.4 Cleaned data set for model training
2. Training
	2.1 LogisticRegression
	2.2 RandomForestClassifier
	2.3 DecisionTreeClassifier
	2.4 Result
3. Testing
5. Conclusions
## Results
During the project:
1. we studied and prepared the data:
	- we looked at the general information about the data
	- made sure that there were no omissions
	- preprocessed the text (removed extra characters, removed stop words)
2. trained the following models: Logistic Regression, Random Forest Classifier and Decision Tree Classifier. Only the Logistic Regression model coped with the task - to achieve the F1 quality metric of at least 0.75.
Result: as the best model for classifying comments, I can recommend the Logistic Regression model with the hyperparameter class_weight = 'balanced', solver='liblinear' and 'C' = 10, which gives the result F1 = 0.771.
## Used tool stack
- python
- pandas
- numpy
- seaborn
- matplotlib
- sklearn
- nltk
- re