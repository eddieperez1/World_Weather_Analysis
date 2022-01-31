# World_Weather_Analysis
This project was written in python using Jupyter Notebooks. config.py stores the API keys used in this project as strings in variables weather_key and g_key. APIs are [openweathermap](https://home.openweathermap.org/) and [Google Maps API](https://developers.google.com/maps). config.py is needed to run the code in this project.
## Overview of Repository

The project focuses on improving a fake app called PlanMyTrip to practice using APIs. A few recommended changes were suggested to take the app to the next level. Specifically, adding the weather description to the weather data. Then, use input statements to filter the data for their weather preferences, which will be used to identify potential travel destinations and nearby hotels. From the list of potential travel destinations, choose four cities to create a travel itinerary. Finally, using the Google Maps Directions API, a travel route between the four cities in New Zealand as well as a marker layer map.

## Deliverable 1: Retrieve Weather Data
In Weather_Database.ipynb in main folder, 2,000 random pairs of Latitude and Longitude were created. Then a list was created with these 2,000 pairs and the nearby city for each latitude and longitude pair was found using [citipy](https://github.com/wingchen/citipy) module. An API call was performed with the OpenWeatherMap. 
The following data was retrieved
- Latitude and Longitude
- Maximum temperature
- % humidity
- % cloudiness
- Wind speed
- Weather description 
The data was added to a Pandas DataFrame then added to Weather_Database/WeatherPy_Database.csv
## Deliverable 2: Create a Customer Travel Destinations Map

## Deliverable 3: Create a Travel Itinerary Map
