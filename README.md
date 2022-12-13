# B9DA108 Programming for Data Analysis (B9DA108_2223_TMD1S)
CA_ONE_(60%) Primary objective: To design and develop a Data Acquisition and Preprocessing Pipeline.

You are required to develop a Data Acquisition and Preprocessing Pipeline of your choice, including data acquisition (API, Web scraping, DB Extract etc.), Extraction of features and Transformations as appropriate, followed by loading into an appropriate database. The focus of the complexity of the pipeline is your choice.

This is a repository created for CA1 of Programming for Data Analysis.

repository link - https://github.com/Siddhesh1886/B9DA108_Programming_For_Data_Analysis_CA1_10628348.git

Name - Siddhesh Anant Sawant
ID - 10628348
Group - C

For this assessment, I have decided to scrape the data from below website.

https://www.zucar.ie/find-a-vehicle?page=1 

I have used json API package to scrape the data since the data from the above website is in json format. I have written for loop to get the data from 9 pages and stored it in Python dataframe. I have performed below operations on the dataframe:

-	Used head() function to check if data is properly stored in the dataframe.
-	shape method to verify the dimensions of the data.
-	After my initial analysis, I have dropped irrelevant columns using drop() function.
-	I have checked for null values in each column and replaced them with 0s.
-	Then I verified the data types of each column using info() function. I noticed that some of the columns were not having appropriate data types. I have converted date columns as datetime data-type and numeric columns as float data-types.
-	Renamed few columns for better understanding.
-	Feature Engineering: 
o	I have computed ‘discount (%)’ from 'price' and 'was_price' columns.
o	Created combined 'make-model' column from 'make' and 'model' columns.
o	Created 'registration_year' column from ‘registration_date'.


Post data acquisition, data transformation and feature engineering techniques, I have come up with below questions based on the data:

1. What are the second-hand cars available in 'Cork' with the budget of '15000-25000' Euros?
2. How many of these have model year and registration year on or after 2017?
3. How many of these are with Petrol - Manual transmission?
4. Can you please share more details of these cars like price, color, body-type and so on.
5. What will be the final cost of ‘Nissan-Juke’ if I go with 60 months finance option?

I have applied dataframe filtering techniques on appropriate columns to find out the answers to the above questions. 

Finally, I have stored the final cleaned dataframe in PostgreSQL database which is installed on my machine locally. I have used ‘psycopg2’ package to establish the connection between Jupyter notebook and the database.  

