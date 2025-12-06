Power BI Weather Dashboard using WeatherAPI

This project is a real-time Weather Monitoring Dashboard built in Power BI using live data from WeatherAPI.com.
It displays current weather, 7-day forecast, AQI indicators, sunrise/sunset, and multiple environmental metrics.

Dashboard Preview

This dashboard includes:

Current temperature and conditions

City selector

7-day forecast line chart

Air Quality Index indicators

Humidity, pressure, visibility, UV index

Rain probability indicators

Sunrise and sunset timings

A modern dark-themed UI with structured visuals

Features:

Live weather data using WeatherAPI

Current weather metrics (temperature, humidity, wind speed, pressure, precipitation, UV index)

Forecast visualization

Air Quality Index cards (PM10, CO, O3, SO2, PM2.5, NO2)

Rain percentage indicators

Interactive visuals and slicers

Professional dark UI design

Technologies Used:

Power BI Desktop

WeatherAPI (REST API)

Power Query / M Language

DAX


Step 1: Obtain WeatherAPI Key

Create an account at WeatherAPI.com

Generate and copy your API key

This key will be used to authenticate API requests

Step 2: API URL Format
https://api.weatherapi.com/v1/current.json?key=YOUR_API_KEY&q=CITY_NAME

Replace:

YOUR_API_KEY with your WeatherAPI key

CITY_NAME with the city you want to fetch data for

Step 3: Connect Power BI to WeatherAPI

Open Power BI Desktop

Select Get Data → Web

Paste the API URL

Load the JSON response

Step 4: Transform Data in Power Query

Expand the current record

Expand nested fields like condition and air_quality

Rename fields for clean modeling

Close & Apply

Step 5: Build Dashboard Visuals

The dashboard uses:

Cards for temperature, humidity, UV index, pressure

A line chart for 7-day forecast

Gauge for wind speed

AQI indicator cards

Rain percentage bar visuals

Icons for weather conditions

Sunrise and sunset time display

City selection slicers

DAX Measures for Air Quality Indicators

Example reusable DAX measures:

AQI_PM25 = SELECTEDVALUE('Weather Data'[pm2_5])
AQI_PM10 = SELECTEDVALUE('Weather Data'[pm10])
AQI_NO2  = SELECTEDVALUE('Weather Data'[no2])
AQI_SO2  = SELECTEDVALUE('Weather Data'[so2])
AQI_CO   = SELECTEDVALUE('Weather Data'[co])


These measures can be used in cards or KPIs.

Project Structure
WeatherDashboard/
│── WeatherAPI.pbix
│── README.md
│── Weather API.PNG

Conclusion:

This project demonstrates how to integrate Power BI with WeatherAPI to build a real-time, fully interactive weather dashboard.
It covers API connectivity, JSON data transformation, modeling, visual design, and DAX-based AQI indicators.
The dashboard is scalable and can be extended with additional metrics or API endpoints.
