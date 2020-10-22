# Toronto Bike Station
* Overview
* Repo content
* Setup

## Overview:
Storing information about Toronto bike stations from data acquired from Bike Share Toronto data.
The data endpoints are:
* https://tor.publicbikesystem.net/ube/gbfs/v1/en/station_information
* https://tor.publicbikesystem.net/ube/gbfs/v1/en/station_status

The purpose is to acquire the data and load it after merging it to answer the following questions:
* How many bike stations are available in the city?
* What is the average bike availability?
* What are the 3 largest bike stations in the city?
* What are the 3 smallest bike stations in the city?

As well as finding the closest stations given a some coordinates.

## Repo content:
* etl_code.ipynb: The implementation in a jupyter notebook.
* etl_code.html: HTML version of the notebook
* data: has the input and output data directories.
  * input: The payload from the 2 endpoints saved as json file.
  * output: The merged information in an sqlite format.
* requirements.txt: Python requirements file.

## Setup:
* Clone the repo locally, then make a python virtual environment using `$python3 -m venv <venv_name>`
lets assume the venv_name is ocean_venv moving forward.
* Activate the venv by `$source ocean_venv/bin/activate`
* Install the python requirements `$pip install requirements.txt`
* To run the jupyter notebook: `$jupyter notebook`

**NOTE**: Running certain cells will overwrite the data inputs and outputs.
