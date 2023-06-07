# 15. Module project 3
# Assessment of the risk of an accident along the selected route
## Project description
It is necessary to create a system that could assess the risk of an accident along the chosen route. 
Risk refers to the probability of an accident with any damage to the vehicle. 
As soon as the driver has booked a car, got behind the wheel and chosen a route, the system should assess the level of risk. 
If the risk level is high, the driver will see a warning and recommendations along the route.
## The idea of solving the problem from the customer:
1. Create an accident prediction model (the target value is at_fault (the culprit) in the parties table)
- For the model, choose the type of culprit — only car (car).
- Select cases when an accident led to any damage to the vehicle, except for the SCRATCH type.
- For modeling, we limit ourselves to data for 2012 — they are the most recent.
- A prerequisite is to take into account the age factor of the car.
2. On the basis of the model to investigate the main factors of an accident.
3. To understand whether the results of modeling and analysis of the importance of factors will help answer the questions:
- Is it possible to create an adequate driver risk assessment system when issuing a car?
- What other factors need to be taken into account?
- Do I need to equip the car with any sensors or a camera?
### Brief description of the tables
- collisions — general information about the accident
	Has a unique case_id. This table describes the general information about the accident. For example, where it happened and when.
- parties — information about road accident participants
	Has a non-unique case_id, which is mapped to the corresponding accident in the collisions table. Each line here describes one of the parties involved in the accident. If two cars collided, there should be two rows in this table with a case_id match. If you need a unique identifier, this is case_id and party_number.
- vehicles — information about affected vehicles
	Has non-unique case_id and non-unique party_number, which are mapped to the collisions table and the parties table. If you need a unique identifier, this is case_id and party_number.
## Project Structure
1. Connect to the database. Load the sql tables
2. Conduct an initial study of the tables
	2.1 Conclusion
3. Conduct a statistical analysis of the accident factors
	3.1 Let's find out in which months the greatest number of accidents occurs (collisions table)
	3.2 We will analyze the severity of damage to the vehicle, based on the condition of the road at the time of the accident
	3.3 Find the most common causes of accidents (parties table)
		3.3.1 We will find the most frequent violations:
		3.3.2 Does the weather affect the probability of an accident:
		3.3.3 Does lighting affect the likelihood of an accident:
	3.4 Cars with what type of body are more likely to be seriously damaged in an accident
	3.5 Conclusions:
4. Create a model for driver risk assessment
	4.1 We will prepare a data set based on the primary assumption of the customer:
	4.2 EDA
	4.3 We will carry out the primary selection of the factors necessary for the model
		4.3.1 Let's look at the distribution of the target column
		4.3.2 vehicle_type
		4.3.3 vehicle_age
		4.3.4 party_type
		4.3.5 insurance_premium
		4.3.6 party_sobriety
		4.3.7 party_drug_physical
		4.3.8 cellphone_in_use
		4.3.9 weather_1
		4.3.10 location_type
		4.3.11 collision_damage
		4.3.12 primary_collision_factor
		4.3.13 type_of_collision
		4.3.14 motor_vehicle_involved_with
		4.3.15 road_surface
		4.3.16 road_condition_1
		4.3.17 lighting
		4.3.18 collision_date
		4.3.19 collision_time
		4.3.20 We encode categorical features
		4.3.21 We will prepare training and test samples
		4.3.22 Let's do the scaling
	4.4 Conclusion:
5. Model Selection
	5.1 Let's choose a metric for evaluating the model based on the task set by the business:
	5.2 Decision Tree Classifier
	5.3 Random Forest Classifier
		5.4 CatBoost
	5.5 Model Selection
	5.6 Confusion Matrix - Error Matrix
		5.6.1 Decision Tree:
		5.6.2 Random Forest:
		5.6.3 CatBoost:
	5.7 Let's analyze the importance of the main factors affecting the probability of an accident
	5.8 Conclusions
6. Conclusions
## Results
The best model is the Cart boost model.
- F1 on the test sample = 0.63789
- Total predictions: 17165
- Correctly classified: 71.0%
- Correctly classified wine - Recall: 68.0%
- Predicted fault corresponding to reality - Precision: 85.0%
- This model pays most attention to the availability of insurance and sobriety of the participant

Since the most important factor of an accident is the level of sobriety of the culprit (party_sobriety), then you can:
- equip the car with an alcohol intoxication analyzer
- measurement of the condition during landing should be made a prerequisite for admission to the steering wheel, without this the car will not start
- to make sure that it is the driver who breathes into the tube, add a camera aimed at the driver's seat

And the presence of insurance must be prescribed when registering in the application.
## Used tool stack
- python
- pandas
- seaborn
- numpy
- matplotlib
- sklearn
- sqlalchemy
- catboost
