# Azure Weather Streaming Project

A real-time data streaming pipeline that fetches weather data for Chennai, India, processes it, and visualizes it using Azure services.

## Overview
- **Objective**: Stream and analyze Chennai's weather (temperature, humidity, UV) with 3-day forecasts.
- **Data Source**: WeatherAPI.com (JSON API).
- **Tools**: Azure Databricks, Event Hubs, Microsoft Fabric (Eventstream, KQL Database), Power BI.

## Architecture
1. **Databricks**: Fetches weather data via API and streams JSON to Event Hubs.
2. **Event Hubs**: Receives and forwards real-time weather data.
3. **Microsoft Fabric**: Processes data via Eventstream, stores it in a KQL database table.
4. **Power BI**: Visualizes current conditions, trends, and 3-day predictions.

## Repository Contents
- `databricks/`: PySpark script (`weather_streaming.py`).
- `event_hubs/`: Configuration details (`event_hubs_config.txt`).
- `fabric/`: KQL table schema (`weather_table.kql`) and Eventstream screenshots.
- `powerbi/`: Dashboard screenshots (current weather, trends, predictions).

## Setup
1. **Databricks**: Run `weather_streaming.py` with your API key and Event Hubs connection string.
2. **Event Hubs**: Configure namespace and hub as per `event_hubs_config.txt`.
3. **Fabric**: Set up Eventstream (see screenshots) and create the KQL table with `weather_table.kql`.
4. **Power BI**: Connect to the Fabric KQL database and build the dashboard.

## Screenshots
### Eventstream Setup
![Event Hubs Input](fabric/eventstream_screenshots/input.png)  
![KQL Output](fabric/eventstream_screenshots/output.png)  

### Power BI Dashboard
![Current Weather](powerbi/dashboard_screenshots/current_weather.png)  
![Trends](powerbi/dashboard_screenshots/trends.png)  
![Predictions](powerbi/dashboard_screenshots/predictions.png)  

## Notes
- Replace API keys and connection strings with your own.
- Power BI `.pbix` file available upon request.

---
*By [Your Name] | [LinkedIn](https://linkedin.com/in/yourprofile)*
