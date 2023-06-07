# 00. Basic Python
## Project description
Using real data from Yandex Music, test hypotheses and compare the behavior of users in Moscow and St. Petersburg
## Hypotheses
- User activity depends on the day of the week. Moreover, in Moscow and St. Petersburg this manifests itself in different ways.
- On Monday morning, certain genres of music prevail in Moscow, while others prevail in St. Petersburg. This is true for Friday evening as well.
- Moscow and St. Petersburg prefer different genres of music. In Moscow, they listen to pop music more often, in St. Petersburg - Russian rap.
## Data Description
- userID;
- Track — track name;
- artist — the name of the artist;
- genre — the name of the genre;
- City — user's city;
- time — listening start time;
- Day — the day of the week.
## Project Structure
1.  Data overview  
2.  Data preprocessing  
    2.1  Heading style  
    2.2  Missing values  
    2.3  Duplicates  
3.  Hypothesis testing  
    3.1  Comparison of user behavior of two capitals  
    3.2  Music at the beginning and end of the week  
    3.3  Genre preferences in Moscow and St. Petersburg  
4.  Research results  
## Results 
- The day of the week affects the activity of users in Moscow and St. Petersburg in different ways. The first hypothesis was fully confirmed.
- Musical preferences do not change much during the week - be it Moscow or St. Petersburg. Thus, the second hypothesis was only partly confirmed. This result could have been different were it not for gaps in the data.
- The tastes of users in Moscow and St. Petersburg have more in common than differences. Contrary to expectations, genre preferences in St. Petersburg resemble those in Moscow. The third hypothesis was not confirmed. If there are differences in preferences, they are invisible to the bulk of users.
## Used tool stack
- python
- pandas