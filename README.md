# NYC 311 Analysis

## Download data

After git cloning the repository, download the NYC 311 request data:

```shell
$ mkdir data/
$ curl https://data.cityofnewyork.us/api/views/erm2-nwe9/rows.csv?accessType=DOWNLOAD \
--output 311_Service_Requests_from_2010_to_Present.csv
```

## Installation

Create a conda environment and install dependencies:
```shell
conda env create -f environment.yml
conda activate nyc311
```

## Data cleaning

The data preparation process is explained in `data_cleaning.ipynb`. It exports a clean dataset `nyc311_clean.csv` in the data folder.

## Data analysis

`analysis.ipynb` walks through the analysis to answer three questions:

1. What are the number of complaints per agency for each zip code?
2. For each zip code, find which other zip code they are most and least similar to
3. What are the anomalous zip codes for each agency?

The results are saved in the results folder.