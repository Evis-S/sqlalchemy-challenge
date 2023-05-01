# sqlalchemy-challenge
This homework analyzes Hawaii precipitation and weather station data, and produces visualizations of rainfall and temperature patterns.

Part 1: Analyze and Explore the Climate Data
We used Python and SQLAlchemy to do a basic climate analysis and data exploration of our climate database. Specifically, we used SQLAlchemy ORM queries, Pandas, and Matplotlib.

Precipitation Analysis
Find the last date in the data set.
We use this date for it
 get the previous 12 months of rainfall data.
 Selected only the "date" and "prcp" values.
Loaded the query results into a Pandas DataFrame. Explicitly set the column names.
Sorted the DataFrame values by "date"
Plot the results in a bar chart.

Station Analysis

A query is designed to calculate the total number of stations, and 9 stations found. To find the most active station list, and observation counts is sorted in descending order. Station USC00519281 has the highest number of observations.

A query is created to retrieve the last 12 months of temperature observation data (TOBS) and filter by the station with the highest number of observations. The Plot for the results as a histogram with bins=12.

Part 2: Design Your Climate App
The following routes are created by using Flask.
/
Homepage.
List all the available routes.
/api/v1.0/precipitation
Convert the query results from your precipitation analysis (i.e. retrieve only the last 12 months of data) to a dictionary using date as the key and prcp as the value.
Return the JSON representation of your dictionary.
/api/v1.0/stations
Return a JSON list of stations from the dataset.
/api/v1.0/tobs
Query the dates and temperature observations of the most-active station for the previous year of data.
Return a JSON list of temperature observations for the previous year.
/api/v1.0/<start> and /api/v1.0/<start>/<end>
Return a JSON list of the minimum temperature, the average temperature, and the maximum temperature for a specified start or start-end range.
For a specified start, calculate TMIN, TAVG, and TMAX for all the dates greater than or equal to the start date.
For a specified start date and end date, calculate TMIN, TAVG, and TMAX for the dates from the start date to the end date, inclusive.
