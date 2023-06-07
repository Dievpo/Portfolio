# 14. Models and algorithms in machine learning
# Predicting the temperature of a star
## Project description
The task from the Sky in the Palm of your Hand observatory is to figure out how to use a neural network to determine the temperature on the surface of detected stars.
Usually , scientists use the following methods to calculate the temperature:
- The law of displacement of Wine.
- Stefan-Boltzmann law.
- Spectral analysis.
Each of them has pros and cons.
The observatory wants to introduce machine learning technologies to predict the temperature of stars, hoping that this method will be the most accurate and convenient.
The observatory's database contains the characteristics of 240 stars that have already been studied.
## Task
It is necessary to develop a neural network that will help predict the absolute temperature on the surface of the star.
Features:
- Relative luminosity L/Lo - the luminosity of a star relative to the Sun.
- Relative radius R/Ro - the radius of the star relative to the radius of the Sun.
- Absolute magnitude Mv - a physical quantity that characterizes the brightness of a star.
- Star color (white, red, blue, yellow, yellow-orange, etc.) - the color of the star, which is determined based on spectral analysis.
- The type of star.
Target:
- Absolute temperature T(K) - the temperature on the surface of the star in Kelvins.
## Project Structure
1. Importing libraries
2. Loading data
3. Data preprocessing and analysis
	3.1 Data analysis
		3.1.1 Let's put the column names in order
		3.1.2 Let's study the general information about the data
		3.1.3 Let's check for duplicates
		3.1.4 Let's check for the presence of passes
		3.1.5 Let's study the temperature column
		3.1.6 Let's study the luminosity column
		3.1.7 Let's study the radius column
		3.1.8 Let's study the magnitude column
		3.1.9. Let's study the type column
		3.1.10 Let's study the color column
		3.1.11 Conclusion:
	3.2 Let's split the data into samples
	3.3 Preparing data for training
		3.3.1 Let 's apply the OHE technique to categorical features
		3.3.2 Scaling quantitative data
4. Building a basic neural network
	4.1 Basic Model 1
	4.2 Basic Model 2
	4.3 Basic Model 3
	4.4 Base Model 4
	4.5 Base Model 5
	4.6 Conclusion based on the results of the model construction: 
5. Neural Network Improvement
	5.1 Batch Normalization
	5.2 Dropout
		5.2.1 The value of p=0.1
		5.2.2 The value of p=0.3
		5.2.3 The value of p=0.5
		5.2.4 Conclusion based on the results of model improvement:
6. Got a model:
7.Conclusions  
## Results
The neural network with 5 hidden layers, trained in 1000 epochs, 5 hidden layers, activation function - ReLU(), with the number of neurons: h1: 350 | h2: 150 | h3: 1350 | h4: 1200 | h5: 1250, proved to be the best. 
It was possible to reach 1299.98 on the test sample according to the RMSE metric. 
It was not possible to get a significant improvement in the RMSE metric. 
Given that the standard deviation of the target is 9552, the result of the model is good. 
It can be seen that the model still poorly identifies stars with high surface temperatures, which may be explained by the small number of such stars in the sample.
## Used tool stack
- python
- pandas
- numpy
- matplotlib
- seaborn
- sklearn
- torch
