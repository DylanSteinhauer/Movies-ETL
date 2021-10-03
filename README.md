# Movies-ETL
## Purpose
The purpose of this challenge is to create an automated pipeline that takes in new data, performs the appropriate transformations, 
and loads the data into existing tables.
In order to do this, I needed to refactor the code from this module to create one function that takes in the three files—Wikipedia data, Kaggle metadata, and the MovieLens rating data—and performs the ETL process by adding the data to a PostgreSQL database.
## Results
The "process_ETL" function runs through the data pipeline from extraction, transformation, and loading. In this example, the function extracts data from three filepaths: wikipedia.movies.json, ratings.csv., and movies_metadata.csv. It then performs the transformation steps, which include cleaning data from both Wikipedia and Kaggle. Once the data is cleaned, the Wikipedia and Kaggle Movies datasets are merged into one dataset with the ratings dataset being kept apart. The transformed datasets are then loaded into a SQL database.\
![movies_query](https://user-images.githubusercontent.com/87148177/135764802-712075c9-74b9-4cdf-ac0d-65f8588b0156.png)\
After completing the ETL process, I had a database with two tables: one for movies and one for ratings. The movies table consists of 31 columns holding a range of information for 6052 different movies.\
![ratings_query](https://user-images.githubusercontent.com/87148177/135764830-91b72db8-d947-4a9e-877c-65b85460e446.png)\
The ratings table consists of 5 different columns containing information on over 26 million individual user ratings.\
