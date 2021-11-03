## Why?

Typically, data is extracted from databases for analysis. But in a server-less architecture, a database server is not required for analysis. CSV files of the spatial data of fishing entities can be directly stored on S3 to be accessed in the notebooks. Moreover, the shape files of cells and other geographical regions such as large marine areas can also be stored on S3. This shape files data can be then accessed directly in Jupyter notebooks for creating interactive maps. This allows us to extract the necessary data, and conduct data analysis or create visualizations, and also create maps – everything from within a Jupyter Notebook.

In the case of SAU, a subset of the whole PostgreSQL database can be stored in S3 for this geospatial data analysis and mapping purposes. This subset of data includes identifiers for cell, eez, lme as well as catch sum and real value metrics by year for attributes such as sector type, catch type, gear type, and taxon.



## How?

### Using S3 data directly in notebooks

If the data is in the form of a CSV file in S3, then this data can be directly accessed in notebooks via CloudFront and by using `pandas` library in Python. In a similar way, shape files for cells and marine areas can be accessed using `geopandas` library in Python. Please refer to sample notebooks provided in this repository for further details and examples that demonstrate basic usage of this functionality.

