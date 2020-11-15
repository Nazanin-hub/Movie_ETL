# Movies-ETL

## Project Overview

The Amazing Prime Video team would like to develop an algorithm to predict which low budget movies being released will become popular. I was tasked to help one member of the Amazing Prime Video team creating the datasets for the hackathon. First, I extracted the data from Wikipedia data, Kaggle metadata, and the MovieLens rating data. Then, transform it into one clean data and Finally, load that dataset into a SQL table. For this analysis, I used the following breakdown:

 - Write an ETL Function to Read Three Data Files
 - Extract and Transform the Wikipedia Data
 - Extract and Transform the Kaggle data
 - Load data to a SQL database 

## Resources

Data Source: wikipedia-movies.json, movies_metadata.csv, ratings.csv
Software: Python 3.8.3, Anaconda Navigator 1.9.6, Jupyter Notebook 6.0.3, PostgreSQL 11.9, pgAdmin 4

## Results

### Write an ETL Function to Read Three Data Files

Using Python and Pandas to write a function that reads Wikipedia JSON, the Kaggle metadata and MovieLens csv files and created three separate DataFrames.

### Extract and Transform the Wikipedia Data

First, I extracted data from Wikipedia data. Then, I transformed and cleaned the Wikipedia data in the ETL function based on the following:

  - cleaned and filtered data with list comprehensions
  - created the clean movie function
  - removed duplicates with regular expressions 
  - removed columns with null values
  - droped null values and converted data to string values
  - Cleaned the box office, budget data, the release date, and the running time
  - converted the cleaned Wikipedia data to a Pandas DataFrame

### Extract and Transform the Kaggle data

First, I extracted and transformed the Kaggle metadata using the ETL function based on the following:

 - Cleaned the Kaggle metadata and converted the transformed data into the Kaggle DataFrame
 - Merged Wikipedia and Kaggle DataFrames with dropping unnecessary columns and using a function to fill in the missing Kaggle data to create the movies_df.

Then, I extracted and transformed the MovieLens ratings data using the ETL function based the following:

 - cleaned the ratings counts and converted the transformed data into the cleaned ratings DataFrame
 - Merged movies_df DataFrame with the cleaned ratings DataFrame to create the movies_with_ratings_df DataFrame
 - Filled the empty values in the movies_with_ratings_df DataFrame with “0”

### Create the Movie Database

Using Python, Pandas, the ETL process, code refactoring, and PostgreSQL to add the movies_df DataFrame and MovieLens rating CSV data to a SQL database. The below SQL queries show the number of rows for the movies and ratings tables.

![] (
