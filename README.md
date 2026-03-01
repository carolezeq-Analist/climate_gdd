# climate_gdd
Agricultural insurance validation pipeline — integrated SICOR (Central Bank of Brazil) rural credit data with INMET meteorological stations using Haversine distance..

Agroclimatic Risk Assessment Using Insurance Claims and INMET Data

Overview

This project investigates recurrent agricultural insurance claims for soybean crops by integrating:
	•	Geospatial clustering of claim coordinates
	•	Meteorological data from INMET stations
	•	Precipitation accumulation analysis
	•	Growing Degree Days (GDD) modeling
	•	Phenological stage estimation
	•	Comparison with agronomic literature thresholds

The goal is to assess whether repeated insurance claims are supported by agroclimatic evidence.


Objectives
	•	Detect spatial anomalies in insurance claim records
	•	Identify high-frequency claim locations
	•	Associate claims with nearest meteorological stations
	•	Quantify precipitation during:
	•	Adverse event period
	•	Entire crop cycle
	•	Estimate soybean phenological stages using GDD accumulation
	•	Compare observed climate conditions with agronomic expectations


Data Sources
	•	SICOR insurance claims dataset (CSV)
	•	INMET meteorological stations (hourly data)
	•	Soybean phenological parameters from agronomic literature


Methodology

Data Cleaning and Spatial Validation
	•	Longitude sign correction
	•	Filtering coordinates within Brazil’s geographic bounds
	•	Extraction of soybean-only records
	•	Spatial grouping by centroid coordinates

Anomaly Detection
	•	Counting claims per coordinate
	•	Identification of high-frequency locations
	•	Static spatial visualization (Cartopy)
	•	Interactive heatmap (Folium)

Station Proximity Analysis
	•	Haversine distance calculation
	•	Selection of top 3 closest INMET stations

Meteorological Processing
	•	Parsing hourly station CSV files
	•	Resampling to daily scale
	•	Precipitation accumulation
	•	Crop-cycle rainfall assessment

Growing Degree Days (GDD) Modeling

Daily GDD calculated using:

GDD = ((Tmax + Tmin) / 2) − Tb

Where:
	•	Tb = 10°C (soybean base temperature)
	•	Tmax capped at 38°C
	•	Tmin floored at 10°C
Literature Comparison

Observed precipitation per stage compared with expected agronomic values.


Key Outputs
	•	Spatial anomaly maps
	•	Interactive WebGIS heatmap
	•	Station proximity validation
	•	Rainfall during adverse event
	•	Crop-cycle rainfall totals
	•	GDD accumulation curves
	•	Precipitation vs Literature comparison dashboard


Main Insight

The analysis identified cases where:
	•	Recurrent insurance claims occur in the same spatial location
	•	Adverse events coincided with critical phenological stages
	•	Observed precipitation during grain filling (R3–R5) was below expected agronomic thresholds

This supports the hypothesis that climate stress contributed to yield loss.


Technologies Used
	•	Python
	•	Pandas
	•	NumPy
	•	Matplotlib
	•	Cartopy
	•	Folium
	•	Glob
	•	Bash (data extraction automation)


Skills Demonstrated
	•	Geospatial data validation
	•	Spatial clustering
	•	Agroclimatic modeling
	•	Time-series processing
	•	Phenological stage estimation
	•	Meteorological data parsing
	•	Data visualization (static + interactive)
	•	Analytical reasoning applied to real-world datasets

Author

Carolina da Silva Ezequiel
Environmental Management | Geospatial & Remote Sensing
Python | GIS | Agroclimatic Analysis
