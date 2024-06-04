** Please note: I am no longer using OpenWeatherMap API for this project. I am using the Met Eireann API. **

### Executive Summary
Using pipeline activities and PySpark notebooks in MS Fabric, I pulled Dublin's weather data from the Met Eireann API and created a dashboard to track weather warnings and forecasts.

### Solution Architecture
<img width="720" alt="image" src="https://github.com/johnuzoma/Weather-Data-Engineering/assets/18267074/210c7418-8db4-4b31-819b-ad512b3fbd3d">

### Data Pipelines

###### Pipeline for Dublin Weather Forecast (Text)

<img width="406" alt="image" src="https://github.com/johnuzoma/Weather-Data-Engineering/assets/18267074/3013f4cc-da4c-47c4-839d-3b6ff8db11df">

###### Pipeline for Dublin Weather Forecast (Numeric) - Source data is in XML format, hence I used notebooks to extract and transform it

<img width="550" alt="image" src="https://github.com/johnuzoma/Weather-Data-Engineering/assets/18267074/cefa2286-b6d8-4380-854f-a9b2353d0ad1">

###### Pipeline for Dublin Weather Warnings

<img width="406" alt="image" src="https://github.com/johnuzoma/Weather-Data-Engineering/assets/18267074/3fc9abe0-0d25-4a3b-830c-bab59c7d9e10">
 
### Power BI Dashboard
###### Snapshot as of May 28, 2024 11:40 am

<img width="890" alt="image" src="https://github.com/johnuzoma/Weather-Data-Engineering/assets/18267074/1e63b5b6-3c90-4d87-906a-e71ea21f01a0">







