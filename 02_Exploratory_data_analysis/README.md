# 02. Exploratory data analysis
## Project description
Yandex Real Estate service data is an archive of ads for several years about the sale of apartments in St. Petersburg and neighboring settlements.
The task is to perform data preprocessing and study them in order to find interesting features and dependencies that exist in the real estate market.
## Data Description
- airports_nearest — distance to the nearest airport in meters (m)
- balcony — number of balconies
- ceiling_height
- cityCenters_nearest — distance to the city center (m)
- days_exposition — how many days the ad was placed (from publication to removal)
- first_day_exposition — publication date
- floor
- floors_total — total floors in the house
- is_apartment — apartments (boolean)
- kitchen_area — kitchen area in square meters (m²)
- last_price — price at the time of unpublishing
- living_area — living area in square meters (m²)
- locality_name — name of the locality
- open_plan — open plan (boolean)
- parks_around3000 — number of parks within a 3 km radius
- parks_nearest — distance to the nearest park (m)
- ponds_around3000 — the number of ponds within a radius of 3 km
- ponds_nearest — distance to the nearest body of water (m)
- rooms — number of rooms
- studio — studio apartment (boolean)
- total_area — total area of the apartment in square meters (m²)
- total_images — the number of photos of the apartment in the ad
## Project Structure
1.  Connecting Libraries  
2.  Open the data file and study the general information   
3.  Data preprocessing 
4.  Count and add new columns to the table 
    4.1  Price per square meter  
    4.2  Add columns: day of the week, month and year of publication  
    4.3  Added to the table: apartment floor type (values - "first", "last", "other")
    4.4  Added to the table: distance in km to the city center
5.  Conduct exploratory data analysis
    5.1  Let's study the following parameters of objects:
         5.1.1  Total area
         5.1.2  Living space
         5.1.3  Kitchen area
         5.1.4  Object price
         5.1.5  Number of rooms
         5.1.6  Ceiling height
         5.1.7  Apartment floor
         5.1.8  Apartment floor type (“first”, “last”, “other”)
         5.1.9  The total number of floors in the house
         5.1.10 Distance to city center in meters  
         5.1.11 Distance to nearest airport
         5.1.12 Distance to nearest park  
         5.1.13 Day and month of ad publication
    5.2  Apartment sale time
    5.3  Factors affecting the total (full) cost of the object:
         5.3.1  Total area
         5.3.2  Living area
         5.3.3  Kitchen area
         5.3.4  Number of rooms
         5.3.5  Apartment floor type (“first”, “last”, “other”)
         5.3.6  Placement dates (weekday, month, year)
    5.4  The average price of one square meter in 10 settlements with the largest number of ads
    5.5  Average price per kilometer from the center of St. Petersburg
6.  Overall Conclusion
## Results 
The study of scatter diagrams showed a direct relationship between:
- the cost of the object and the total area is, and the higher the total area, the higher the cost of the object
- the total cost of the object and the number of rooms
- price per square meter and distance from the center. The greater the distance from the center, the lower the price.
## Used tool stack
- python
- pandas
