# Movies-ETL
## Overview
  * Amazing Prime would like to keep their dataset updated on a daily basis. The project consists of creating an automated pipeline that takes in new data, performs the appropriate transformations, and loads the data into existing tables. 
  * For the project, I refactored the code from existing class module (Module 8: ETL) to create one function that takes in the three files associated — Wikipedia data, Kaggle metadata, and the MovieLens rating data — and performed the ETL process by adding the data to a PostgreSQL database.

## Deliverable 1:
  * For this deliverable, it was necessary to write an ETL Function to Read Three Data Files.
    * I created a function that takes in the three arguments: 
      * Wikipedia data, Kaggle metadata, and MovieLens rating data (from Kaggle)   
    * Resulting wikipedia dataframe:
      * ![Screen Shot 2021-08-23 at 1 44 25 AM](https://user-images.githubusercontent.com/60943801/130402672-7c380d51-7054-4a33-b451-9e5d7bd81683.png)
    * Resulting kaggle dataframe:
      * ![Screen Shot 2021-08-23 at 1 47 04 AM](https://user-images.githubusercontent.com/60943801/130402802-d9215741-8b02-463d-b20a-8019d1abec4e.png)
    * Resulting ratings datagrame:
      * ![Screen Shot 2021-08-23 at 1 47 59 AM](https://user-images.githubusercontent.com/60943801/130402880-d5f80079-b78a-43e1-9367-7287b7641cb6.png)
    
## Deliverable 2: 
  * For this deliverable, I extracted and transformed the Wikipedia Data
    * Methods utilized:
      * try-except blocks, to catch errors while extracting the IMDb IDs with a regular expression and dropping duplicate IDs.
      * lambda functions, to convert box office data to string values 
      * regular expressions, to match different data formats.
## Deliverable 3:
  * For this deliverable, I extracted and transformed the Kaggle Data
    * Then merged the Kaggle metadata DataFrame with the Wikipedia movies DataFrame to create the movies_df DataFrame.
## Deliverable 3:
## Deliverable 4: 
  * In this deliverable the movie database was created
    * The resulting movies_df DataFrame and MovieLens rating CSV data was added to a SQL database.

## Errors: 
  * The challenge required that the resulting movies and ratings tables consist of 6,052 rows and 26,024,289 rows, respectively.
    * The results from my code resulted in 6,077 rows for the movies table and 26,024,289 (importing) rows for the ratings table in my original code, but then 52,058,578 rows in the postgres table.
    * This is something that I need to go back into and fix in my code as it is erroneous.
