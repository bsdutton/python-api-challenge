# python-api-challenge

## SOLUTIONS INDEX

### Complete Solutions for WeatherPy are in WeatherPy-main.ipynb
* Working file is WeatherPy-working.ipynb

### Analysis and Notes are in python-api challenge - SOLUTIONS README.md
* This is important because the randomly selected cities list used had NO cities where humidity was > 100%.
  * I had no data to clean.
* When this is run again, a new set of cities will be randomly selected; and, this may not be the case.
* Unless I lock the cities list by commenting out the random selection statements.

### WeatherPy/output_data contains all required CSVs and PNGs which include:
1) city.csv as required output of cleaned DataFrame city_weather2
  * I initially sent my output to city_weather.csv because I thought the output_data_file = "output_data/cities.csv" meant to preserve the cities list in a CSV.
  * I sent the cities list used for the solutions to cities_list.csv.
  * I saved city_weather.csv in output_data/practice folder.
2) request_response_log.csv to satisfy the required printlog for the API requests with responses.
  * I display the printlog as the for-loop with try-except are working through the API calls.
  * I also sent the printlog to a list.
  * I used the list to create a DataFrame which I sent to a CSV.
3) response_error_log.csv
  * I included the same steps in the for-loop with try-except to show the list and then DataFrame of the cities in the random selected list that do not exist in OpenWeatherMap.
#### PNG image for each scatter plot was made, but I think the PDF image turns out much better.  I made both.  Rubric calls for PNG.  Images include:
1) MAX_Temp_vs_Latitude.pdf
2) MAX_Temp_vs_Latitude.png
3) Percent_Humidity_vs_Latitude.pdf
4) Percent_Humidity_vs_Latitude.png
5) Percent_Cloudiness_vs_Latitude.pdf
6) Percent_Cloudiness_vs_Latitude.png
7) Wind_Speed_vs_Latitude.pdf
8) Wind_Speed_vs_Latitude.png
9) Northern_Hemisphere_MAX_Temp_vs_Latitude.pdf
10) Northern_Hemisphere_MAX_Temp_vs_Latitude.png
11) Southern_Hemisphere_MAX_Temp_vs_Latitude.pdf
12) Southern_Hemisphere_MAX_Temp_vs_Latitude.png
13) Northern_Hemisphere_Percent_Humidity_vs_Latitude.pdf
14) Northern_Hemisphere_Percent_Humidity_vs_Latitude.png
15) Southern_Hemisphere_Percent_Humidity_vs_Latitude.pdf
16) Southern_Hemisphere_Percent_Humidity_vs_Latitude.png
17) Northern_Hemisphere_Percent_Cloudiness_vs_Latitude.pdf
18) Northern_Hemisphere_Percent_Cloudiness_vs_Latitude.png
19) Southern_Hemisphere_Percent_Cloudiness_vs_Latitude.pdf
20) Southern_Hemisphere_Percent_Cloudiness_vs_Latitude.png
21) Northern_Hemisphere_Wind-Speed_vs_Latitude.pdf
22) Northern_Hemisphere_Wind-Speed_vs_Latitude.png
23) Southern_Hemisphere_Wind-Speed_vs_Latitude.pdf
24) Southern_Hemisphere_Wind-Speed_vs_Latitude.png
#### WeatherPy/output_data/Practice contains practice CSVs and PNGs and historical IPYNB (prior to cleaning)


### Solutions for VacationPy
