# Python API What's the Weather Like?
Python, APIs, JSON traversals, Heat Map, and Geocode

## Background

Whether financial, political, or social -- data's true power lies in its ability to answer questions definitively. So let's take what you've learned about Python requests, APIs, and JSON traversals to answer a fundamental question: "What's the weather like as we approach the equator?"

Now, we know what you may be thinking: _"Duh. It gets hotter..."_

But, if pressed, how would you **prove** it?

![Equator](Images/equatorsign.png)

## Technologies
* API
* Matplotlib
* Pandas
* Python
* gmaps
* Scipy

## Part I - WeatherPy

In this example, you'll be creating a Python script to visualize the weather of 500+ cities across the world of varying distance from the equator. To accomplish this, you'll be utilizing a [simple Python library](https://pypi.python.org/pypi/citipy), the [OpenWeatherMap API](https://openweathermap.org/api), and a little common sense to create a representative model of weather across world cities.

Your first requirement is to create a series of scatter plots to showcase the following relationships:

* Temperature (F) vs. Latitude
* Humidity (%) vs. Latitude
* Cloudiness (%) vs. Latitude
* Wind Speed (mph) vs. Latitude

After each plot add a sentence or too explaining what the code is and analyzing.

Your second requirement is to run linear regression on each relationship, only this time separating them into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude):

* Northern Hemisphere - Temperature (F) vs. Latitude
* Southern Hemisphere - Temperature (F) vs. Latitude
* Northern Hemisphere - Humidity (%) vs. Latitude
* Southern Hemisphere - Humidity (%) vs. Latitude
* Northern Hemisphere - Cloudiness (%) vs. Latitude
* Southern Hemisphere - Cloudiness (%) vs. Latitude
* Northern Hemisphere - Wind Speed (mph) vs. Latitude
* Southern Hemisphere - Wind Speed (mph) vs. Latitude

After each pair of plots explain what the linear regression is modeling such as any relationships you notice and any other analysis you may have.


### Part II - VacationPy

Now let's use your skills in working with weather data to plan future vacations. Use jupyter-gmaps and the Google Places API for this part of the assignment.

* Create a heat map that displays the humidity for every city from the part I of the homework.

  ![heatmap](Images/heatmap.png)

* Narrow down the DataFrame to find your ideal weather condition. For example:

  * A max temperature lower than 80 degrees but higher than 70.

  * Wind speed less than 10 mph.

  * Zero cloudiness.

  * Drop any rows that don't contain all three conditions. You want to be sure the weather is ideal.

* Using Google Places API to find the first hotel for each city located within 5000 meters of your coordinates.

* Plot the hotels on top of the humidity heatmap with each pin containing the **Hotel Name**, **City**, and **Country**.

  ![hotel map](Images/hotel_map.png)
  
  ### Observations
  
 *   After collecting weather data from 549 random cities around the world using the OpenWeatherMap API, which was collected  in May 2019. The data showed collected was maximum temperature 42.78 C (108.86 F), humidity (%), cloudiness (%) and wind speed (in mph) with the corresponding city, and with respect to the geo-coordinate, Latitude. Temperatures are higher closer to the Equator (at 0° Latitude) lower in the Northern Hemisphere, at this time of year in May. This data on temperature is the result of seasons and the tilt of the Earth's axis compared to the plane of its revolution around the Sun. Throughout the year the northern and southern hemispheres are alternately turned either toward or away from the sun depending on Earth's position in its orbit. The hemisphere turned toward the sun receives more sunlight and is in summer, while the other hemisphere receives less sun and is in winter.
*	There is a strong positive correlation between latitude and the max temperature.
* There is small to no correlation between humidity and latitude as well as with cloudiness and latitude. A small group of cities exhibited abnormally low humidity levels in the Northern Hemisphere in the US.  
*	Wind speeds increase in the upper and lower halves on the hemisphere, especially in the north.  There isn't a good relationship between wind speed and latitude. The difference isn't significant enough.
