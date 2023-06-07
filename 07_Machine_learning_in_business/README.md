# 07. Machine learning in business
# Choosing a location for a well
## Project description
Mining company GlavRosGosNeft. We need to decide where to drill a new well.
The steps for choosing a location are usually as follows:
- Characteristics for wells are collected in the selected region: oil quality and volume of its reserves;
- Build a model to predict the volume of reserves in new wells;
- Choose the wells with the highest value estimates;
- The region with the maximum total profit of the selected wells is determined.
You have been provided with oil samples in three regions. The characteristics for each well in the region are already known. Build a model to determine the region where mining will bring the most profit. Analyze possible profits and risks using the Bootstrap technique.
## Data Description
Geological exploration data of three regions are in the files:
- /datasets/geo_data_0.csv.
- /datasets/geo_data_1.csv.
- /datasets/geo_data_2.csv.
Features:
- id - the unique identifier of the well;
- f0, f1, f2 - three signs of points (it doesn't matter what they mean, but the signs themselves are significant);
Target:
- product - the volume of reserves in the well (thousand barrels).

Conditions of the problem:
- Only linear regression is suitable for training the model (the rest are not predictable enough).
- During the exploration of the region, 500 points are explored, from which, using machine learning, the best 200 are selected for development.
- The budget for the development of wells in the region is 10 billion rubles.
- At current prices, one barrel of raw materials brings 450 rubles of income. The income from each unit of the product is 450 thousand rubles, since the volume is indicated in thousands of barrels.
- After assessing the risks, you need to leave only those regions in which the probability of losses is less than 2.5%. Among them, choose the region with the highest average profit.
Synthetic data: details of contracts and characteristics of deposits were not disclosed.
## Project Structure
1.  Loading and preparing data  
    1.1  Import libraries  
    1.2  Loading Data   
2.  Train and validate the model  
3.  Preparation for profit calculation
4.  Calculation of profit and risks  
    4.1  Profit calculation  
    4.2  Calculation of profit and risks  
## Results
1. When calculating indicators for the best 200 wells out of 500 in the sample:
- The average stock of raw materials from one well among all regions (118.66, 119.77, 116.00, respectively) exceeds the minimum required volume of 111.11.
2. As a result of applying the Boostrap technique, it was revealed that the only suitable region (the probability of losses is less than 2.5%) is region 1:
- The probability of losses was 0.7%;
- Average revenue - 451.79 million rubles;
- The 95% confidence interval (67.48 - 849.38 million rubles) is the narrowest among all regions and does not contain negative values (unlike other regions).
## Used tool stack
- python
- pandas
- numpy
- matplotlib
- seaborn
- sklearn
