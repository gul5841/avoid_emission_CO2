# Spatial-Temporal Analysis of Renewable Energy Generation and Avoided CO2 Emissions in Turkey (2021-2025)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)

## 📌 Project Overview
This repository contains the dataset, analysis scripts, and visualization tools for the spatial-temporal evaluation of unlicensed renewable energy production in Turkey. The study covers all 81 provinces on a monthly basis from 2021 to 2025, analyzing four primary renewable energy sources: **Biomass, Solar, Hydropower, and Wind**. 

The main objective is to identify regional generation patterns, cluster provinces based on their capacity-energy-emission profiles, and calculate the corresponding avoided CO2 emissions using advanced data mining and machine learning techniques.

## 📊 Dataset Description
The comprehensive multidimensional dataset was structured using Large Language Models (LLM) for advanced data mining. The conceptual structure includes:
* **Spatial-Temporal Identifiers:** Province license plate codes (1-81), years (2021-2025), and months.
* **Meteorological Variables:** Provincial population, rainfall, solar radiation, temperature, and wind speed.
* **C_ (Capacity):** Installed unlicensed electricity capacity (MW).
* **G_ (Generation):** Electricity generation (MWh).
* **A_ (Avoided):** Calculated avoided CO2 emissions (tCO2e).
* **T_Emission:** Total estimated CO2 emissions.
* **CEEI:** Capacity-Energy-Emission Index.

## ⚙️ Methodology
The analytical workflow consists of the following primary stages:
1. **LLM-Based Data Mining:** Extraction and structuring of raw data sources.
2. **Data Preprocessing & Normalization:** Scaling variables for machine learning models.
3. **K-Means Clustering Analysis:** Grouping 81 provinces based on their renewable energy profiles.
   * *Elbow Method:* Used to determine the optimal number of clusters ($k$).
4. **Avoided CO2 Calculation:** Estimating the environmental impact of regional renewable generation.
5. **GIS Spatial Visualization:** Mapping generation amounts and avoided CO2 emissions across Turkey (darker shades indicate higher levels of avoided CO2).




## 📂 Repository Structure
```text
├── notebooks/                  # Jupyter notebooks for the analysis workflow
│   ├── data_extraction/        # LLM-based data mining and data parsing scripts
│   └── modelling/              # K-Means clustering, CO2 calculations, and visualizations
├── processed_data/             # Cleaned, normalized, and analysis-ready datasets
│   ├── final/                  # Final integrated dataset used for machine learning
│   └── steps/                  # Intermediate data outputs from preprocessing stages
└── raw_data/                   # Original, unmodified source data
│   ├── energy_reports/         # Unlicensed capacity and generation reports (2021-2025)
│   ├── geo_metadata/           # Spatial identifiers and province plate codes
│   ├── map_data/               # GIS shapefiles and spatial mapping coordinates
│   ├── population/             # Provincial population statistics
│   ├── rain/                   # Meteorological data: Rainfall
│   ├── solar/                  # Meteorological data: Solar radiation
│   ├── temperatur/             # Meteorological data: Temperature
│   └── wind/                   # Meteorological data: Wind speed
│
├── requirements.txt        # Python dependencies required to run the code
└── README.md               # Project documentation

