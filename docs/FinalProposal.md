Final Project Proposal

Climate Change Calculator  

🔍 Problem Statement

The Philippines experiences a plethora of typhoons per year. Weather events are becoming more extreme, temperature deviations may affect food supply, among other issues. Additionally, a lot of Philippines cities utilize outdated flood data, implying most infrastructure today are no longer built for the changes the country has experienced today.

This program is a simple yet possibly significant part of weather analysis and predictions, and climate monitoring. It can aid in real world aspects such as: Number one, Agriculture and Farming through indicating whether conditions for crops are suitable enough. Number two, Flood and Disaster readiness through alerting citizens of possible rainfall events. Lastly, number three, Urban Planning to inform infrastructure design and energy systems.

The Philippines is eerily vulnerable to climate change, experiencing 20 or so typhoons per year. This can result in loss of livelihoods, loss of homes, death, a lack of food, and other issues. If this problem is not solved, it can result in extreme poverty of both the people and the government.  

🎯 Project Objectives

1. Find: Find out the day with the highest recorded rainfall
2. Infer: Infer the average daily temperature.
3. eXamine: eXamine data, and aid in interpretation and decision making.
   
⚙️ Planned Features

Your program must have at least 5 features (minimum).
We have provided 2 starter ideas for each dataset — you must design at least 3 additional features.

- Feature 1: (Find the day with the highest rainfall.)
- Feature 2: (Compute the average daily temperature.)
- Feature 3: (Analyze how wind speed varies with different weather statuses.)
- Feature 4: (Find the day with the highest wind speed.)
- Feature 5: (Determine the average wind speed for the week.)
(You may add more features if you like.)

⌨️ Planned Inputs and Outputs

Inputs

What kind of data will the user provide (if any)?
Example: student ID, date range, product name
Outputs

- The user would have to provide the highest and lowest recorded rainfall in a specific area, along with the highest and lowest recorded daily temperature in that area and the possible weather forecast for the week. This will find the average rainfall and daily temperature in order to determine if agriculture and farming are suitable in the area, along with disaster preparation and readiness for heavy rainfall.

What kind of results will your program display?
Example: class averages, top products, weather summary

- The program will display the weather summary, such as the average temperature and the average rainfall in the area in order to establish the risks and appropriate safety measures to be taken in the event of an extreme weather event. In addition, based on the weather summary, the program will also determine the appropriate type of urban planning or structures that will be constructed to better adapt to the weather in the area.


Logic Plan:

Pseudocode:
START
Load weather data from JSON file into weather_records list
(Eacht record contains: date, rainfall_mm, temperature_C, wind_speed_kph, weather_status)

choice = 0

WHILE choice != 7:
    OUTPUT "======================================"
    OUTPUT "   CLIMATE CHANGE CALCULATOR - PHILIPPINES"
    OUTPUT "======================================"
    OUTPUT "[1] Find the day with the highest rainfall"
    OUTPUT "[2] Compute the average daily temperature"
    OUTPUT "[3] Analyze wind speed by weather condition"
    OUTPUT "[4] Find the day with the highest wind speed"
    OUTPUT "[5] Calculate average wind speed for the week"
    OUTPUT "[6] Generate full climate risk summary"
    OUTPUT "[7] Exit program"
    OUTPUT ""
    OUTPUT "Enter your choice (1-7): "
    INPUT choice

    IF choice == 1:
        highest_rainfall = 0
        rainiest_day = ""
        FOR record IN weather_records:
            IF record.rainfall_mm > highest_rainfall:
                highest_rainfall = record.rainfall_mm
                rainiest_day = record.date
        OUTPUT "Wettest day: ", rainiest_day
        OUTPUT "Rainfall: ", highest_rainfall, " mm"
        IF highest_rainfall > 100:
            OUTPUT "EXTREME RAINFALL - High flood risk!"
        ELSE IF highest_rainfall > 50:
            OUTPUT "Heavy rain detected - Prepare for possible flooding"

    ELIF choice == 2:
        total_temp = 0
        day_count = 0
        FOR record IN weather_records:
            total_temp += record.temperature_C
            day_count += 1
        average_temp = total_temp / day_count
        OUTPUT "Average daily temperature: ", average_temp, "°C"
        IF average_temp >= 32:
            OUTPUT "VERY HOT - Risk of heat stress and drought"
        ELSE IF average_temp >= 28:
            OUTPUT "Warm conditions - Normal for tropical climate"
        ELSE IF average_temp < 22:
            OUTPUT "Unusually cool - Monitor crop growth"

    ELIF choice == 3:
        Create empty groups: Sunny, Rainy, Cloudy, Stormy
        FOR record IN weather_records:
            IF record.weather_status == "Sunny":
                Add record.wind_speed_kph to Sunny group
            ELSE IF record.weather_status == "Rainy":
                Add to Rainy group
            ELSE IF record.weather_status == "Cloudy":
                Add to Cloudy group
            ELSE IF record.weather_status == "Stormy":
                Add to Stormy group
        Calculate and display average wind speed for each non-empty group
        OUTPUT "Wind is strongest during: ", highest average group

    ELIF choice == 4:
        max_wind = 0
        windiest_day = ""
        wind_status = ""
        FOR record IN weather_records:
            IF record.wind_speed_kph > max_wind:
                max_wind = record.wind_speed_kph
                windiest_day = record.date
                wind_status = record.weather_status
        OUTPUT "Highest wind speed recorded:"
        OUTPUT "Date: ", windiest_day
        OUTPUT "Wind speed: ", max_wind, " kph"
        OUTPUT "Weather condition: ", wind_status
        IF max_wind >= 118:
            OUTPUT "SUPER TYPHOON LEVEL WINDS!"
        ELSE IF max_wind >= 89:
            OUTPUT "Typhoon-force winds - Extremely dangerous"

    ELIF choice == 5:
        total_wind = 0
        day_count = 0
        FOR record IN weather_records:
            total_wind += record.wind_speed_kph
            day_count += 1
        avg_wind_week = total_wind / day_count
        OUTPUT "Average wind speed this week: ", avg_wind_week, " kph"
        IF avg_wind_week > 40:
            OUTPUT "Very windy week - Secure loose objects"
        ELSE IF avg_wind_week < 15:
            OUTPUT "Calm conditions - Favorable for outdoor activities"

    ELIF choice == 6:
        OUTPUT "CLIMATE RISK SUMMARY REPORT"
        OUTPUT "-------------------------------"
        Run calculations from features 1, 2, 4, 5 silently
        Display:
            - Total days analyzed
            - Average temperature
            - Total rainfall (sum)
            - Highest rainfall day and amount
            - Highest wind speed day and speed
            - Dominant weather condition
        Then display risk assessment:
            IF highest_rainfall > 80 AND max_wind > 70:
                OUTPUT "HIGH RISK: Strong typhoon with flooding likely"
            ELSE IF average_temp > 31 AND total rainfall < 50:
                OUTPUT "DROUGHT RISK: Hot and dry conditions"
            ELSE IF many days with rain > 30 mm:
                OUTPUT "FLOOD RISK: Frequent heavy rain"
            OUTPUT "Recommendation: Upgrade drainage systems and elevate structures"

    ELIF choice == 7:
        OUTPUT "Thank you for using Climate Change Calculator."
        OUTPUT "Stay informed. Stay safe. Protect our planet."
    
    ELSE:
        OUTPUT "Invalid choice! Please enter a number from 1 to 7."

    IF choice != 7:
        OUTPUT ""
        OUTPUT "Press Enter to return to the main menu..."
        WAIT for user to press Enter

END WHILE

End Program


![flowchart](https://github.com/user-attachments/assets/2318fa1e-ca27-4aa9-88bd-66c547384956)



