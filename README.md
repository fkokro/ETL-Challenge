![](ETL.png)
# ETL: Extract, Transform, Load Project<br/>
<br/>
**Extract:**<br/>
<br/>
I used 5 different datasets from two public platforms. The first source comes via web scraping of the Official Site of the State of New Jersey. The second source from Data USA a public data repository sponsored by Deloitte. The data in the five files include the following information:<br/>
•	Cities and city ZIP codes in New Jersey<br/>
•	Professional Salary Ranges in New Jersey<br/>
•	Median Household Income of Families in New Jersey<br/>
•	Wage Disparities Between Genders and Race in New Jersey and Surrounding Areas<br/>
•	Wage Distribution <br/>
<br/>
The following sources for our datasets used:<br/>
<br/>
https://nj.gov/nj/gov/direct/njzips.html<br/>
https://datausa.io/profile/geo/new-jersey#economy <br/>
(All four data sources can be found the above link)<br/>
<br/>
**Transformation:**<br/>
<br/>
In order to transform the public data and use it in the study I performed the following data transformations:<br/>
  •	Used Beautiful Soup and the Response function to web scrape for every ZIP code and City in New Jersey.<br/>
     o	Parsed through the HTML data to find all relevant data, loaded the data into a list then Pandas Dataframe and last, changed the data type. <br/>
  •	Used Pandas functions in Jupyter Notebook to load four CSV files.<br/>
      o	Each CSV file contained information relevant to the New Jersey data study.<br/>
      o	Through a series of Pandas operations, I was able to slice dataframes, change data types, and join a relevant data.<br/>
      o	Reviewed the data sets and transformed into data frames<br/>
    •	Created tables in Postgres to store these transformed data frames, then dumped the data frames into Postgres SQL Database using Sqlalchemy<br/>
<br/>
<br/>
**Load:**<br/>
<br/>
The last step was to load these transformed data frames from the Postgres SQL Database into a jupyter notebook using Sqlalchemy. This task was completed to_sql call in Sqlalchemy with Prostgres query string and engine call. I was able to load the transformed data frames into the notebook using SQL as my query language. <br/>
<br/>
<br/>
**Summary**<br/>
Now the data is cleaned and prepared I can create a series of visualizations to explore New economic data. The data should reflect wages, gender and race wage discrepancies, New Jersey Cities and top paying jobs. 

