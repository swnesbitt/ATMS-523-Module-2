# M2Assignment: Xarray, Dask, and Cloud Computing

This repository contains the code and data for the Module 2 assignment. The notebook, `M2Assignment.ipynb`, explores the use of **Xarray** and **Dask** for analyzing large climate datasets.

## Project Description

The primary goal of this project is to analyze daily precipitation data (`tp`) from the **ERA5-Land** reanalysis dataset, using efficient, memory-friendly methods suitable for large-scale data. The notebook performs the following key tasks:

1.  **Data Ingestion**: Opens and combines multiple NetCDF files into a single, lazy-loaded dataset using `xarray.open_mfdataset` and **Dask**. This approach allows for processing data that is larger than the available RAM.
2.  **Statistical Analysis**: Calculates the **95th percentile** of daily precipitation to identify extreme weather events. A **Cumulative Distribution Function (CDF)** plot is generated to visualize this percentile.
3.  **Geospatial Analysis**: Creates two different maps to visualize precipitation patterns over the continental USA using **Cartopy**:
    * **Composite Mean Map**: Shows the average precipitation on days that exceed the 95th percentile.
    * **Anomaly Map**: Displays the precipitation anomaly relative to the 1981–2010 climatological mean.

## Data

The data used in this project is from the **ERA5-Land** reanalysis, specifically the daily total precipitation (`tp`) variable.

**Data Source:** Copernicus Climate Change Service (C3S)
**License:** Creative Commons Attribution 4.0 International License (CC BY 4.0)

Due to file size constraints, the raw data files are **not included** in this repository.

## Installation and Usage

To run this notebook, you need a Python environment with the following libraries:

* `xarray`
* `dask`
* `numpy`
* `matplotlib`
* `cartopy`
* `h5netcdf`

You can install these dependencies using `pip`:

```bash
pip install xarray dask numpy matplotlib cartopy h5netcdf