# CO2-Glacier Analysis (Programming with Data)

[![Python](https://img.shields.io/badge/Python-3.9-blue)](https://python.org) 
[![Pandas](https://img.shields.io/badge/Pandas-2.0-green)](pandas.pydata.org)

## 📋 Project Overview
Analyzed **global CO₂ emissions (1750–2020)** vs **glacier melt (1900–2000)** using data from World Bank, Global Carbon Project, and NSIDC. Built complete **ETL pipeline** + **statistical analysis**.

**Key Findings:**
- Weak correlation: **r=0.275** (CO₂ vs glacier area)
- Polynomial regression: **R²=0.0007** 
- Processed **272+ years** of climate data

## 🎯 Business Value
Demonstrates skills in:
- **ETL pipelines** (scraping → cleaning → merging)
- **Data quality** (outliers, imputation, normalization)
- **Statistical analysis** (correlation, regression)
- **Climate impact assessment**

## 📊 Data Sources
Three sources in `archive/` folder:
1. `scraped_data.json` – Backup JSON (Macrotrends/World Bank)
2. `GCB2022v27_MtCO2_flat.csv` – Global Carbon Project CO₂
3. `database_glacier.csv` – NSIDC glacier dataset

## 📈 Output Files
Generated in `archive/`:
1. `cleaned_co2_30_years.csv`
2. `cleaned_co2_3_centuries.csv`
3. `merged_co2_data.csv`
4. `cleaned_glacier_data.csv`
5. `merged_co2_glacier_data.csv`

## 🛠 Tech Stack
| Category | Tools |
|----------|-------|
| Data | Pandas, NumPy |
| Viz | Matplotlib, Seaborn |
| ML | Scikit-learn |
| Scraping | Selenium |

## 🚀 Quick Start
```bash
pip install -r requirements.txt
# Run notebook
jupyter notebook co2-glacier-analysis.ipynb
