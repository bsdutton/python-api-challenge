# python-api challenge

# FIRST PART - WeatherPy
  * Working file was WeatherPy-working.ipynb

## All generated output files were from WeatherPy-working.ipynb

## ANALYSIS for WeatherPy
1) The temperature range from colder towards the North and South Poles to hotter near the Equator makes sense in this scatter plot between Max Temperature versus Latitude.
2) The correlations you would expect to see in the separate plots of temperature versus latitude for Northern Hemisphere and Southern hemisphere are evident on the overall plot.  The correlations show they converge at the Equator. 
3) There are no correlations that can be derived for percent humidity versus latitude, percent cloudiness versus latitude, and wind speed versus latitude.
4) The latitudes nearest the Equator remain constantly warm all year round.  The scatter plots show strong correlations that support this.
5) The strong negative correlation shown with linear regression between max temperature and latitude for the Northern latitudes appears it would intersect with the strong positive correlation shown in the linear regression for the Southern latitudes.  The intersection does not appear to be at the Equator, but it appears to be dloser to the 20 degree North latitude mark.  This seems like it could be a reflection of Summer in the North latitudes.  An interesting analysis would be to see if this perceived intersection shifts near 20 degrees South latitude during Winter.  This would mirror the tilt of the Earth's axis throughout the year.
6)  The lack of correlation shown with humidity, cloudiness, and wind speed versus latitude is because these variables are fluid and dependent on the movement of the atmosphere.  Yes, there is an air temperatue component which is fluid, but temperature of the earth and oceans due to the warming of the sun on a daily and seasonal basis contribute more of a static component to the overall temperature measurement, and this is why you seen strong correlations between temperature and latitude. 

## NOTES for WeatherPy
1) I initially used list comprehension  with a for-loop in order to retrieve data for each of the randomly selected cities.
  * I did not get any exception responses.
  * This list comprehension for-loop worked every time.  I consitently checked the length to compare with the cities list.
  * The cities list used for all the outputs for WeatherPy had 616 cities.
  * I only noticed exceptions when I tried to do try-except by printing out the first and last responses.
  * I got a 404 on the last response the first time I ran the try-except.
2) However, the list comprehension for-loop did not make sense when I wanted to append data to the separate lists.
3) I started to use a for-loop which include my response.get and append list statements.
4) I had to do the most work getting the try-except to work.
  * I added print statements at the end of the for-loop.
  * One print statement was to show the request sent.
  * Second print statement was to show the response received.
  * I used these as my print log.
  * These allowed me to see the 404 responses which made the for-loop with try-except fail.
  * I had a third print statement for the exception.
5) I found I was making the mistake of keeping the response.get statement right after the for-loop which made it outside the try-except.
6) Moving the response.get as first line after try made everything start to work.
7) I used the example of the url_query to send all of my print results to lists which I moved into DataFrames and output as CSVs.
  * These are meant to be my print logs even though the print results are output in the notebook.
  * The cities list contained 616 cities.  The request_response_log.csv contains 576 cities.  The response_error_log.csv contains 40 cities.
8) For the step to inspect data and remove cities where humidity > 100%.
  * In the randomly generated cities list, I had no cities with humidity > 100%.
  * If the entire Jupyter Notebook is run again, the results maybe different.
  * Preserving the cities list by commenting out the random selection statements allows this notebook to be run again with the same results.
9) For the pair of scatter plots analyzing the same data for Northern Hemisphere and Southern Hemishere.
  * I arranged these scatter plots so I performed all the Northern Hemisphere scatter plots with linear regressions at one time since the DataFrame .loc > 0 had to be run first. 
  * I had to keep alternating and running the .loc DataFrames over and over again to get the correct number of datapoints for each hemisphere.
  * By reordering so all scatter plots and linear regressions for each hemisphere were grouped together, I only had to run the .loc DataFrame once for each hemisphere.
  * This made iterations for the best results much faster.
10) I added module country_converter to change the ISO 2 letter country code to a short name for the country.
11) I initially made all my plots with Latitude for the x_values, but I found when I switched Latitude to y_values it was easier to make some sense between it and the other variable it was being measured against.
  * I saved all my original plots with Latitude as x_values in tje output_data/practice folder.

  ## NOTES for VacationPy
  1) I used WeatherPy-main.ipynb as my starter Notebook.
  2) All solutions and outputs are taken from VacationPy-working.ipynb.
  3) All CSVs and PNGs are saved in VacationPy/vacation_output_data folder.
  4) VacationPy-main.ipynb is a cleaned Notebook without all the extra codeblocks used to resolve the code.
  5) If VacationPy-main.ipynb is run, a new city list will be created.
    * All CSVs and PNGs as output are saved in VacationPy/fresh_vacation_output_data folder.
  6) I toggled the toolbar on and off so the heatmaps could be downloaded as PNG.
  7) I could not get the codeblock with the API requests for nearbysearch to work yet.  I still have to fix it.
  8) But I got the second heatmap with clickable markers.  Hover_text works, too; but only the city name is shown so far.
  9) I set the center coordinates and zoom level for the heatmaps to make them show up the same every time.