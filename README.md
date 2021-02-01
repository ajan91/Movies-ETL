# Movies-ETL

# Background and Purpose

**Background**
"Amazing Prime loves the dataset and wants to keep it updated on a daily basis. Britta needs your help to create an automated pipeline that takes in new data, performs the appropriate transformations, and loads the data into existing tables. You’ll need to refactor the code from this module to create one function that takes in the three files—Wikipedia data, Kaggle metadata, and the MovieLens rating data—and performs the ETL process by adding the data to a PostgreSQL database."

**Purpose**
This new assignment consists of four technical analysis deliverables. You will submit the following:
1. Deliverable 1: Write an ETL Function to Read Three Data Files
2. Deliverable 2: Extract and Transform the Wikipedia Data
3. Deliverable 3: Extract and Transform the Kaggle data
4. Deliverable 4: Create the Movie Database


# Deliverable 1: Write an ETL Function to Read Three Data Files

**Deliverable 1 has 4 deliverables which are the following:**
1. An ETL function is written to read in the three data files.
2. The function converts the Wikipedia JSON file to a Pandas DataFrame, and the DataFrame is displayed in the ETL_function_test.ipynb file.
3. The function converts the Kaggle metadata file to a Pandas DataFrame, and the DataFrame is displayed in the ETL_function_test.ipynb file.
4. The function converts the MovieLens ratings data file to a Pandas DataFrame, and the DataFrame is displayed in the ETL_function_test.ipynb file.

# Deliverable 2: Extract and Transform the Wikipedia Data

**Deliverable 2 has 4 deliverables which are the following:**
1. The TV shows are filtered out, and the wiki_movies_df DataFrame is created.
2. A try-except block is used to catch errors while extracting the IMDb IDs with a regular expression and dropping duplicate IDs.
3. The extraction and transformation of the Wikipedia data in the ETL function does the following:
  3.1. A list comprehension is used to keep columns with non-null values.
  3.2.  The non-null box office data is converted to string values using the lambda and join functions. 
  3.3.  A regular expression is used to match the six elements of "form_one" of the box office data. 
  3.4.  A regular expression is used to match the three elements of "form_two" of the box office data.
  3.5.  The following columns are cleaned in the Wikipedia DataFrame:
        - The box office column
        - The budget column
        - The release date column
        - The running time column
4. The cleaned Wikipedia data is converted to a Pandas DataFrame, and the DataFrame is displayed in the ETL_clean_wiki_movies.ipynb file.

# Deliverable 3: Extract and Transform the Kaggle Data

**Deliverable 3 has 3 deliverables which are the following:**
1. The extraction and transformation of the Kaggle metadata using the ETL function does the following:
  1.1. The Kaggle metadata is cleaned.
  1.2. The Wikipedia and Kaggle DataFrames are merged.
  1.3. The following is performed on the merged Wikipedia and Kaggle DataFrames to create the movies_df:
      1.3.1. Unnecessary columns are dropped.
      1.3.2. A function is used to fill in the missing Kaggle data.
      1.3.3. The movies_df DataFrame is filtered to keep specific columns.
      1.3.4. The movies_df DataFrame columns are renamed.

2. The extraction and transformation of the MovieLens ratings data using the ETL function does the following:
    2.1. The ratings counts are cleaned.
    2.2. The movies_df DataFrame is merged with the cleaned ratings DataFrame to create the movies_with_ratings_df DataFrame.
    2.3.The empty values in the movies_with_ratings_df DataFrame are filled with “0”.

3. The movies_with_ratings_df and the movies_df DataFrames are displayed in the ETL_clean_kaggle_data.ipynb file.

# Deliverable 4: Create the Movie Database

**Deliverable 4 has 3 deliverables which are the following:**
1. The data from the movies_df DataFrame replaces the current data in the movies table in the SQL database, as determined by the movies_query.png.
2. The data from the MovieLens rating CSV file is added to the ratings table in the SQL database, as determined by the ratings_query.png.
3. The elapsed time to add the data to the database is displayed in the ETL_create_database.ipynb file.
