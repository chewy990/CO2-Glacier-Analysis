# CO₂–Glacier Climate Analysis

## Objective

Built an end-to-end data pipeline to evaluate whether long-term CO₂ growth correlates with measurable glacier change.

---

## Dataset

- 272+ years of CO₂ emissions (1750–2020)
- 100,000+ glacier records (1900–2000)
- Sources: World Bank, Global Carbon Project, NSIDC

---

## Approach

### Data Engineering
- Web-scraped CO₂ data using Selenium (with JSON fallback)
- Merged multi-century climate datasets
- Outlier detection (IQR filtering)
- Time alignment and yearly aggregation

### Missing Data Handling
- Median imputation
- Linear regression-based imputation
- IterativeImputer for temporal reconstruction
- Cross-validation (MAE, R²) for model evaluation

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

---

## Tech Stack

Python • Pandas • NumPy • Scikit-learn • Selenium • Matplotlib • Seaborn • SciPy

---

## Run Locally

```bash
pip install -r requirements.txt
jupyter notebook co2-glacier-analysis.ipynb
```
