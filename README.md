# python-api-challenge
Hotel Mapping Assignment

Overview

This project involves analyzing weather data, filtering cities based on specific criteria, and identifying nearby hotels using the Geoapify API. The data is visualized on an interactive map to provide insights into the chosen cities and their accommodations.

Objectives

Filter cities based on weather conditions such as temperature and humidity.

Use the Geoapify Places API to search for hotels near the filtered cities.

Visualize the selected cities and hotels on an interactive geographic map.

Steps

1. Data Preparation

Input Data: A CSV file (cities.csv) containing city weather data.

Processing: Load the data into a Pandas DataFrame and filter cities based on:

Maximum temperature range (e.g., 20°C to 30°C).

Humidity levels below a certain threshold (e.g., < 60%).

Output: A filtered DataFrame with columns for city, country, latitude, longitude, and humidity.

2. Hotel Search

API Setup:

Use the Geoapify Places API to find hotels within a 5 km radius of each city.

Configure API request parameters for hotel search.

Implementation:

Iterate through the filtered DataFrame.

Use latitude and longitude to query the API.

Extract the hotel name from the API response.

Handle cases where no hotel is found by marking entries as "No hotel found."

3. Visualization

Interactive Map:

Create an interactive map using hvplot.pandas.

Plot city locations as points, with size based on humidity and color coded by hotel name.

Display additional information such as city name, country, and hotel name on hover.

Map Configuration:

Use a light base map (CartoLight).

Configure map dimensions for better visualization.

Dependencies

Ensure the following Python libraries are installed:

pandas

requests

hvplot

geoviews

To install missing dependencies:

pip install pandas requests hvplot geoviews

Project Files

cities.csv: Input file containing weather data.

api_keys.py: File containing the Geoapify API key.

Generated interactive map visualizing hotels near selected cities.

Usage

Place the cities.csv and api_keys.py files in the project directory.

Ensure the Geoapify API key is correctly configured in api_keys.py:

geoapify_key = "YOUR_API_KEY"

Run the Python script or Jupyter Notebook to:

Filter the cities based on specified criteria.

Search for hotels near the filtered cities.

Visualize the results on an interactive map.

Review the interactive map for insights into the filtered cities and their ho
