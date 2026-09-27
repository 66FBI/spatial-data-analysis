# Spatial Data Analysis

A collection of practical spatial data analysis exercises developed in **Python**, covering vector and raster GIS, interactive mapping, OpenStreetMap data acquisition, point-process analysis, spatial statistics, clustering and spatial autocorrelation.

The repository progresses from fundamental geospatial data operations to more advanced methods for analyzing spatial patterns and relationships.

## Notebooks

### 1. [Vector Data Loading and Visualization](notebooks/01_vector_data_loading_visualization.ipynb)

Introduction to geospatial vector data processing with **GeoPandas**.

Topics include:

- loading spatial datasets,
- inspecting geometries and attributes,
- coordinate reference systems,
- spatial data preparation,
- thematic and contextual visualization,
- combining GeoPandas plots with basemaps.

### 2. [Vector Spatial Operations](notebooks/02_vector_spatial_operations.ipynb)

Geometric and spatial operations on vector datasets.

The notebook covers:

- length, area and distance calculations,
- spatial relationships between geometries,
- buffers,
- spatial joins and overlays,
- geometric transformations,
- practical manipulation of GeoDataFrames.

### 3. [Raster Terrain Analysis](notebooks/03_raster_terrain_analysis.ipynb)

Raster data processing and terrain analysis using **Rasterio**.

The analysis includes:

- reading raster datasets and metadata,
- raster visualization,
- accessing raster values and spatial coordinates,
- sampling raster values,
- clipping rasters using vector geometries,
- analysis of elevation data,
- terrain slope calculation.

The exercises use elevation data for the Kraków area to connect raster operations with practical terrain analysis.

### 4. [Interactive Mapping with Folium](notebooks/04_interactive_mapping_folium.ipynb)

Construction of interactive web maps using **Folium**.

The notebook explores:

- map configuration and basemaps,
- markers and custom icons,
- vector overlays,
- GeoJSON layers,
- tooltips and popups,
- feature groups and layer controls,
- marker clustering,
- CRS transformation,
- MiniMap controls,
- animated routes with AntPath.

### 5. [OpenStreetMap and Overpass Queries](notebooks/05_openstreetmap_overpass_queries.ipynb)

Acquisition and processing of **OpenStreetMap** data using the Overpass API.

Topics include:

- communication with Overpass servers,
- construction of spatial OSM queries,
- retrieval of nodes, ways and relations,
- conversion of OSM responses to GeoJSON,
- transformation into GeoDataFrames,
- visualization of downloaded geographic features.

### 6. [Point Process Simulation](notebooks/06_point_process_simulation.ipynb)

Simulation of spatial point processes and investigation of their statistical properties.

The notebook introduces methods for generating and visualizing point patterns under different spatial assumptions, providing a foundation for subsequent point-pattern analysis.

Topics include:

- generation of spatial point patterns,
- random point processes,
- simulation within spatial study areas,
- visualization and comparison of simulated patterns.

### 7. [Point Process Intensity Estimation](notebooks/07_point_process_intensity_estimation.ipynb)

Estimation of spatial point-process intensity using multiple approaches.

The analysis includes:

- division of study areas into regular grids,
- local point-density estimation,
- spatial intensity visualization,
- kernel density estimation,
- comparison of intensity estimates under different parameter choices.

The notebook uses **KDEpy** together with GeoPandas and Shapely for spatial intensity analysis.

### 8. [Point Pattern Distance Functions](notebooks/08_point_pattern_distance_functions.ipynb)

Analysis of spatial point patterns using distance-based statistics.

The notebook investigates relationships between observed points using methods including:

- nearest-neighbor distances,
- **G-function** analysis,
- **F-function** analysis,
- empirical distance distributions,
- comparison with simulated spatial patterns,
- Monte Carlo envelopes.

These methods are used to assess whether observed point distributions differ from patterns expected under spatial randomness.

### 9. [Point Pattern Statistical Tests](notebooks/09_point_pattern_statistical_tests.ipynb)

Statistical testing of spatial point-pattern characteristics.

The notebook extends the previous point-process analyses using formal statistical procedures, including:

- quadrat-based analysis,
- **Morisita index**,
- chi-square testing,
- Kolmogorov–Smirnov testing,
- comparison of observed and theoretical spatial distributions.

The exercises demonstrate how exploratory spatial patterns can be evaluated using statistical hypothesis testing.

### 10. [Spatial Clustering and Autocorrelation](notebooks/10_spatial_clustering_autocorrelation.ipynb)

Application of clustering algorithms and spatial autocorrelation statistics to geographic data.

The notebook covers clustering methods including:

- **K-Means**
- **Agglomerative Clustering**
- **DBSCAN**
- **HDBSCAN**

It also introduces spatial weight matrices based on:

- Rook contiguity,
- K-nearest neighbors,
- distance bands.

Spatial structure is evaluated using global statistics including:

- **Moran's I**
- **Geary's C**

This final notebook combines conventional machine-learning clustering with explicitly spatial statistical methods using **PySAL**.

## Topics

The exercises collectively cover:

- vector GIS analysis
- raster and terrain analysis
- coordinate reference systems
- interactive web mapping
- OpenStreetMap and Overpass API
- spatial point processes
- kernel density estimation
- point-pattern analysis
- Monte Carlo simulation
- spatial statistical testing
- clustering
- spatial weights
- spatial autocorrelation

## Technologies

- **Python**
- **GeoPandas**
- **Rasterio**
- **Shapely**
- **Folium**
- **PySAL**
- **KDEpy**
- **scikit-learn**
- **SciPy**
- **NumPy**
- **pandas**
- **Matplotlib**
- **Seaborn**
- **Contextily**
- **OpenStreetMap / Overpass API**
- **Jupyter Notebook**

## Repository Structure

```text
spatial-data-analysis/
├── data/
│   ├── KRK_data.gpkg
│   ├── Miejscowosci.csv
│   ├── TPN_data.gpkg
│   ├── Wojewodztwa_dane.csv
│   └── data.gpkg
├── notebooks/
│   ├── 01_vector_data_loading_visualization.ipynb
│   ├── 02_vector_spatial_operations.ipynb
│   ├── 03_raster_terrain_analysis.ipynb
│   ├── 04_interactive_mapping_folium.ipynb
│   ├── 05_openstreetmap_overpass_queries.ipynb
│   ├── 06_point_process_simulation.ipynb
│   ├── 07_point_process_intensity_estimation.ipynb
│   ├── 08_point_pattern_distance_functions.ipynb
│   ├── 09_point_pattern_statistical_tests.ipynb
│   └── 10_spatial_clustering_autocorrelation.ipynb
├── requirements.txt
└── README.md
```

## Installation

The Python dependencies used throughout the notebooks are listed in `requirements.txt`.

```bash
pip install -r requirements.txt
```

## Authors

**Michał Kuśnierz**  
**Tymoteusz Chrzan**  
**Tymoteusz Hajduk**

Developed as part of the **Spatial Data Analysis** course in the Geoinformatics program at **AGH University of Science and Technology**, 2025.
