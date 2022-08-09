

# Liao. et al

**Evaluation of river routing on a unstructured grid for coupled earth system modeling**

Chang Liao<sup>1\*</sup>, 
Donghui Xu<sup>1</sup>,
Tian Zhou<sup>1</sup>,
Matt Cooper<sup>1</sup>,
Darren Engwirda<sup>2</sup>, 
Hong-Yi Li<sup>3</sup>,
and L. Ruby Leung<sup>1</sup>

<sup>1 </sup> Atmospheric Sciences and Global Change, Pacific Northwest National Laboratory, Richland, WA, USA

<sup>2 </sup> T-3 Fluid Dynamics and Solid Mechanics Group, Los Alamos National Laboratory, Los Alamos, NM, USA

<sup>3 </sup> University of Houston, Houston, TX, USA

\* corresponding author:  chang.liao@pnnl.gov
## Abstract

River networks are important features in surface hydrology. However, accurately representing river networks in spatially distributed hydrologic and Earth system models is often sensitive to the model's spatial resolution. Specifically, river networks are often misrepresented because of the mismatch between the model's spatial resolution and river networks details, resulting in significant uncertainty in projected flow direction. In this study, we developed a topological relationships-based river network representation method for spatially distributed hydrologic models. This novel method uses (1) graph theory algorithms to simplify real-world vector-based river networks and assist in mesh generation; and (2) a topological relationship-based method to reconstruct conceptual river networks. The main advantages of our method are that (1) it combines the strengths of vector-based and DEM raster-based river network extraction methods; and (2) it is mesh-independent and can be applied to both structured and unstructured meshes. This method paves a path for advanced terrain analysis and hydrologic modeling across different scales. 

## Journal reference

Liao. et al. (2022). Topological relationships-based flow direction modeling part 1 river networks representation

## Code reference

References for each minted software release for all code involved.  

Liao, Chang, & Cooper, Matt. (2022). Pyflowline: a mesh-independent river networks generator for hydrologic models (0.1.22). Zenodo. https://doi.org/10.5281/zenodo.6604337



## Data reference

### Input data
Reference for each minted data source for your input data.  For example:



### Output data
Reference for each minted data source for your output data.  For example:



## Contributing modeling software

| Model | Version | Repository Link | DOI |
|-------|---------|-----------------|-----|
| PyFlowline | version | https://doi.org/10.5281/zenodo.6604337 | link to DOI dataset |



## Reproduce my experiment

You need to follow three major steps to reproduce this study: 

1. Run the [MPAS tool](https://github.com/DOE-ICoM/mpas_mosart/blob/main/workflow/jigsaw_mpas.md)
2. Run the [PyFlowline tool](https://github.com/DOE-ICoM/mpas_mosart/blob/main/workflow/hexwatershed.md)


## Reproduce my figures

Use the scripts found in the `figures` directory to reproduce the figures used in this publication.

