## Why?

Even though Jupyter Notebooks offer flexibility to conduct data analysis and create visualizations/maps within the notebook itself, the data behind the scenes might be needed in some cases. Once the initial data analysis is completed (or) visualizations/maps are created in a Jupyter notebook, users might want to download the data behind those tables, charts and maps for future reference (or) for further exploration and analysis.       



## How?

There are several ways to download data from a Jupyter notebook. Easiest way for notebook users to export the `pandas` data frame to csv using `to_csv` function like `df.to_csv('file1.csv')`. But if the notebook is not being run on user’s local python environment – then it might add some complexity around fetching files from the server where the notebook would save the CSV file.      

Another approach is to leverage Java Script to run the download application on client side. This approach allows the user to fetch the data similar to download files from a website. Please refer to examples in `notebooks` section of SAU phase 1 repository for more details about this download data functionality. Data behind the data frames and also the visualizations can be downloaded by the user as demonstrated in the notebooks.

Maps can be downloaded as `html` files that can be easily shared as needed. Once a Folium map is created in the Jupyter notebook, that map object can then be easily saved into the local computer using a command such as `map.save('heatmap_lme_catch_sum.html')`







