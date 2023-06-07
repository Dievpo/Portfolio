# 03. Module project 1
## Project description
The customer of this study is the Ministry of Culture of the Russian Federation.
It is necessary to study the Russian film distribution market and identify current trends. Pay attention to films that have received state support. To answer the question of how interesting such films are to the viewer.
## Data Description
The mkrf_movies table contains information from the rental license registry. One film can have several distribution certificates.
- title — the title of the movie;
- puNumber — rental certificate number;
- show_start_date — movie premiere date;
- type — movie type;
- film_studio — production studio;
- production_country — country of origin;
- director;
- producer;
- age_restriction — age category;
- refundable_support — amount of state support refundable funds;
- nonrefundable_support — the amount of non-refundable state support funds;
- financing_source — source of government funding;
- budget — the total budget of the movie;
- ratings — movie rating on KinoPoisk;
- genres — the genre of the movie.
The budget column already includes the full amount of government support. The data in this column is only for those films that received government support.

The mkrf_shows table contains information about movie screenings in Russian cinemas.
- puNumber — rental certificate number;
- box_office - fees in rubles.
## Project Structure
1.  Connecting Libraries  
2.  Open data files and merge them into one dataframe   
3.  Data preprocessing 
    3.1  Check Data Types  
    3.2  Examine the gaps in the dataframe  
    3.3  Examine duplicates in a dataframe
    3.4  Learn Categorical Meanings
    3.5  Check quantitative values
    3.6  Add new columns
4.  Conduct exploratory data analysis
5.  Explore films that have received government support
6.  Write a general conclusion
## Used tool stack
- python
- pandas
