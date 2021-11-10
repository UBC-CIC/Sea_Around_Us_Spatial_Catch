## Why?

Geospatial data manipulation is an important part in the analysis of data containing geographic information. Regular data wrangling libraries such as `pandas` cannot be directly used for this purpose. Users need the ability to perform spatial operations on the data and the python library called `geopandas` helps users in this regard. However, installation of this powerful library can be tricky. To avoid conflicts in the python environment when a direct `pip install` or a `conda install` method is used, it is recommended to install dependencies of `geopandas` in a manual fashion using wheel files.

## How?

__Installation instructions for GeoPandas__

Wheel files contain pre-compiled extensions, and can be very helpful in avoiding compilation failures. Christoph Gohlke at UC Irvine maintains a [large library](http://www.lfd.uci.edu/~gohlke/pythonlibs/) of Python wheels for Windows.

There are five wheel files that are necessary for correct installation of `geopandas` -  GDAL, Fiona, pyproj, rtree, and shapely. Briefly, the installation process looks like this - first get the wheel files of above five packages, then pip install those wheels in the same order, and then `geopandas` can be directly installed using `pip install geopandas`. Please note your python version and whether your architecture is 32 or 64 bit to download the correct version of wheels from the website. Following resources and blog posts have detailed instructions of this process and can be useful as a reference.

> https://geoffboeing.com/2014/09/using-geopandas-windows/
>
> https://towardsdatascience.com/geopandas-installation-the-easy-way-for-windows-31a666b3610f
>
> https://www.linkedin.com/pulse/installing-geopandas-manually-windows-alaa-hassan
>
> https://hatarilabs.com/ih-en/how-to-install-python-geopandas-on-anaconda-in-windows-tutorial

After the installation process is complete, try importing the libraries to verify the installation. A Jupyter notebook to test  `geopandas` is also provided in the `notebooks` section of this repository.



