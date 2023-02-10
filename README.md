# Intra_biome_variation_method 

***Important note:***

## Code for "*A new method based on surface-sample pollen data for reconstructing palaeovegetation patterns"*

#### **Authors**: Esmeralda Cruz-Silva, Sandy P. Harrison, Elena Marinova, I. Colin Prentice

#### Paper available at: https://onlinelibrary.wiley.com/doi/10.1111/jbi.14448 

### Abstract

**Aim**: Biomisation has been the most widely used technique to reconstruct past regional vegetation patterns because it does not require an extensive modern pollen dataset. However, it has well-known limitations including its dependence on expert judgement for the assignment of pollen taxa to plant functional types (PFTs) and PFTs to biomes. Here we present a new method that combines the strengths of biomisation with those of the alternative dissimilarity-based techniques.
 
**Location**: The Eastern Mediterranean-Black Sea Caspian Corridor (EMBSeCBIO) region, 28°-49°N, 20°-62°E.

**Methods**:  Modern pollen samples, assigned to biomes based on potential natural vegetation data, are used to characterize the within-biome means and standard deviations of the abundances of each taxon. These values are used to calculate a dissimilarity index between any pollen sample and every biome, and thus assign the sample to the most likely biome. We calculate a threshold value for each modern biome; fossil samples with scores below the threshold for all modern biomes are thus identified as non-analogue vegetation. We applied the new method to the EMBSeCBIO region to compare its performance with existing reconstructions.

**Results**: The method captured changes in the importance of individual taxa along environmental gradients. The balanced accuracy obtained for the EMBSeCBIO region using the new method was better than obtained using biomisation (77% vs. 65%). When the method was applied to high-resolution fossil records, 70% of the entities showed more temporally stable biome assignments than obtained using biomisation. The technique also identified likely non-analogue assemblages in a synthetic modern dataset and in fossil records.

**Main conclusions**: The new method yields more accurate and stable reconstructions of vegetation than biomisation. It requires an extensive modern pollen dataset, but is conceptually simple, and avoids subjective choices about taxon allocations to PFTs and PFTs to biomes.

### Data availability

The **SMPDS** data is available through the University of Reading Data archive at: https://researchdata.reading.ac.uk/194/

The **EMBSeCBIO** pollen data base is available through the University of Reading Data archive at: https://researchdata.reading.ac.uk/309/

The **Pontential Natural vegetation map** NetCDF file included in "Data" file of this repository. Originally obtained from https://zenodo.org/record/3631254#.YPbrpOhKibg

### Analyses
**Extract_PNV_observed_biome**

The observed biome in the PNV map for each pollen sample in the modern training data set, was derived using a search window of 20x20 km around the location of the sample point. It was used the Global map of potential natural vegetation (Hengl et al., 2018) in its updated version of spatial resolution of 250m, at a resolution of 1km. We determined both the dominant and subdominant biome in each search window for subsequent evaluation based on which biomes occupied the largest and second-largest number of 1 km2 pixels within the search window. 

**Modern_vegetation_reconstruction (Tables 2 to 4)**

Modern pollen samples assigned to biomes based on potential natural vegetation data are used to characterize biomes according to the within-biome means and standard deviations of the abundances of each taxon. These are used to calculate a dissimilarity index between any given pollen sample and every biome, and thus assign a pollen sample to the most likely biome. We have applied the new technique to the EMBSeCBIO region in order to compare the performance of the new method with existing reconstructions. The biome reconstructions were evaluated quantitatively using a matrix of predicted versus observed vegetation at each site. We constructed confusion matrices for the evaluation on the test dataset and on the EMBSeCBIO dataset, based on both the dominant and subdominant biome registered in the search window around the sample. 

**Biomes_boxplots (figure 3 and Supplementary figure )**

The training samples were grouped according to the dominant biome observed in the PNV map. Each modern biome was then characterised by the relative abundance (expressed in terms of the mean, range, and standard deviation) of all taxa present to account for variability in pollen abundances within each biome. 
Boxes show the median and standard deviation of the abundance of individual taxa.

**Modern_point_maps (Figure 4)**

The reconstructed modern biome distribution for the EMBSeCBIO region was mapped.

**Cutpoints_optimal_ROC_identification (Figure 5 and Table 6)**
We used the similarity scores obtained from the modern pollen samples in the modern testing dataset (without downsampling) for each biome (Supplementary figure 3) and made pair-wise comparisons between biomes. We obtained the optimal threshold value that differentiated each pair of biomes by calculating specificity and sensitivity metrics (Supplementary figure 4) and plotting these on a receiver operating characteristic (ROC) curve, where the point with the maximum balance (sensitivity + specificity) was selected as the optimal threshold between the two biomes. 



 
## References

Harrison, S. P., Marinova, E., & Cruz-Silva, E. (2021). EMBSeCBIO pollen database [Data set]. University of Reading. https://doi.org/10.17864/1947.309

Hengl, T., Walsh, M. G., Sanderman, J., Wheeler, I., Harrison, S. P., & Prentice, I. C. (2018). Global mapping of potential natural vegetation: An assessment of machine learning algorithms for estimating land potential. PeerJ, 6, e5457. https://doi.org/10.7717/peerj.5457

Villegas-Diaz, R., Cruz-Silva, E., & Harrison, S. P. (2021). ageR: Supervised Age Models [R]. Zenodo. https://doi.org/10.5281/zenodo.4636716
