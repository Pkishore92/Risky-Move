Risky-Move

MoveApps

Github repository: *https://github.com/Pkishore92/Risky-Move*

## Description
*An app to understand and visualize the movement of animals around linear infrastructures such as roads, railways etc, where the movement is hindered by fragmentation of foraging habitats and refuge. The app displays outputs such as displacements, distance traveled, intersection points with linear infra, distance/proximity to the nearest linear infra and highlights such critical points of crossing.*

## Documentation
*Risky Move is an app to understand the movement of animals around linear infrastructures. The structure of the code is such that, preliminary understanding of displacement, time intervals, cumulative distance travelled, movement/dormant status of animal through threshold are computed. This is followed by extraction of OSM data by querying using bounding box and the based on the interest, railways or highways or both are filtered from the osm data. These sf objects are then matched with a CRS which will provide us with intersection points, min-max distances to the linear infrastructure. A static and interactive plot is then generated to visualize the extracted data. To make this interactive, a shiny app is created to observe the paths and intersection which provides us insights of critical paths taken by animals to cross for foraging and refuge movement.*

### Input data
*MoveStack in Movebank format*

*Example*: MoveStack in Movebank format

### Output data
*Tables, static map plots, interactive map plot, shiny visualization app*

*Example:* MoveStack in Movebank format

### Artefacts
*’extracted_data.csv’ : csv-file containing all the variables computed, ‘static_map.png’ : a map displaying intersection and plots of all the locations*

*Example:* `rest_overview.csv`: csv-file with Table of all rest site properties

### Settings
*Since our switch to use shiny bookmarks for storing seleted settings made in the UI, it is not possible any more to have settings in MoveApps to set before running the App and opening the UI. Instead a `store settings` button is included in the UI.

`Store settings`: click to store the current settings of the app for future workflow runs

### Most common errors
*’shiny visualization force closes’, ‘tabulation object error in shiny’*


### Null or error handling
*shiny visualization force closes: When shinyApp is running, the window force closes if there are any naming errors which calling variables from the dataframe, so keep a check on the variable names.tabulation object error in shiny: overlaying sf objects on the map has reactive error in shiny which interrupts the table formation, so prevent overlaying and reading data*

*Please indicate for each setting as well as the input data which behaviour the App is supposed to show in case of errors or NULL values/input. Please also add notes of possible errors that can happen if UI settings/parameters are improperly set and any other important information that you find the user should be aware of.*

*Example:* **Setting `input$radius`:** If no radius AND no duration are given, the input data set is returned with a warning. If no radius is given (NULL), but a duration is defined then a default radius of 1000m = 1km is set. 
