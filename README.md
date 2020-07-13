# Movies_ETL
Using ETL for a Hackathon about Movies

## List of Assumptions (also commented within code)
- We will not lose too much data by getting rid of movies with no imdblink
- We will not lose too much data by dropping 90% null columns
- The Box office column does not contain solely string objects
- Box office & Budget numbers are not in standardized string format and we can cover most of the data using using 5 forms and convert them to numeric based on the form.
- There is bad data in 'adult'
- There is no bad data in 'video'
- Need to coerce kaggle data types
- Kaggle data is better, but can fill 0 rows with wiki_data


## Challenge Analysis
In this assignment, our task was to take we based data from two different source, clean and merge with in a comprehensible way to provide convenient data for a hackathon. Using Json, and pandas we read the data into data frames to make the cleaning of the data easier. While cleaning the data, we diagnosed the cleaning steps that needed to be applied multiple times and would be done more efficiently with a function, versus steps that might be done only once and could vary based on updated data. We found that the wiki data was quite messy and need heavy cleaning. We isolated the movies (the data we wanted), and cleaned the columns and reduced the columns to only relevant data we desired. We then had to use regular expressions, a very poweful tool, to take box office, budget, run time, and release date data, and convert them to their appropriate data types. Through inital exploratory data analysis we found expressiont types that would caputure most of the data we required. After cleaning this, we looked at the Kaggly data which was much easier to coerce to their data types. We considered the fact that in the future this might not be the case and used try-except statement to throw debugging error statements in this case. Finally we merged the two data sets, and through exploratory analysis we found that the kaggle data was much better than the wiki date, but the wiki data was a bit more expansive and could be used to fill holes in the kaggle data for some columns. This will likely be the case going forward because Kaggle is a movie database and wikipedia is an information database based on user contributions. We then transformed the ratings dating by grouping is conveniently and pivoting it to prepapre fo a merge with our merged database. We then used the SQLAlchemy module to upload the data to SQL. Looking back, we really only used the wikipedia data to fill in gaps in the kaggle data. So a good analysis would be to see how many gaps there are in the Kaggle data and if it's really worth doing all the wiki data cleaning for those gaps.
