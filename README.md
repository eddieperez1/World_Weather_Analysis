# World_Weather_Analysis
This project was written in Python using Jupyter Notebooks. config.py stores the API keys used in this project as strings in variables weather_key and g_key. APIs are [openweathermap](https://home.openweathermap.org/) and [Google Maps API](https://developers.google.com/maps). config.py is needed to run the code in this project.

## Overview of Repository

The project focuses on improving a fake app called PlanMyTrip to practice using APIs. A few recommended changes were suggested to take the app to the next level. Specifically, adding the weather description to the weather data. Then, use input statements to filter the data for their weather preferences, which will be used to identify potential travel destinations and nearby hotels. From the list of potential travel destinations, choose four cities to create a travel itinerary. Finally, using the Google Maps Directions API, a travel route between the four cities in New Zealand as well as a marker layer map.

## Deliverable 1: Retrieve Weather Data
In Weather_Database.ipynb in main folder, 2,000 random pairs of Latitude and Longitude were created. Then a list was created with these 2,000 pairs and the nearby city for each latitude and longitude pair was found using [citipy](https://github.com/wingchen/citipy) module. An API call was performed with the OpenWeatherMap. 

The following data was retrieved:
- Latitude and Longitude
- Maximum temperature
- % humidity
- % cloudiness
- Wind speed
- Weather description 

The data was added to a Pandas DataFrame then added to Weather_Database/WeatherPy_Database.csv

## Deliverable 2: Create a Customer Travel Destinations Map
config.py is required for Vacation_Search.ipynb in Vacation_Search folder to run. In Vacation_Search.ipynb, Two input statements that prompt the user to enter their minimum and maximum temperature criteria for their vacation were created. The data Weather_Database/WeatherPy_Database.csv was imported into city_data_df Pandas dataframe. ThenU the dataframe was filtered using input minimum and maximum temperature. Next, hotels dataframe was created to store city_data_df with hotel names. The hotels names were extracted from Google Places API. The hotels_df was cleaned by dropping data with no hotel names. The cleaned hotels_df dataframe was save to Vacation_Search/WeatherPy_vacation.csv. Using [gmaps](https://pypi.org/project/python-gmaps/) module with google API key, a google map was made with html descriptive markers for each hotel. 

![Vacation Search Hotels Map](/Vacation_Search/WeatherPy_vacation_map.png)

## Deliverable 3: Create a Travel Itinerary Map
config.py is required for Vacation_Itinerary.ipynb in Vacation_Itinerary folder to run. In Vacation_Itinerary.ipynb, import Vacation_Search/WeatherPy_vacation.csv into a Pandas dataframe. From the vacation search map in deliverable 2, four cities were choose in New Zealand within close proximity of each other. Using Google Directions API, create a route with gmaps module. From the four cities, the latitude and longitude were extracted to use with gmaps direction layer to add to gmaps figure.

![Vacation Travel Route](/Vacation_Itinerary/WeatherPy_travel_map.png)

Then using the Google Map Places API, A map was made with gmaps with Hotel Name, City, Country, and Current Weather for the four cities in New Zealand.

![Vacation Travel Map Markers](/Vacation_Itinerary/WeatherPy_travel_map_markers.png)
