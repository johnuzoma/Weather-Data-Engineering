# Weather-Data-Engineering
### Project end-to-end architecture
<img width="887" alt="project e2e schematic" src="https://github.com/johnuzoma/Weather-Data-Engineering/assets/18267074/072e85f1-5aa2-4b04-a4c6-b37e2417586b">


### Data Pipeline in Azure Data Factory
<img width="847" alt="data pipeline" src="https://github.com/johnuzoma/Weather-Data-Engineering/assets/18267074/e639556e-9522-4f3c-bb3f-ab165a62ef0c">

1. The pipeline begins with the "Set variable" activity which declares a variable and sets its value equal to a folder structure involving the current year, month and day.
2. Then we have 2 "Copy" activities, each of which are used for pulling current and forecast weather data fom the API, by passing the longitude, latitude and API key as parameters.
  
    - In the top "Copy" activity, the current weather data is loaded into the folder declared by initial variable as a JSON file.
    - In the bottom "Copy" activity, the forecast weather data is loaded directly into the root Files folder as another JSON file.
   
4. Then we have the top notebook which cleans and transforms the current weather data. The data is read from a defined base parameter, PARAM_file_path, which takes the value of the dynamic path for the current weather JSON file.
5. The second notebook for the forecast data has no base parameters, since the data is simply read from the JSON file in root Files folder.
6. The dataflow is used for appending (analogous to UNION in SQL) the current and forecast weather data, and finally loading the result into a lakehouse table.
 
### Power BI Report
*Snapshot as of April 3, 2024*

<img width="604" alt="PBI report" src="https://github.com/johnuzoma/Weather-Data-Engineering/assets/18267074/9a660940-24e8-4c42-b09a-c92f5197e719">



