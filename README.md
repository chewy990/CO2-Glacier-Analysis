# CO2-Glacier Analysis

[![Python](https://img.shields.io/badge/Python-3.9-blue)](https://python.org) 
[![Pandas](https://img.shields.io/badge/Pandas-2.0-green)](pandas.pydata.org)

## Project Overview
I wanted to see if rising CO₂ emissions were causing glaciers to melt faster. Used data from 1750-2020 (CO₂) and 1900-2000 (glaciers) from World Bank, Global Carbon Project, and NSIDC.

**Key Findings:**
- Correlation: r=0.275 (CO₂ vs glacier area)
- Polynomial regression: R²=0.0007 
- Processed 272+ years of climate data

## ETL Process
1. EXTRACT: Web-scraped Macrotrends (Selenium) + GCP/NSIDC CSVs
2. TRANSFORM: Outliers, missing values (linear imputation), merged datasets
3. LOAD: 5 cleaned CSVs for analysis

## Data Sources
Three sources in `archive/` folder:
1. `scraped_data.json` – Backup JSON (Macrotrends/World Bank)
2. `GCB2022v27_MtCO2_flat.csv` – Global Carbon Project CO₂
3. `database_glacier.csv` – NSIDC glacier dataset

## Output Files
Generated in `archive/`:
1. `cleaned_co2_30_years.csv`
2. `cleaned_co2_3_centuries.csv`
3. `merged_co2_data.csv`
4. `cleaned_glacier_data.csv`
5. `merged_co2_glacier_data.csv`

## Tech Stack
| Category      | Tools                    |
|---------------|--------------------------|
| Data          | Pandas, NumPy           |
| Visualization | Matplotlib, Seaborn     |
| ML            | Scikit-learn            |
| Scraping      | Selenium                |

## Quick Start
```bash
pip install -r requirements.txt
jupyter notebook co2-glacier-analysis.ipynb
```

## Screenshot
<img width="1026" height="636" alt="log_scale_graph" src="https://github.com/user-attachments/assets/89c259ce-a20a-4773-92a4-6a1407ddf5a1" />

