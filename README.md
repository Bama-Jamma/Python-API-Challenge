# Python-API-Challenge

# WeatherPy

This repository contains a Python script for analyzing weather data using the OpenWeatherMap API. The script collects weather information for a list of randomly generated cities around the world and performs various analyses on the data. The results are visualized using scatter plots and linear regression.

### Dependencies
The following dependencies are required to run the script:

matplotlib
pandas
numpy
requests
scipy
Make sure you have these libraries installed in your Python environment before running the script.

### Getting Started
Clone the repository to your local machine or download the script directly.
Obtain an API key from OpenWeatherMap by signing up at their website (https://openweathermap.org) and create a free account.
In the script, replace weather_api_key in the line from api_keys import weather_api_key with your API key obtained from OpenWeatherMap.
Run the script in a Python environment.
Functionality
The script performs the following tasks:

Generates a list of random latitude and longitude combinations to represent cities around the world.
Uses the citipy library to determine the nearest city for each latitude and longitude combination.
Fetches weather data for each city using the OpenWeatherMap API.
Parses the retrieved JSON data to extract relevant weather information such as temperature, humidity, cloudiness, wind speed, etc.
Stores the retrieved data in a Pandas DataFrame for further analysis.
Saves the DataFrame as a CSV file for future reference.
Generates scatter plots to visualize the relationships between latitude and various weather parameters such as temperature, humidity, cloudiness, and wind speed.
Performs linear regression analysis on the scatter plots to determine any potential correlations between latitude and weather parameters in the northern and southern hemispheres.

### Results
The script generates four scatter plots and performs linear regression analysis on each of them to evaluate the relationships between latitude and weather parameters.

Latitude vs. Max Temperature:

Shows the relationship between latitude and maximum temperature in Celsius.
Includes separate plots for the northern and southern hemispheres.
Displays the regression line and equation for each hemisphere.
Saves the plot as Fig1.png.
Latitude vs. Humidity:

Shows the relationship between latitude and humidity percentage.
Includes separate plots for the northern and southern hemispheres.
Displays the regression line and equation for each hemisphere.
Saves the plot as Fig2.png.
Latitude vs. Cloudiness:

Shows the relationship between latitude and cloudiness percentage.
Includes separate plots for the northern and southern hemispheres.
Displays the regression line and equation for each hemisphere.
Saves the plot as Fig3.png.
Latitude vs. Wind Speed:

Shows the relationship between latitude and wind speed in miles per hour.
Includes separate plots for the northern and southern hemispheres.
Displays the regression line and equation for each hemisphere.
Saves the plot as Fig4.png.
The linear regression analysis provides insights into the correlations (if any) between latitude and different weather parameters in the northern and southern hemispheres.

### Usage
You can use this script to analyze weather data and visualize the relationships between latitude and various weather parameters. The generated scatter plots and regression analysis can help you understand how latitude influences temperature, humidity, cloudiness, and wind speed. Feel free to modify the script or extend its functionality according to your specific requirements.

#### Note: The script collects weather data for a large number of cities, so it may take some time to complete the data retrieval process depending on your internet connection and API response times.

### Contributors
This script was created by Dustin Shaddix who worked in study groups with multiple classmates.

# VacationPy

### Hotel Search and Map Visualization
This code snippet demonstrates the process of searching for hotels near specific latitude and longitude coordinates and visualizing the hotel locations on a map. The script uses the Geoapify API to retrieve hotel information based on the provided coordinates.

### Prerequisites
Before running the code, ensure that you have the following:

A valid geoapify_key to access the Geoapify API.
Required Python libraries, including requests, pandas, and hvplot.
Hotel Search
To initiate the hotel search, set the parameters in the params dictionary. The parameters include the desired hotel category (accommodation.hotel) and the limit of hotel results to retrieve (limit: 1). Replace geoapify_key with your actual Geoapify API key.

The script iterates through a DataFrame named hotel_df, which contains latitude and longitude coordinates. For each row in the DataFrame, the script performs the following steps:

Extracts the latitude and longitude values.
Updates the params dictionary with the current coordinates to specify the search area.
Sends a request to the Geoapify API to retrieve hotel information based on the provided parameters.
Stores the name of the nearest hotel (if found) in the Hotel Name column of the hotel_df DataFrame.
Prints the search results, displaying the city name and the nearest hotel name.
Map Visualization
The code snippet includes map visualization using the hvplot library. The hotel_df DataFrame is plotted as points on a map, where each point represents a hotel location. The size and color of the points correspond to the humidity level of each hotel's city. The map is configured with appropriate labels, colors, and attributes for better visualization.

To display the map, run the code snippet. The map will show the hotel locations with tooltips containing the hotel names. The size and color of the points represent the humidity level, providing additional information about the hotels' surroundings.

#### Note: The %capture --no-display directive is used to suppress the immediate display of the map in this code snippet, but it can be removed to display the map directly.
