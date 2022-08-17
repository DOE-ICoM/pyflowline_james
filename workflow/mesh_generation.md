## Mesh generation

### Overview

Our method is mesh independent, so theoratically you can use any meshes. However, we require the mesh data must meet the following format:

|  | Requirements | Note |
|-------|---------|-----------------|
| Format | GeoJSON |  |
| Spatial reference | Geographic coordinate system (GCS) WGS84 |  |
| Field | ID |  |


### Structured meshes

`PyFlowline` provides built-in algorithm for several structured meshes:


| Mesh | Description | Note |
|-------|---------|-----------------|
| Hexagon | A projection based hexagon mesh |  |
| Latlon | A longitude/latitude mesh |  |
| Square | A projection based rectangle mesh |  |

Because PyFlowline requires mesh data must be GCS system, the generated meshes are automatically converted to the GCS spatial reference.


### JIGSAW MPAS workflow

#### Overview

The mesh generation process is supported by the JIGSAW and MPAS tools.

In order to `burn` the river networks into the mesh so mesh cell aligh with the actual river flowlines, a vector-based flowline GIS dataset is required.
This dataset was produced from the NHD dataset, and it was simplified using the PyFlowline to remove small rivers and braided rivers.

The coastal line is also used in the mesh refinement.

The final MPAS mesh resolution varies between 3 and 10 km with high resolution near the coastal line and river networks.

#### USGS National Hydrography Dataset river flowline processing

The raw NHD flowline dataset contains more than 10, 000 flowlines, and cannot be directly used by JIGSAW for mesh generation, which requires the `distance` between flowline to be less than the desired mesh resolution.

First, we use the stream order to remove small rivers.
Second, even with the reduced flowlines, there are still many small rivers and braided rivers. 

Currently, the `MOSART` model and our numerical model design do not support multiple flow directions caused by braided rivers. 
Therefore, a list of algorithms from the `Pyflowline` are applied to remove both small flowlines and braided rivers. 

The filtered flowlines are then used by the `JIGSAW` to generate the mesh. 


#### JIGSAW MPAS mesh generation

`JIGSAW` is used to generate the MPAS mesh. For details on how to use this tool, see [JIGSAW](https://github.com/dengwirda/jigsaw-geo-python).



