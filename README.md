# Intra_biome_variation_method 

## Code for "*A new method based on surface-sample pollen data for reconstructing palaeovegetation patterns"*

#### **Authors**: Esmeralda Cruz-Silva, Sandy P. Harrison, Elena Marinova, I. Colin Prentice

#### Paper available at:

### Abstract

**Aim**: 
 
**Location**: The Eastern Mediterranean-Black Sea Caspian Corridor (EMBSeCBIO) region, 28°-49°N, 20°-62°E.

**Methods**:  

**Results**: 

**Main conclusions**: 

### About this repository

This contains codes to perform the modern vegetation reconstructions presented in the paper.

### Data availability

The **SMPDS** data is available through the University of Reading Data archive at: https://researchdata.reading.ac.uk/194/

The **EMBSeCBIO** pollen data base is available through the University of Reading Data archive at: https://researchdata.reading.ac.uk/309/

The **Pontential Natural vegetation map** NetCDF file included in "Data" file of this repository. Originally obtained from https://zenodo.org/record/3631254#.YPbrpOhKibg

## Analysis
### Extract_PNV_observed_biome
The observed biome in the PNV map for each pollen sample in the modern training data set, was derived using a search window of 20x20 km around the location of the sample point. It was used the Global map of potential natural vegetation (Hengl et al., 2018) in its updated version of spatial resolution of 250m, at a resolution of 1km. We determined both the dominant and subdominant biome in each search window for subsequent evaluation based on which biomes occupied the largest and second-largest number of 1 km2 pixels within the search window. 
### Biomes_boxplots (to generate figure 3)
The training samples were grouped according to the dominant biome observed in the PNV map. Each modern biome was then characterised by the relative abundance (expressed in terms of the mean, range, and standard deviation) of all taxa present to account for variability in pollen abundances within each biome. 
Boxes show the median and standard deviation of the abundance of individual taxa.
### Modern_vegetation_reconstruction (to generate figure 4)
The reconstructed modern biome distribution was mapped, where each point represents the location of a pollen sample, the colour indicates the reconstructed biome, and the size of the point shows the similarity value.
### Past_vegetation_reconstruction (to generate figures 5 and 6)
We calculated the similarity scores between each fossil pollen sample and the target biomes. For mapping purposes, every sample was allocated to the biome with the largest similarity score. We then plotted the typical biome within a 300-year time window, which is close to the average resolution of the fossil pollen records (328 years).  To visualize the changes through time, we produced down-core plots showing the proportion of the similarity score assigned to each sample. 
## References

Harrison, S. P., Marinova, E., & Cruz-Silva, E. (2021). EMBSeCBIO pollen database [Data set]. University of Reading. https://doi.org/10.17864/1947.309

Hengl, T., Walsh, M. G., Sanderman, J., Wheeler, I., Harrison, S. P., & Prentice, I. C. (2018). Global mapping of potential natural vegetation: An assessment of machine learning algorithms for estimating land potential. PeerJ, 6, e5457. https://doi.org/10.7717/peerj.5457

Villegas-Diaz, R., Cruz-Silva, E., & Harrison, S. P. (2021). ageR: Supervised Age Models [R]. Zenodo. https://doi.org/10.5281/zenodo.4636716
