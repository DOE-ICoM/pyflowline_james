## PyFlowline workflow

### USGS National Hydrography Dataset river flowline processing


The raw NHD flowline dataset contains more than 10, 000 flowlines, to reduce the total number of flowline, the stream order is used to remove small rivers.

The filtered flowlines are converted to the GeoJSON format.

### Install the PyFlowline python package

Install the Pyflowline package using Conda (recommended):

        conda install -c conda-forge pyflowline

### Data preparation

1. Configure the path in the JSON files under the `example` folder.
2. Set up model parameters, e.g., mesh resolution.


### Run simulation

Run the simulations using the `run_susquehanna.py` script using your preferred Python environment.

Correct errors if there are issues in the path configuration.

### Visualization

Two types of output are available under the outpur folder
1. JSON files, contain information of mesh and flowline topological relationship;
2. GeoJSON files, contain conceptual flowlines in the `GIS` format.

