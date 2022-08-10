## How to create the MPAS mesh

### USGS National Hydrography Dataset river flowline processing

The raw NHD flowline dataset contains more than 10, 000 flowlines, to reduce the total number of flowline, the stream order is used to remove small rivers.
And a list of other algorithms from the `Pyflowline` are applied to remove both small flowlines and braided rivers. The filtered flowlines are then used by the `JIGSAW` to generate the mesh. 


### Jigsaw- MPASmesh generation

`JIGSAW` is used to generate the MPAS. For details on how to use this tool, see [JIGSAW](https://github.com/dengwirda/jigsaw-geo-python)



