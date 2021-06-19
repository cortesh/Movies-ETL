# Movies-ETL

# Background
Create an automated pipeline that takes in new data, performs the appropriate transformations, and loads the data into existing tables. Refactor the code from this module to create one function that takes in the three files—Wikipedia data, Kaggle metadata, and the MovieLens rating data—and performs the ETL process by adding the data to a PostgreSQL database.

## What You're Creating
This new assignment consists of four technical analysis deliverables. You will submit the following:

Deliverable 1: Write an ETL Function to Read Three Data Files
Deliverable 2: Extract and Transform the Wikipedia Data
Deliverable 3: Extract and Transform the Kaggle data
Deliverable 4: Create the Movie Database

## Deliverable 1 Requirements
You will earn a perfect score for Deliverable 1 by completing all requirements below:

An ETL function is written to read in the three data files. (10 pt)
The function converts the Wikipedia JSON file to a Pandas DataFrame, and the DataFrame is displayed in the ETL_function_test.ipynb file. (5 pt)
​The function converts the Kaggle metadata file to a Pandas DataFrame, and the DataFrame is displayed in the ETL_function_test.ipynb file. (5 pt)
​The function converts the MovieLens ratings data file to a Pandas DataFrame, and the DataFrame is displayed in the ETL_function_test.ipynb file. (5 pt)

## Deliverable 2: Extract and Transform the Wikipedia Data (30 points)
Deliverable 2 Instructions
Extract and transform the Wikipedia data to merge it with the Kaggle metadata. While extracting the IMDb IDs using a regular expression string and dropping duplicates, use a try-except block to catch errors.

## Deliverable 2 Requirements
Complete all requirements below:

1. The TV shows are filtered out, and the wiki_movies_df DataFrame is created. (3 pt)
2. A try-except block is used to catch errors while extracting the IMDb IDs with a regular expression and dropping duplicate IDs. (5 pt)
3. The extraction and transformation of the Wikipedia data in the ETL function does the following:
4. A list comprehension is used to keep columns with non-null values. (3 pt)
5. The non-null box office data is converted to string values using the lambda and join functions. (3 pt)
6. A regular expression is used to match the six elements of "form_one" of the box office data. (2 pt)
7. A regular expression is used to match the three elements of "form_two" of the box office data. (2 pt)
8. The following columns are cleaned in the Wikipedia DataFrame: (8 pt)
  * The box office column
  * The budget column
  * The release date column
  * The running time column
9. The cleaned Wikipedia data is converted to a Pandas DataFrame, and the DataFrame is displayed in the ETL_clean_wiki_movies.ipynb file. (4 pt)

## Deliverable 3: Extract and Transform the Kaggle Data (30 points)
Extract and transform the Kaggle metadata and MovieLens rating data, then convert the transformed data into separate DataFrames. Merge the Kaggle metadata DataFrame with the Wikipedia movies DataFrame to create the movies_df DataFrame. Finally, Merge the MovieLens rating data DataFrame with the movies_df DataFrame to create the movies_with_ratings_df.

## Deliverable 3 Requirements
complete all requirements below:

1. The Kaggle metadata is cleaned. (4 pt)
2. The Wikipedia and Kaggle DataFrames are merged. (3 pt)
3. The following is performed on the merged Wikipedia and Kaggle DataFrames to create the movies_df: (8 pt)
4. Unnecessary columns are dropped.
5. A function is used to fill in the missing Kaggle data.
6. The movies_df DataFrame is filtered to keep specific columns.
7. The movies_df DataFrame columns are renamed.
8. The extraction and transformation of the MovieLens ratings data using the ETL function does the following:
9. The ratings counts are cleaned. (3 pt)
10. The movies_df DataFrame is merged with the cleaned ratings DataFrame to create the movies_with_ratings_df DataFrame. (4 pt)
11. The empty values in the movies_with_ratings_df DataFrame are filled with “0”. (3 pt)
12. The movies_with_ratings_df and the movies_df DataFrames are displayed in the ETL_clean_kaggle_data.ipynb file. (5 pt)


## Deliverable 4: Create the Movie Database (15 points)
Add the movies_df DataFrame and MovieLens rating CSV data to a SQL database.

## Deliverable 4 Requirements
complete all requirements below:

1. The data from the movies_df DataFrame replaces the current data in the movies table in the SQL database, as determined by the movies_query.png. (5 pt)
2. The data from the MovieLens rating CSV file is added to the ratings table in the SQL database, as determined by the ratings_query.png. (5 pt)
3. The elapsed time to add the data to the database is displayed in the ETL_create_database.ipynb file. (5 pt)
