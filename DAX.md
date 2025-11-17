```
AQI Suggestion = 
VAR AQI = ROUND(SELECTEDVALUE('Current'[current.air_quality.pm10]), 0)
RETURN
    SWITCH(
        TRUE(),
        AQI <= 50, "Air is clean and healthy",
        AQI <= 100, "Acceptable air quality, stay active",
        AQI <= 150, "Sensitive groups should reduce outdoor time",
        AQI <= 200, "Avoid outdoor exertion",
        AQI <= 300, "Avoid outdoor activity if possible",
        "Stay indoors and wear a mask if going outside"
    )
```
```
AQI_statusAQI Status text = 
VAR AQI = ROUND(SELECTEDVALUE('Current'[current.air_quality.pm10]),0)
RETURN
    SWITCH(
        TRUE(),
        AQI <= 50, "Good",
        AQI <= 100, "Moderate",
        AQI <= 150, "Unhealthy for sensitive",
        AQI <= 200, "Unhealthy",
        AQI <= 300, "Very Unhealthy",
        "Hazardous"
    )
```
```
CO Color = 
VAR AQI = ROUND(SELECTEDVALUE('Current'[current.air_quality.co]),0)
RETURN
    SWITCH(
        TRUE(),
        AQI <= 50, "#43d946",
        AQI <= 100, "#fff570",
        AQI <= 200, "#d99343",
        AQI <= 300, "#ff5b0f",
        "#d95243"
    )
```
```
Curr_Temp_C = SUM('Current'[current.temp_c]) & " °C"
```
```
For_Temp_C = SUM('Forcast_Day'[forecast.forecastday.day.avgtemp_c]) & " °C"
```
```
Last_update_date_curr = "Last updated, " & FORMAT(FIRSTNONBLANK('Current'[current.last_updated],""),"dd mmm")
```
```
Left_value_PM10 = [MAX Value] - SUM('Current'[current.air_quality.pm10])
```
```
MAX Value = 300
```
```
NO2 Color = 
VAR AQI = ROUND(SELECTEDVALUE('Current'[current.air_quality.no2]),0)
RETURN
    SWITCH(
        TRUE(),
        AQI <= 50, "#43d946",
        AQI <= 100, "#fff570",
        AQI <= 200, "#d99343",
        AQI <= 300, "#ff5b0f",
        "#d95243"
    )
```
```
O3 Color = 
VAR AQI = ROUND(SELECTEDVALUE('Current'[current.air_quality.o3]),0)
RETURN
    SWITCH(
        TRUE(),
        AQI <= 50, "#43d946",
        AQI <= 100, "#fff570",
        AQI <= 200, "#d99343",
        AQI <= 300, "#ff5b0f",
        "#d95243"
    )
```
```
PM 10 Color = 
VAR AQI = ROUND(SELECTEDVALUE('Current'[current.air_quality.pm10]),0)
RETURN
    SWITCH(
        TRUE(),
        AQI <= 50, "#43d946",
        AQI <= 100, "#fff570",
        AQI <= 200, "#d99343",
        AQI <= 300, "#ff5b0f",
        "#d95243"
    )
```
```
PM 2.5 Color = 
VAR AQI = ROUND(SELECTEDVALUE('Current'[current.air_quality.pm2_5]),0)
RETURN
    SWITCH(
        TRUE(),
        AQI <= 50, "#43d946",
        AQI <= 100, "#fff570",
        AQI <= 200, "#d99343",
        AQI <= 300, "#ff5b0f",
        "#d95243"
    )
```
```
SO2 Color = 
VAR AQI = ROUND(SELECTEDVALUE('Current'[current.air_quality.so2]),0)
RETURN
    SWITCH(
        TRUE(),
        AQI <= 50, "#43d946",
        AQI <= 100, "#fff570",
        AQI <= 200, "#d99343",
        AQI <= 300, "#ff5b0f",
        "#d95243"
    )
```
```
Wind_speed = SUM('Current'[current.wind_kph]) & " kph"
```
