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
