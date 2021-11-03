# Sea Around Us - Spatial Catch

## Project Overview

The [Sea Around Us](http://www.seaaroundus.org/) (SAU) is an international research initiative at the University of British Columbia that acts as a critical resource to assess the impact of fisheries on marine environments. SAU collects fisheries-related information from every maritime country since fisheries reporting started in the  1950s. The data is viewed by government subsidiaries, marine biodiversity and is available on their website. In addition to this, the SAU website also offers visualization of some geospatial data through interactive maps.

Currently, *Sea Around Us* allows mapping of catch of fishing countries and of taxon by year by half degree cells. This is accessed via the page: https://www.seaaroundus.org/data/#/spatial-catch. Users can choose only one country from the list of fishing countries. The user can slide the year bar to display the catch map for different years. In addition, users can choose to narrow down the catch map by identifying a taxon or several taxa, a commercial group, or a functional group.

*Sea Around Us* seeks to broaden the impact of this geospatial functionality by offering additional filtering capacities and analyses. Providing access to additional filters such as catch type and gear type that are not available in the visualizations on the website would be helpful to researchers. Moreover, enabling different views of data such as distribution of catch by sector type for each economic zone gives the users more flexibility in conducting meaningful analysis and research. To broaden the impact of the SAU dataset , UBC-CIC in collaboration with the SAU team will provide additional analytical tools to researchers. 

The proposed solution extends the current functionality provided on the website by offering a new way to interact with and derive insights from the SAU datasets. This is achieved by providing access to additional data filters such as catch type and gear type in the Jupyter notebooks, and also by enabling users to customize the data aggregations available for analysis. Interactive maps are included in the Jupyter notebooks – both at cell level and at exclusive economic zone (EEZ) level. While cell level data gives a granular view of the data, EEZ level data can be helpful in uncovering patterns and trends at a higher level. For example, EEZ level understanding of distribution of catch for each sector type can be very helpful for researchers, which is currently not available in the visualizations on the website. Cell level maps visualize the catch sum of all relevant half degree cells, with additional data filters available to the user. A half degree cell is equivalent to approximately 55 km x 55 km at the equator. EEZ level maps would enable users to analyze the trends and distributions for the whole zone. For example, users will be able to look at the recent 20 years trend of the catch for every EEZ related to a fishing entity. Similarly, distribution of the catch by different sector types can also be visualized within the map itself.

As this proposal involves providing access to more details and granular data compared to the website, users are able to select only one fishing entity at a time. Users can choose fishing entities from a list, and the Jupyter notebooks will only load the data related to that selection. For example, when a user selects Canada as a fishing entity – catch data for all the EEZ and half degree cells related to Canada will be available for users for further analysis and visualization. Researchers can also download these Jupyter notebooks containing maps in the form of html files that can be shared enabling easy collaboration.



## User Guides

Documentation for different steps involved in this project is added in individual user guides in the `docs` folder of this repository.

## Example Notebooks

Jupyter notebooks that demonstrate different scenarios related to data analysis, visualizations, and data access are included in the `notebooks` folder of this repository.

## Table of Contents

* __User Guides__
  * [CloudFront](https://github.com/UBC-CIC/Sea_Around_Us_Spatial_Catch/blob/main/docs/00%20-%20CloudFront_setup.md)
  * [Data Access](https://github.com/UBC-CIC/Sea_Around_Us_Spatial_Catch/blob/main/docs/01%20-%20Access%20data%20from%20S3.md)
  * [Data Analysis](https://github.com/UBC-CIC/Sea_Around_Us_Spatial_Catch/blob/main/docs/02%20-%20Data%20analysis%20in%20notebooks.md)
  * [Visualizations](https://github.com/UBC-CIC/Sea_Around_Us_Spatial_Catch/blob/main/docs/03%20-%20Create%20visualizations%20in%20notebooks.md)
  * [Create Maps](https://github.com/UBC-CIC/Sea_Around_Us_Spatial_Catch/blob/main/docs/04%20-%20Create%20maps%20in%20notebooks.md)
  * [Download maps](https://github.com/UBC-CIC/Sea_Around_Us_Spatial_Catch/blob/main/docs/05%20-%20Download%20maps%20from%20notebooks.md)
  * [SageMaker](https://github.com/UBC-CIC/Sea_Around_Us_Spatial_Catch/blob/main/docs/06%20-%20SageMaker_setup.md)
  * [Tools & Technologies](https://github.com/UBC-CIC/Sea_Around_Us_Spatial_Catch/blob/main/docs/07%20-%20Tools_and_technologies.md)
* __Example Notebooks__
  * [S3 Data Access via CloudFront](https://github.com/UBC-CIC/Sea_Around_Us_Spatial_Catch/blob/main/notebooks/01%20-%20test_cloudfront_data_access.ipynb)
  * [Interactive widgets](https://github.com/UBC-CIC/Sea_Around_Us_Spatial_Catch/blob/main/notebooks/02%20-%20test_ipywidgets_interaction.ipynb)
  * [Working with shape files](https://github.com/UBC-CIC/Sea_Around_Us_Spatial_Catch/blob/main/notebooks/03%20-%20test_geopandas_shape_files.ipynb)
  * [Working with Maps](https://github.com/UBC-CIC/Sea_Around_Us_Spatial_Catch/blob/main/notebooks/04%20-%20test_folium_maps.ipynb)
  * [Visualizations](https://github.com/UBC-CIC/Sea_Around_Us_Spatial_Catch/blob/main/notebooks/05%20-%20test_altair_visualizations.ipynb)
* __Data Dictionary__
  * [Data dictionary](https://github.com/UBC-CIC/Sea_Around_Us_Spatial_Catch/blob/main/data-dictionary/Data_dictionary.md)
  * [Appendices](https://github.com/UBC-CIC/Sea_Around_Us_Spatial_Catch/blob/main/data-dictionary/Appendices.md)

    

## Deployment Guide

The instructions provided in this repository refer to several tools and libraries for conducting data analysis and creating visualizations. This is a brief overview of the installations for these tools and libraries, please refer to official documentation for in-depth details.

**Python** : Head over to `https://www.python.org/` and navigate to specific `Downloads` section for instructions based on your operating system. Download the latest stable release of Python for your computer and operating system. Verify the successful installation by entering `python` in the command window terminal - a response from python interpreter should be received including it's version number.

**Jupyter Notebook** : The Jupyter notebook environment helps in analyzing the SAU data present in the S3 public bucket of SAU. Navigate to `Getting started with the classic Jupyter Notebook` section in the official Jupyter website `https://jupyter.org/install`. and install Jupyter Notebook as per the given instructions. If you are not already familiar with usage of Jupyter, refer to `https://jupyter.readthedocs.io/en/latest/running.html#running` for further details on how to run Jupyter Notebooks.

**Anaconda** : Instead of installing above tools individually, a popular alternative is to use open source Anaconda Individual Edition distribution that includes Python, R, necessary tools like Jupyter Notebooks, and commonly used packages such as Pandas and NumPy by default as part of it's installation. Refer to `https://www.anaconda.com/products/individual` for further details.

**Additional Packages** : Additional packages necessary for data analysis and visualizations can be installed by referring to the install instructions from official sources. For example, `pandas` library for python can be installed using either `conda install pandas` or `pip install pandas` command as mentioned in `https://pypi.org/project/pandas/`. These packages can also be installed from within the notebooks as highlighted on top in the example notebooks. 

## License

This project is distributed under [MIT License](https://github.com/UBC-CIC/Sea-Around-Us/blob/main/LICENSE).

