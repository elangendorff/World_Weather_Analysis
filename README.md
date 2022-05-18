# World Weather Analysis

## Overview
Expand the PlanMyTrip app to include the following features:
- Add the weather description to the weather data for found cities.
- Allow users to filter the data based on their temperature preferences in order to identify potential travel destinations and nearby hotels.
- Create a travel itinerary between four cities in proximity to each other and create a travel route (including waypoint markers) between them.

## Resources
- Software:
  - Python 3.10.4
    - Packages: citipy, gmaps, numpy, os, pandas, requests, sys, time
  - Jupyter Notebook

## Note to Grader
The Google Maps and Places API key requires a credit card, which I am unable to supply. I have written the code to the best of my ability despite this limitation, and I believe the code will run correctly should you supply your own API key in a `config.py` file. (I, of course, can not be certain of this, as this limitation prevents me for being able to test the code.)

### Config File (for API Keys)
The `config.py` file should be placed in the `World_Weather_Analysis` folder, one level up from each of the three Jupyter Notebooks (`Weather_Database.ipynb`, `Vacation_Search.ipynb`, and `Vacation_Itinerary.ipynb`) used in this Challenge.

The file should contain the following two API keys:
- `weather_api_key` for (OpenWeather)
- `g_key` for Google Maps and Places.

### Missing `g_key` Consequences

#### Hotel Names
When run with a `g_key` equal to `your Google API key goes here`, every city will have a "hotel" called "need g_key". This is because otherwise the Hotel fields would be left blank, and rows with no hotel later get removed from the data. In this case, that would result in an empty DataFrame, and we would be unable to proceed.

When run with an authorized `g_key`, the resulting DataFrame should behave properly.

#### Map Images
Maps created without an authorized `g_key` lack several details (_e.g._, map texture), and route pathing is not available. Since I cannot access an authorized `g_key`, the image files I have saved reflect the images presented as I saw them, despite their lack of some relevant details. They were saved, nonetheless, because the Challenge instructions requested them.

It is my hope that, when run with an authorized `g_key`, you will see the maps as they are intended.