# **🌦️ Real-Time Weather Analytics & Forecasting Dashboard (Power BI | WeatherAPI)  **
### 📌 Overview

This project fetches real-time and forecast weather data for five major cities in **West Bengal — Digha, Contai, Kolkata, Haldia, and Kharagpur** — using **WeatherAPI.com.**
The data is modeled, transformed, and visualized in **Power BI** to create an interactive weather reporting dashboard.

Locations used:

- **Digha**
- **Contai**
- **Kolkata**
- **Haldia**
- **Kharagpur**

##
### 🧭 Project Background

Weather data from APIs is highly nested and difficult to analyze directly.
To make it usable, I built a proper data pipeline that extracts, transforms, and structures weather information into a meaningful Power BI data model.

This allows clear insights into:

 - Real-time weather
 - 7-day forecasts
 - Hourly trends
 - Air quality
 - City comparisons

##
### 🛠️ What I Set Out to Achieve

**The goal of this project was to:**

 - Convert raw JSON API responses into analysis-ready tables
 - Create a scalable data model for multiple cities
 - Build a structured Fact/Dimension model
 - Use DAX to generate KPIs and weather indicators
 - Deliver a clean, interactive Power BI dashboard

##
### ⚙️ How I Built the Solution

To deliver the final dashboard, I implemented the following steps:

### 1. Data Extraction

Pulled weather data using 5 API URLs for each city.
Expanded nested JSON levels such as ```location```, ```current```, ```forecastday```, and ```hour```.

### 2. Data Cleaning & Transformation

 - Removed unused fields
 - Replaced nulls / handled missing data
 - Corrected data types
 - Removed duplicates
 - Standardized schema across all cities

### 3. Data Modeling (Star Schema)
Created the following structured tables:

 - Master Weather Table (Fact)
 - Location (Dimension)
 - Current Weather (Dimension)
 - Forecast Day (Dimension)
 - Forecast Hours (Dimension)
 - City-specific tables (Digha / Contai / Kolkata / Haldia / Kharagpur)

### 4. DAX Calculations
Developed measures for:

 - AQI Suggestion
 - AQI_statusAQI Status text
 - CO Color
 - Column
 - Curr_Temp_C
 - For_Temp_C
 - Last_update_date_curr
 - Left_value_PM10
 - MAX Value
 - NO2 Color
 - 03 Color
 - PM 10 Color
 - PM 2.5 Color
 - SO2 Color
 - Wind_speed

### 5. Dashboard Development
Designed interactive visuals for:

 - Current weather overview
 - 7-day forecast
 - City-wise comparisons
 - AQI indicator cards

##
### 🎯 Final Outcome
The result is a fully automated weather analytics dashboard that:

 - Tracks real-time and forecast data for 5 cities
 - Uses a clean and scalable star-schema model
 - Shows clear weather patterns and AQI trends
 - Provides user-friendly visuals for temperature, humidity, and air quality
 - Can easily support more cities or more datasets in the future

This project demonstrates strong skills in **API integration, Power Query, DAX, and data modeling—end to end.**

**DashBoard**
<img width="1407" height="792" alt="Dashboard image" src="https://github.com/user-attachments/assets/82d0c6f5-4b36-4988-bf11-609373a97533" />
