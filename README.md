# Risky-Move
An app to understand the movement of animals around linear infrastructures such as roads, and rails which hinders smooth movement and puts animals in vulnerable situations, which have led to unfortunate deaths and collisions.  

GitHub repository: *https://github.com/Pkishore92/Risky-Move*

## Description
*An app to understand and visualize the movement of animals around linear infrastructures such as roads, railways etc, where the movement is hindered by fragmentation of foraging habitats and refuge. The app displays outputs such as displacements, distance travelled, intersection points with linear infra, and distance/proximity to the nearest linear infra and highlights such critical points of crossing.*

## Documentation
*Risky Move is an app to understand the movement of animals around linear infrastructures. The structure of the code is such that, a preliminary understanding of displacement, time intervals, cumulative distance travelled, and movement/dormant status of the animal through the threshold is computed. This is followed by extraction of OSM data by querying using a bounding box and based on the interest, railways or highways or both are filtered from the osm data. These sf objects are then matched with a CRS which will provide us with intersection points, and min-max distances to the linear infrastructure. A static and interactive plot is then generated to visualize the extracted data. To make this interactive, a shiny app is created to observe the paths and intersections which provides us insights into critical paths taken by animals to cross for foraging and refuge movement.*

### Input data
*MoveStack in Movebank format*

### Output data
*Tables, static map plots, interactive map plots, shiny visualization app*

### Artefacts
*’extracted_data.csv’: CSV file containing all the variables computed, ‘static_map.png’: a map displaying intersection and plots of all the locations*

### Settings
`Store settings`: click to store the current settings of the app for future workflow runs

### Most common errors
*’ shiny visualization force closes’, ‘tabulation object error in shiny’*

### Null or error handling
*shiny visualization force closes: When the shiny app is running, the window force closes if there are any naming errors which call variables from the data frame, so keep a check on the variable names. tabulation object error in shiny: overlaying of objects on the map has a reactive error in shiny which interrupts the table formation, so prevent overlaying and reading data*
