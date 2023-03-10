# sqlalchemy-challenge

In this scenario i have decided to treat myself to a long holiday vacation in Honolulu, Hawaii. To help with my trip planning, i decide to do a climate analysis about the area. The following sections outline the steps that i took to accomplish this task.

## Part 1: Analyze and Explore the Climate Data
In this section, i used Python and SQLAlchemy to do a basic data exploration and analysis of an SQL climate database. Specifically, there is application of  SQLAlchemy ORM queries, Pandas, and Matplotlib. I completed the following steps:

##### a.	summarized local precipitation for the weather stations
##### b.	temperature for a range of trip dates

##### Made use of the SQLAlchemy create_engine() function to connect to the SQLite database (Hawaii.sqlite).
##### The SQLAlchemy automap_base() function to reflect tables into classes, and then save references to the classes named station and measurement.
##### Link Python to the database by creating a SQLAlchemy session.

### Precipitation Analysis
    Find the most recent date in the dataset.
    Using that date, get the previous 12 months of precipitation data by querying the previous 12 months of data.
    Select only the "date" and "prcp" values.
    Load the query results into a Pandas DataFrame, and set the index to the "date" column.
    Sort the DataFrame values by "date".
    Plot the results by using the DataFrame plot method, as the following image shows:
    Use Pandas to print the summary statistics for the precipitation data.

 ### Station Analysis
    Design a query to calculate the total number of stations in the dataset.
    Design a query to find the most-active stations (that is, the stations that have the most rows). To do so, complete the following steps:
    List the stations and observation counts in descending order.
    Answer the following question: which station id has the greatest number of observations?
    Design a query that calculates the lowest, highest, and average temperatures that filters on the most-active station id found in the previous query.
    Design a query to get the previous 12 months of temperature observation (TOBS) data. To do so, complete the following steps:
    Filter by the station that has the greatest number of observations.
    Query the previous 12 months of TOBS data for that station.
    Plot the results as a histogram with bins=12, 
    
    
## Part 2: Design Your Climate App
Designed a Flask API based on the queries that i just developed. To do so, I used Flask to create the following:

???/
#### Home page
???	/api/v1.0/precipitation
#### Daily precipitation totals for last year
???	/api/v1.0/stations
#### Active weather stations
???	/api/v1.0/tobs
#### Daily temperature observations 
???	/api/v1.0/trip/yyyy-mm-dd
#### Min, average & max temperatures for the range beginning with the provided start date through 08/23/17
???	/api/v1.0/trip/yyyy-mm-dd/yyyy-mm-dd
#### Min, average & max temperatures for the range beginning with the provided start - end date range

