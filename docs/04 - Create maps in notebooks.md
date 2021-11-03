## Why?

Data analysis of geospatial data cannot be conducted effectively in a typical approach using tables and visualizations. Often the patterns are not directly visible in the data, especially when there are several geographic regions. Maps are a key tool in analyzing geospatial data effectively, and insights based on patterns in geographical regions can often be easily drawn from heatmaps and choropleth maps.

## How?

__Working with shape files__

The goal of `GeoPandas` is to make working with geospatial data in python easier. `GeoPandas` extends the datatypes used by `pandas` to allow spatial operations on geometric types. Geometric operations are performed by `shapely`. `Geopandas` combines the capabilities of `pandas` and `shapely`, providing geospatial operations in `pandas` and a high-level interface to multiple geometries to `shapely`. `GeoPandas` enables you to easily do operations in python that would otherwise require a spatial database such as PostGIS.

Refer to official documentation at `https://geopandas.org/docs.html` for user guide and hands-on examples. `Reading and Writing Files` section in these docs has more details on accessing all the shape files together as a single zip file, for example. 

__Working with maps__

`Folium` is python library built on top of `leaflet.js` that makes it easy to convert data from (Geo)DataFrames into interactive Leaflet maps. It enables both the binding of data to a map for choropleth visualizations as well as passing rich vector/raster/HTML visualizations as markers on the map. 

`Folium` builds on the data wrangling strengths of the Python ecosystem and the mapping strengths of the `leaflet.js` library. Refer to the official documentation at `https://python-visualization.github.io/folium/`, especially the `Quickstart` section that contains hands-on examples.



>  Please refer to `notebooks` section in this repository for examples illustrating usage of `geopandas` and `folium` libraries in Jupyter notebooks.



