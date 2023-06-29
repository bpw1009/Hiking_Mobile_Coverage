# Hiking Mobile Coverage
Here is a quick draft of a project to look at using geospatial data processing techniques to see what the mobile coverage will be like on a hiking trip.

* I downloaded the hiking route coordinates from AllTrails using my subscription.
* I got Verizon's mobile coverage data (as of May 2015) from the FCC's website.
* I used several different python packages to process and visualize the data including the following:
  * geopandas, shapely, goepy, pandas, matplotlib, plotly, and reverse_geocoder to identify the Verizon records since the locations were not labeled.
 

In this example, I used the hiking route coordinates for Hancock Trail in the White Mountains of New Hampshire. This trail happens to be in Grafton County, NH. I reverse geocoded a point in each of the Verizon records in New Hampshire until one returned Grafton County. Each record contains Verizon mobile coverage data for one county. 

I then joined the hiking route to the coverage data and checked if each of the points on the route was in or out of coverage.

After this, I crated a variety of visualizations based on the result. I used openstreetmaps for reference points.

In this example, assuming a constant rate of hiking, a hiker would be in coverage about 76% of the trip.

A next step in this project could be to factor in changes in rate of speed based on the elevation gain or planned breaks. One function to estimate hiking speed is Tobler's Hiking Function. (https://rpubs.com/chrisbrunsdon/hiking)
