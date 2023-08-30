# Challenge6_python-api-challenge

Two data sources (Weather from OpenWeather and hotel accomodation from geoapify) are look at and plot some graphs and maps and make some conclusions.
All the codes are derived from lecture notes and ChatGPT.


WeatherPy:
A random data from 576 cities are generated from certain latitude and longitude range where latitude,longitude, max temperature, 
humidity, cloudiness, wind speed, city name and UTC time are extracted and put into a dataframe.

The dataset are split into Northern Hemisphere (NH) and Southern Hemisphere (SH) using the Equator line.

The following plots are generate for each hemisphere with regression lines with soem preliminary conclusion derives from the graph.
1. Temperature vs Latitude
	- NH:Rvalue of -0.68 is high and suggest strong negative relationship between temperature and latitude.
	     Temperature decreases as Latitude increases. This make sense since temperature drop lower as we head to North pole.
	- SH:Rvalue of 0.75 is high and suggest strong positive relationship between temperature and latitude.
	     Temperatute increases as Latitude increases.  Same effect as above and temperature do rise as we get closer to Equator line.
2. Humidity vs Latitude
	- NH:Rvalue of -0.01 suggest a very weak negative relationship between humidity and latitude.
	     The scatter plot is too wide spread to make any meaningful conclusion.
	- SH:Rvalue of 0.08 suggest a very weak positive relationship between humidity and latitude.
	     The scatter plot is also too wide spread to make any meaningful conclusion.
3. Cloudiness vs Latitidue
	- NH:Rvalue of -0.07 suggest a very weak negative relationship between cloudiness and latitude.
	     The scatter plot is too wide spread to make any meaningful conclusion.
	- SH:Rvalue of 0.01 suggest a very weak positive relationship between cloudiness and latitude.
	     The scatter plot is also too scattered to make any meaningful conclusion.
4. Wind Speed vs Latitude
	- NH:Rvalue of -0.16 suggest a weak relationship between wind speed and latitude.
	     The scatter plot is too wide spread to make any meaningful conclusion.
	- SH:Rvalue of -0.09 suggest a weak relationship between wind speed and latitude.
	     The scatter plot is also too wide spread to make any meaningful conclusion.


VacationPy:
using Geoapify API and geoViews Python library to plan for vacation based on the following criterai:
1. A max temprature lowe than 27 degrees but higherthan 21
2. Wind speed less than 4.5 m/s
3. Cloudiness < 5
4. Humidity < 80

A search for the nearest hotel within 10km of the city Latitude and Longitude and a map is shown with hover for the name of hotel and city as well.