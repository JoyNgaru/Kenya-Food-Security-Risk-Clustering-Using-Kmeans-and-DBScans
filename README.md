# Kenya Food Security Risk Clustering Using K-means and DBScans
About Dataset
This dataset supports the development of a machine learning early-warning system for food insecurity across Kenya's Arid and Semi-Arid Lands (ASAL).
https://www.kaggle.com/datasets/mrtrev254/kenya-food-security-risk

It combines three critical data streams — IPC food insecurity outcomes, CHIRPS rainfall indicators, and MODIS NDVI vegetation features — into a single county-level, time-aligned resource for exploratory analysis, predictive modeling, and humanitarian research.

Current project stage: Data preparation, feature engineering, and exploratory analysis.
Next stage: Baseline classification model to predict high-risk food insecurity cases 1–3 months in advance.

The Problem
Recent IPC projections indicate that millions of Kenyans may face IPC Phase 3 "Crisis" level food insecurity during severe drought periods.
Kenya's ASAL counties are particularly vulnerable to drought-driven food crises.
Humanitarian agencies often react to crises after they peak, not before.
There is limited access to simple, county-level early-warning tools that connect food insecurity outcomes with publicly available environmental indicators such as rainfall and vegetation health.
This dataset was built to help close that gap by providing a clean, merged resource that links environmental stress to food insecurity severity at the county level.

Data Sources
Dataset	Source	Type	Coverage
IPC Acute Food Insecurity	FEWS NET / HDX	Food insecurity phase classifications (Phase 1–5) and population percentages	Kenya ASAL counties
CHIRPS Rainfall	UCSB Climate Hazards Center	Monthly rainfall estimates with station calibration	2019–2026
MODIS NDVI	NASA/USGS via Google Earth Engine	Satellite vegetation health indices from MODIS Terra	2019–2026
Kenya County Boundaries	HDX / administrative boundaries	County shapefiles and GeoJSON for spatial alignment	23 ASAL counties
Files in This Dataset
1. ipc_rainfall_ndvi_master_dataset.csv
The main analysis-ready dataset. It combines IPC outcomes with CHIRPS rainfall and MODIS NDVI features at the county level.

Key columns include:

county — Kenya ASAL county name
ipc_date / analysis_period — time alignment for IPC reporting windows
max_ipc_phase — worst IPC phase recorded for the county
phase_3_plus_population — population in IPC Phase 3 or worse
phase_3_plus_percentage — percentage of population in Crisis level or worse
rainfall_3_month_avg / rainfall_6_month_avg — rolling rainfall averages
mean_ndvi / ndvi_3_month_mean / ndvi_6_month_mean — vegetation health indicators and rolling averages
ndvi_anomaly — deviation from normal vegetation conditions
Use this file for: exploratory data analysis, correlation analysis, feature engineering, and baseline machine learning models.

2. phase3_environment_correlation_summary.csv
A summary table ranking the strongest correlations between environmental indicators and Phase 3+ food insecurity population percentage.

This file is useful for quick insight into which drought-related indicators are most associated with serious food insecurity burden.

Key Features
County-level aggregation for Kenya ASAL counties
Time-aligned environmental and food security indicators
Rolling rainfall and NDVI features prepared for analysis
NDVI anomaly values included for vegetation stress analysis
Correlation-ready structure for drought and food security exploration
Open project license for the derived project files, subject to original data source terms
Current Findings
Exploratory analysis on this dataset reveals:

Counties such as Turkana, Mandera, Marsabit, Wajir, Garissa, Isiolo, Samburu, Tana River, Baringo, and Kwale repeatedly appear as high-risk counties.
Turkana had the highest average Phase 3+ population percentage.
Higher IPC severity is generally associated with lower rainfall and weaker vegetation health.
NDVI indicators showed stronger negative relationships with Phase 3+ population percentage than rainfall indicators.
The strongest environmental signal was the 3-month NDVI mean, with a correlation of approximately -0.692 against Phase 3+ population percentage.
The 6-month rainfall average also showed a meaningful negative relationship with Phase 3+ population percentage, with a correlation of approximately -0.585.
Important note: These results show association, not proof of causation. Food insecurity is also influenced by market prices, livestock conditions, conflict, income, market access, humanitarian support, and other socioeconomic factors.

Use Cases
This dataset can support:

Predictive modeling of food insecurity severity or high-risk classification
Drought impact assessment and environmental monitoring
Humanitarian early-warning research for NGOs and government agencies
Climate-food security policy analysis and resource allocation planning
Educational projects in data science, geospatial analysis, remote sensing, and machine learning
Related Project & Code
The full data pipeline, cleaning notebooks, EDA, and future modeling code are available on GitHub:

🔗 https://github.com/MastaT002/Drought-Food-Security-Early-Warning-System

The repository includes:

IPC data cleaning and inventory
CHIRPS rainfall collection and feature engineering
MODIS NDVI extraction via Google Earth Engine
Master dataset merging and correlation analysis
Jupyter notebooks for reproducible analysis
How to Cite
If you use this dataset in your research or project, please cite:

Trevor Mulundi. Kenya Food Security Risk Dataset: IPC, CHIRPS Rainfall, and MODIS NDVI (2019–2026). Kaggle, 2026.
GitHub: https://github.com/MastaT002/Drought-Food-Security-Early-Warning-System

License
This project is shared under the MIT License for the derived project files, subject to the terms and conditions of the original data sources.
