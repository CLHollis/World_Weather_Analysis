<img src="https://github.com/CLHollis/World_Weather_Analysis/blob/5fd413055075978ca0997d31ac45af652f83e7f7/CHALLENGE/title_photo.PNG" width="1000" height="440">

Jack loves the PlanMyTrip app. Beta testers love it too. And, as with any new product, they’ve recommended a few changes to take the app to the next level. Specifically, they recommend adding the weather description to the weather data you’ve already retrieved in this module. Then, you'll have the beta testers use input statements to filter the data for their weather preferences, which will be used to identify potential travel destinations and nearby hotels. From the list of potential travel destinations, the beta tester will choose four cities to create a travel itinerary. Finally, using the Google Maps Directions API, you will create a travel route between the four cities as well as a marker layer map.

## The Challenging Part
1. Retrieve Weather Data for over 500 random possible vacation destinations for the PlanMyTrip app
   1) In a new Jupyter Notebook Python file [Weather_Database.ipynb](https://github.com/CLHollis/World_Weather_Analysis/blob/a92e4f776f14014018c8ecf7d52093b35bad0274/CHALLENGE/Weather_Database/Weather_Database.ipynb), find 2000 random latitude/longitude coordinates and grab the nearest cities to those.
   2) Grab the weather conditions for all the cities by calling data from the [Open Weather Map API](https://home.openweathermap.org/). 
   3) Make it into a dataframe & save it as [WeatherPy_Database.csv](https://github.com/CLHollis/World_Weather_Analysis/blob/a92e4f776f14014018c8ecf7d52093b35bad0274/CHALLENGE/Weather_Database/WeatherPy_Database.csv)

        <img src="https://github.com/CLHollis/World_Weather_Analysis/blob/5fd413055075978ca0997d31ac45af652f83e7f7/CHALLENGE/Weather_Database/weather_database.PNG" width="900" height="150">

2. Create a Customer Travel Destinations Map
   1) Start a new Jupyter Notebook Python file [Vacation_Search.ipynb](https://github.com/CLHollis/World_Weather_Analysis/blob/a92e4f776f14014018c8ecf7d52093b35bad0274/CHALLENGE/Vacation_Search/Vacation_Search.ipynb), and use the  [WeatherPy_Database.csv](https://github.com/CLHollis/World_Weather_Analysis/blob/a92e4f776f14014018c8ecf7d52093b35bad0274/CHALLENGE/Weather_Database/WeatherPy_Database.csv), have the user enter in their minimum and maximum desired temps to narrow down the search for an ideal destination. (Here, we use 80 & 100 as the example.)
   2) Create a new dataframe from the filtered results
   3) Using [Google Maps APIs](https://jupyter-gmaps.readthedocs.io/en/latest/tutorial.html), search and find a hotel for each sity and add it to the dataframe. 
   4) Save it as [WeatherPy_vacation.csv](https://github.com/CLHollis/World_Weather_Analysis/blob/a92e4f776f14014018c8ecf7d52093b35bad0274/CHALLENGE/Vacation_Search/WeatherPy_vacation.csv)
   5) Use the [WeatherPy_vacation.csv](https://github.com/CLHollis/World_Weather_Analysis/blob/a92e4f776f14014018c8ecf7d52093b35bad0274/CHALLENGE/Vacation_Search/WeatherPy_vacation.csv) to create a map with pop-up markers listing each city's hotel name, city, country code, current weather and temp.

         <img src="https://github.com/CLHollis/World_Weather_Analysis/blob/a92e4f776f14014018c8ecf7d52093b35bad0274/CHALLENGE/Vacation_Search/WeatherPy_vacation_map.PNG" width="700" height="350">

3. Create a Travel Itinerary Map using 4 cities close to each other
   1) Using the [WeatherPy_vacation.csv](https://github.com/CLHollis/World_Weather_Analysis/blob/a92e4f776f14014018c8ecf7d52093b35bad0274/CHALLENGE/Vacation_Search/WeatherPy_vacation.csv), filter out all but the four chosen cities.
   2) Using gmaps.directions function, creat a driving guide map for traveling to all four cities, starting and ending in the same city.

         <img src="https://github.com/CLHollis/World_Weather_Analysis/blob/a92e4f776f14014018c8ecf7d52093b35bad0274/CHALLENGE/Vacation_Itenerary/WeatherPy_travel_map.PNG" width="700" height="700"> 

   4) Using the infobox function, create a map with pop up markers again for the 4 destination cities to know what hotel and current weather conditions are. 

         <img src="https://github.com/CLHollis/World_Weather_Analysis/blob/a92e4f776f14014018c8ecf7d52093b35bad0274/CHALLENGE/Vacation_Itenerary/WeatherPy_travel_map_markers.PNG" width="800" height="675">


## Tools 
- Python 3.7.6
- Jupyter Notebook, 6.0.3
- OpenWeatherMap.org API
- Google Map API

## Credits
- title photo from: https://www.goldcoastholidays.com.au/ > https://d2rdhxfof4qmbb.cloudfront.net/wp-content/uploads/20180221131107/iStock-465629027.jpg
