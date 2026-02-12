# CO₂–Glacier Climate Analysis

## Objective

Built an end-to-end data pipeline to evaluate whether long-term CO₂ growth correlates with measurable glacier change.

**Core Focus:** Large-scale data cleaning, imputation strategy, and statistical validation under high missingness.

---

## Dataset

- 272+ years of CO₂ emissions (1750–2020)
- 100,000+ glacier records (1900–2000)
- Sources: World Bank, Global Carbon Project, NSIDC

---

## Data Challenges

- Glacier dataset contained up to 40%+ missing values in key features
- Multiple time columns required reconstruction and alignment
- CO₂ data spanned 272 years across overlapping sources
- Large sample size introduced statistical significance bias

---

## Approach

### Data Engineering
- Web-scraped CO₂ data using Selenium (with JSON fallback)
- Merged multi-century climate datasets
- Outlier detection (IQR filtering)
- Time alignment and yearly aggregation

### Missing Data Strategy

The glacier dataset contained substantial missingness across structural variables.

To preserve analytical validity:

- Applied median imputation for structural stability
- Built regression models to estimate missing elevation and width values
- Used IterativeImputer to reconstruct temporal variables
- Evaluated imputation quality using MAE, R², and cross-validation


### Statistical Analysis
- Pearson correlation testing
- Time-lag analysis (±10 years)
- Polynomial regression modelling
- Log-scale visualisation for multi-order magnitude comparison

---

## Key Results

- Weak positive correlation between CO₂ and glacier area (r ≈ 0.27)
- Statistically significant p-values influenced by large sample size
- Very low regression explanatory power (R² ≈ 0.0007)
- Demonstrates the distinction between statistical significance and practical predictive strength
- Processed and cleaned 100,000+ glacier records with multi-stage imputation and validation.

---

## Tech Stack

Python • Pandas • NumPy • Scikit-learn • Selenium • Matplotlib • Seaborn • SciPy

---

## Run Locally

```bash
pip install -r requirements.txt
jupyter notebook co2-glacier-analysis.ipynb
```
