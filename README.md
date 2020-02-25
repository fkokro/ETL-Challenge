ETL: Extract, Transform, Load Project

Extract:

I used 5 different datasets from two public platforms. The first source comes via web scraping of the Official Site of the State of New Jersey. The second source from Data USA a public data repository sponsored by Deloitte. The data in the five files include the following information:
•	Cities and city ZIP codes in New Jersey
•	Professional Salary Ranges in New Jersey
•	Median Household Income of Families in New Jersey
•	Wage Disparities Between Genders and Race in New Jersey and Surrounding Areas
•	Wage Distribution 
The following sources for our datasets used:
https://nj.gov/nj/gov/direct/njzips.html
https://datausa.io/profile/geo/new-jersey#economy 
(All four data sources can be found the above link)

Transformation:

In order to transform the public data and use it in the study I performed the following data transformations:
  •	Used Beautiful Soup and the Response function to web scrape for every ZIP code and City in New Jersey.
     o	Parsed through the HTML data to find all relevant data, loaded the data into a list then Pandas Dataframe and last, changed the data type. 
  •	Used Pandas functions in Jupyter Notebook to load four CSV files.
      o	Each CSV file contained information relevant to the New Jersey data study.
      o	Through a series of Pandas operations, I was able to slice dataframes, change data types, and join a relevant data.
      o	Reviewed the data sets and transformed into data frames
    •	Created tables in Postgres to store these transformed data frames, then dumped the data frames into Postgres SQL Database using Sqlalchemy


Load:

The last step was to load these transformed data frames from the Postgres SQL Database into a jupyter notebook using Sqlalchemy. This task was completed to_sql call in Sqlalchemy with Prostgres query string and engine call. I was able to load the transformed data frames into the notebook using SQL as my query language. 


Summary
Now the data is cleaned and prepared I can create a series of visualizations to explore New economic data. The data should reflect wages, gender and race wage discrepancies, New Jersey Cities and top paying jobs. 

