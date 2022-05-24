# Movies-ETL

## Background

Amazing Prime loves the dataset and wants to keep it updated on a daily basis. Britta needs your help to create an automated pipeline that takes in new data, performs the appropriate transformations, and loads the data into existing tables. You’ll need to refactor the code from this module to create one function that takes in the three files—Wikipedia data, Kaggle metadata, and the MovieLens rating data—and performs the ETL process by adding the data to a PostgreSQL database.

### Overview of Project

 Wikipedia has a ton of information about movies, including budgets and box office returns, cast and crew, production and distribution, and so much more. Luckily, one of Britta's coworkers created a script to go through a list of movies on Wikipedia from 1990 to 2018 and extract the data from the sidebar into a JSON. Unfortunately, her coworker can't find the script anymore and just has the JSON file. We'll need to load in the JSON file into a Pandas DataFrame.
 
 ### Project Deliverables
 
 1. Deliverable 1: Write an ETL Function to Read Three Data Files
 2. Deliverable 2: Extract and Transform the Wikipedia Data
 3. Deliverable 3: Extract and Transform the Kaggle Data
 4. Deliverable 4: Create the Movie Database
 5. Deliverable 5: A written report on the Movie Database analysis README.md.

Deliverable 1: Write an ETL Function to Read Three Data Files
 
 -- Using the ETL_function_test file by step:

Created a function to read in three seperate files
Read in the Kaggle metadata and MovieLens ratings CSV files as Pandas DataFrames.
Opened the Wikipedia JSON file and use the json.load() function to convert the JSON data to raw data.
read in the raw Wikipedia movie data as a Pandas DataFrame.
use the code provided to return the three DataFrames.
use the variables provided to create a path to the Wikipedia data, the Kaggle metadata, and the MovieLens rating data files.
set the three variables in Step 6 equal to the function created in Step 1.
set the DataFrames from the return statement equal to the file names in Step 6. In this step, you are reassigning the variables created in Step 6 to the variables in the return statement.
Now to view that all our dataframes are correct use the .head() method to make sure your dataframes look correct(example below):


![image](https://user-images.githubusercontent.com/93686963/169939325-70dd63bd-50f1-4ee5-a437-d5dd42fa6afb.png)

Deliverable 2:
- Extract and Transform the Wikipedia Data with the ETL_clean_wiki_movies.ipynb:

Create the code for the clean movie function that takes in the argument "movie".
Add the function you created in step 1 that reads in the three data files.
Inside the function you created in step 1's python file, remove the code that creates the wiki_movies_df DataFrame from the wiki_movies_raw file, then write a list comprehension that filters out TV shows from the wiki_movies_raw file.
Write a list comprehension to iterate through the cleaned wiki movies list that you created in Step 3.
Read in the cleaned movies list from Step 4 as a DataFrame.
Write a try-except block that will catch errors while extracting the IMDb IDs with a regular expression string and dropping any imdb_id duplicates. If there is an error, capture and print the exception.
Write a list comprehension to keep the columns that have non-null values from the DataFrame created in Step 5, then create a wiki_movies_df DataFrame from the list.
Create a variable that will hold all the non-null values from the "Box office" column.
Convert the box office data created in Step 8 to string values using the lambda and join functions.
Write a regular expression to match the six elements of form_one of the box office data.
Write a regular expression to match the three elements of form_two of the box office data.
Add the parse_dollars() function.
Add the code that cleans the box office column in the wiki_movies_df DataFrame using the form_one and form_two lists created in Steps 10 and 11, respectively.
Add code that cleans the budget column in the wiki_movies_df DataFrame.
Add code that cleans the release date column in the wiki_movies_df DataFrame.
Add code that cleans the running time column in the wiki_movies_df DataFrame.
Use the variables provided to create a path to the Wikipedia data, the Kaggle metadata, and the MovieLens rating data files.
Set the three variables in Step 17 equal to the function created in Deliverable 1.
Set the wiki_movies_df equal to the wiki_file variable.
Add the columns from wiki_movies_df DataFrame to a list, and confirm that they are the same as this image:


