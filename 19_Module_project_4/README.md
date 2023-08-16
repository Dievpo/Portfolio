# 19. Module project 4
# Image search
## Project description
You work in a photo hosting for professional photographers “With Sense” (“With Sense”).  
Your users post their photos on the hosting and accompany them with a full description: they indicate the location of the shooting, the camera model, etc. 
A distinctive feature of the service is the description: it can be provided not only by the one who posts the photo, but also by other users of the portal.   
Your department is experimenting with developing a search for reference photos for photographers. 
The essence of the search is as follows: the user of the service enters a description of the desired scene.  
You have been tasked with developing an on-demand image search demo.  
For the demo version, you need to choose the best model that will receive the vector representation of the image, the vector representation of the text, and at the output it will give a number from 0 to 1 - and show how the text and image fit together.
## Legal restrictions
Image processing restrictions apply in some countries where With Sense operates: search and search services are prohibited from providing any information, including, but not limited to, text, images, videos, and audio containing a description, image, or recording of children's voices.
A child is any person under the age of 16.
Your service strictly follows the laws of the countries in which they operate.  
Therefore, when trying to view images prohibited by law, a disclaimer is shown instead of images:   
⎢ This image is unavailable in your country in compliance with local laws.  
During testing of the model, a disclaimer should be displayed when "harmful" content appears in the request.
## Data description
- The train_dataset.csv file contains the information needed for training: image file name, description ID, and description text. 
Up to 5 descriptions can be available for one picture. The description ID has the format <image file name>#<description serial number>.
- The train_images folder contains images for training the model.
- In the CrowdAnnotations.tsv file, data on matching images and descriptions obtained using crowdsourcing.
- The ExpertAnnotations.tsv file contains data on the correspondence between the image and description, obtained as a result of a survey of experts.
- The test_queries.csv file contains the information needed for testing: the query ID, the query text, and the relevant image. 
Up to 5 descriptions can be available for one picture. 
The description ID has the format <image file name>#<description serial number>.
- The test_images folder contains images for testing the model.
## Project Structure
1. Description of data  
2. Import libraries and data  
3. Exploratory data analysis  
4. Data verification  
5. Image vectorization  
6. Text vectorization  
7. Combining vectors  
8. Training the fit prediction model  
    8.1. Linear models  
    8.2. Neural network  
9. Model testing  
10. Conclusions  
## Results
The target was generated based on the aggregated assessments of experts and crowdsourcing. 
Target - an assessment of the similarity between the description and the image, which lies in the range from zero to one.  
It was decided to solve the regression problem. The quality metric is RMSE.  
The performance of linear regression was not very good. 
Therefore, the operation of the neural network was tested. 
The quality it showed after 10 epochs of training is satisfactory - approximately 0.04 rmse. 
When tested on test data, the model showed low quality. 
As a result, she gave out images in which the context is difficult to say that is similar to the description.  
Unfortunately, the models themselves do not work very well. 
And there are several reasons for this - little data, not a very correct approach. 
In my opinion, it would be more promising to bring the embeddings of images and texts to the same dimension in one space (through trained layers) and use the cosine distance as a proximity measure.
## Used tool stack
- python
- pandas
- seaborn
- numpy
- matplotlib
- sklearn
- transformers
- torch
