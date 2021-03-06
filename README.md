# Mapping and Predicting the Intra-urban Degrees of Deprivation Using EO Data

**Keyword: Deprivation, Slums, Earth Observation, Deep Learning**  

## Background 
The rapid proliferation of slums is a major challenge in urbanization. Most of the growing urban population in Low- to Middle-Income Countries (LMICs) is absorbed by slums, informal settlements, and deprived areas. In the last decades, slums have been successfully detected and mapped, given the increasing availability of very-high-resolution (VHR) satellite image and the development of machine learning (ML) techniques. Yet, most approaches only yield a binary delineation of slum/non-slum – an oversimplified understanding of urban deprivation that mostly built upon their morphological features, e.g., spatial configurations, locations, and extents. This binary delineation also resulted in high uncertainties on where to draw the boundary between slum and non-slum areas. Recently, more approaches were introduced to investigate slums via the lens of ‘Multiple Deprivation’, as it enables to capture it as a multi-dimensional manifestation. Results not only capture the traditional aspects such as housing conditions, physical morphologies but also the socio-economic status, environmental, and other factors of deprivation. However, as most studies are still restricted to a categorical description of multi-deprivation, we thus argue the need to map multi-deprivation in continuous indices to better unveil its diversity and complexity. In this research, we aim to capture intra-urban deprivation's diversity by predicting the deprivation degrees at a continuous variable from VHR images, using Nairobi as a pilot city. 

## Methodology
This research develops an integrated two-stepwise methodology that comprised of two key technical parts: unsupervised learning and deep learning. Based on the literature review and the local context of Nairobi, the term ‘multiple deprivations’ is conceptualized, followed by the development of quantitative indicators covering sub-domains of deprivation. All input data are then transformed and resampled into 100*100m grided raster layers for this intra-city level study. In the unsupervised learning process, principal component analysis (PCA) is applied on the deprivation indicators to generate data-driven multiple deprivation indices (MDI); next, the results from PCA are iteratively refined by inspecting the PCA-model statistic metrics and validated/cross-discussed with previous studies and local knowledge. Then, the final data-driven MDI is used as reference labels for the next deep learning step. 

Continuing with the deep learning process (currently going on), a Convolution neural network(CNN)-based regression model is trained to predict the continuous deprivation index (0 to 1) from VHR satellite image. The inputs of the CNN model are: 
1) the  SPOT satellite image of Nairobi city, 2017. Resolution = 1.5m, with four bands (RGB + near-infrared); 
2) the deprivation indices of urban built-up Nairobi at 100m grid scale, generated from previous unsupervised learning steps. 

The CNN model will be applied to the whole urban area of Nairobi to predict the intra-urban degrees of deprivation. Finally, the gridded outputs allow capturing the diversity and variety of deprivation.  

## Summary
In general, by training this model, the usefulness of using RS-oriented features to predict deprivation degrees is examined, with a continuous data-driven multiple-deprivation index expected, thus increasing our present knowledge on how multi-dimensionality and variety of deprivation could be extracted from physical characteristics in the imagery data.

## Quick guide
- The folder named **'PCA_process'** contains the souce code of pre-processing steps of PCA input, and the rasterization of PCA-based indices. The PCA analysis, however, was conducted in SPSS. 
- The **'CNN-based_regression_model'** contians the source code of a VGG-like regression model, predicting the degrees of deprivation. 


