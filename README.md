# Wildlife Pitch Monitoring System


## Abstract

Lions (*Panthera leo*) are among the most iconic and ecologically significant predators in the world. As apex predators, they play a crucial role in maintaining the balance of ecosystems across the African continent. Despite their ecological importance, lion populations have experienced a significant decline over recent decades due to habitat fragmentation, human encroachment, and increasing environmental pressures.

Rapid urbanization, agricultural expansion, and infrastructure development have divided once-continuous habitats into isolated patches, restricting natural movement and reducing genetic exchange between populations. This fragmentation not only increases the risk of local extinction but also intensifies human-wildlife conflict as lions are forced into closer proximity with human settlements. Illegal poaching and retaliatory killings further threaten their long-term survival.

To address these challenges, this project explores the use of GIS-based spatial analysis, grid-based clustering, and Maximum Entropy (MaxEnt) species distribution modeling to identify habitat suitability patterns and potential ecological corridors for African lions. By understanding where suitable habitats exist and how fragmented populations can remain connected, the study aims to provide insights that support wildlife conservation and landscape connectivity planning.

## Project Objective

The primary objective of this study is to identify potential ecological corridors and suitable habitats for African lions using species distribution modeling and geospatial analysis. By combining lion occurrence records with environmental variables, the project aims to predict habitat suitability, reduce the effects of habitat fragmentation, and support conservation planning efforts. The study further explores the use of grid-based clustering to improve data quality and enhance the reliability of habitat suitability predictions.

## Study Area

This study focuses exclusively on African lions (*Panthera leo*) and their habitat distribution across the African continent. The objective is to identify environmentally suitable habitats and potential ecological corridors that can facilitate safe movement between fragmented lion populations. Understanding these movement pathways is critical for reducing habitat isolation and supporting long-term conservation efforts.

## Dataset Description

The study utilizes a dataset containing **6,638 recorded African lion observations**, stored in `Sample.csv`. Each observation captures both temporal and geographic information, enabling the analysis of lion movement patterns and habitat distribution.

Key attributes available in the dataset include:

- Event date and time information
- Day-of-year indicators
- Year, month, and day fields
- Continental location information
- Geographic coordinates (`decimalLatitude`, `decimalLongitude`)

For this research, the geographic coordinates were the most critical variables, as they provided the spatial foundation required for clustering, habitat suitability analysis, and ecological corridor identification.

## Methodology
