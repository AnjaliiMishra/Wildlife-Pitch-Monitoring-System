# Wildlife Pitch Monitoring System

*Presented at the MaxEnt 2025 Conference • University of Auckland, New Zealand*


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

The Wildlife Pitch Monitoring System follows a structured geospatial workflow to predict habitat suitability for African lions and identify potential ecological corridors. Beginning with raw occurrence records, the data undergoes preprocessing, spatial refinement, habitat suitability modeling, and conservation-oriented spatial analysis.

---

### Model Pipeline 

```mermaid
flowchart LR
    A[ African Lion Occurrence Records]
    --> B[Data Preprocessing]
    --> C[Spatial Grid-Based Clustering]
    --> D[Environmental Variables]
    --> E[MaxEnt Modeling]
    --> F[Habitat Suitability Prediction]
    --> G[Ecological Corridor Identification]

style A fill:#2E7D32,color:#fff,stroke:#1B5E20,stroke-width:2px
style B fill:#2E7D32,color:#fff,stroke:#1B5E20,stroke-width:2px
style C fill:#2E7D32,color:#fff,stroke:#1B5E20,stroke-width:2px
style D fill:#2E7D32,color:#fff,stroke:#1B5E20,stroke-width:2px
style E fill:#2E7D32,color:#fff,stroke:#1B5E20,stroke-width:2px
style F fill:#2E7D32,color:#fff,stroke:#1B5E20,stroke-width:2px
style G fill:#2E7D32,color:#fff,stroke:#1B5E20,stroke-width:2px
```



### 1. Data Collection

The study utilizes **6,638 African lion occurrence records** stored in `Sample.csv`. Each observation contains temporal information and geographic coordinates representing recorded lion sightings across Africa. These occurrence records form the primary input for habitat suitability modeling.

---

### 2. Data Preprocessing

The collected dataset is cleaned to improve data quality before analysis. Duplicate records, incomplete observations, and invalid geographic coordinates are removed to ensure reliable spatial modeling. The processed dataset is then converted into a GIS-compatible format.

---

### 3. Grid-Based Clustering

To reduce spatial sampling bias, the study area is divided into uniform spatial grids. Multiple observations occurring within the same grid cell are represented by a single occurrence point. This preserves the spatial distribution of lion sightings while preventing overrepresentation from heavily sampled regions.

---

### 4. Environmental Variable Preparation

Environmental raster layers influencing lion habitat selection are collected and standardized to a common coordinate system and spatial resolution. These variables include climatic, vegetation, topographical, and land cover datasets used during habitat suitability modeling.

---

### 5. Habitat Suitability Modeling

The processed occurrence records and environmental variables are supplied to the **Maximum Entropy (MaxEnt)** algorithm. Using presence-only data, MaxEnt estimates habitat suitability by identifying environmental conditions associated with known lion occurrences.

---

### 6. Habitat Suitability Prediction

The trained model generates a continuous habitat suitability map, assigning each location a suitability score ranging from low to high. These predictions identify regions capable of supporting sustainable African lion populations.

---

### 7. Ecological Corridor Identification

The habitat suitability map is further analyzed to identify ecological corridors connecting fragmented habitats. These corridors facilitate wildlife movement, promote genetic diversity, and provide valuable insights for long-term conservation planning.



## Results

The Maximum Entropy (MaxEnt) model successfully identified environmentally suitable habitats for African lions across the African continent. The generated outputs highlight habitat suitability patterns, key environmental variables, and potential ecological corridors that support wildlife conservation planning.

---

### Habitat Suitability Mapping

*Image Placeholder*

The habitat suitability map classifies the study area into regions of low, moderate, and high suitability. Areas with higher suitability indicate favorable environmental conditions capable of supporting sustainable African lion populations.

---

### Model Performance

*ROC Curve Placeholder*

The model achieved a **training AUC of 0.887**, indicating strong predictive performance. This demonstrates the model's ability to effectively distinguish environmentally suitable habitats using presence-only occurrence data.

---

### Variable Importance

*Jackknife Analysis Placeholder*

The Jackknife analysis identifies the contribution of each environmental variable to the model. Results indicate that **BIO16 (Precipitation of the Wettest Quarter)** is the most influential predictor affecting habitat suitability.

---

### Response Curves

*Response Curves Placeholder*

Response curves illustrate how predicted habitat suitability changes with variations in environmental conditions, providing insights into the ecological preferences of African lions.



## Tech Stack

| Category | Technology |
|-----------|------------|
| Programming Language | Python |
| Species Distribution Modeling | MaxEnt |
| GIS Software | ArcGIS |
| Data Processing | Pandas, NumPy |
| Visualization | Matplotlib |
| Data Source | GBIF |


## Repository Structure

```text
WildlifePitchMonitoringSystem/
│
├── assets/          # Images and diagrams
├── data/            # Input datasets
├── docs/            # Research documents 
├── outputs/         # Model outputs 
└── README.md     
```




