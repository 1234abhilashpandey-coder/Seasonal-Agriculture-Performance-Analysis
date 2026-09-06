# Seasonal Agriculture Performance Analysis

A data analytics project examining how agricultural performance varies across seasons in India, using a dataset of 4,000 farm records spanning 8 states, 8 crops, and 3 cropping seasons (Kharif, Rabi, Zaid).

## Overview

Agricultural outcomes are shaped by seasonal shifts in rainfall, temperature, soil conditions, and resource use. This project analyzes seasonal farm data to uncover patterns in yield, production, resource usage, and profitability, and to understand how these patterns differ across seasons, crops, and states.

## Objective

- Explore and clean the seasonal agriculture dataset
- Compare yield, production, and profitability across Kharif, Rabi, and Zaid seasons
- Examine how environmental conditions (rainfall, temperature, humidity, soil moisture) and resource usage (fertilizer, pesticide, water, irrigation method) vary by season
- Identify relationships between environmental/resource factors and yield or profit
- Test whether seasonal differences are statistically significant (ANOVA)
- Check whether seasonal patterns hold consistently across different crops and states
- Draw evidence-based conclusions and recommendations for seasonal agricultural planning

## Dataset

`seasonal_agriculture_performance_dataset.csv` — 4,000 farm records with 28 columns covering:
- **Farm details:** state, district, crop, season, farm area
- **Environmental conditions:** rainfall, temperature, humidity, sunlight hours, soil pH, soil moisture
- **Resource usage:** nitrogen, phosphorus, potassium, fertilizer, pesticide, irrigation method, water used
- **Outcomes:** yield, production, market price, total cost, revenue, profit, water efficiency, disease/pest risk

## Methodology

1. **Data cleaning** — handled missing values in rainfall, soil moisture, and yield columns using season-wise median imputation; checked for duplicates and inconsistent categories
2. **Exploratory analysis** — compared yield, production, environmental conditions, resource usage, and profitability across seasons using summary statistics and visualizations
3. **Relationship analysis** — built a correlation matrix and scatter plots to study how environmental and resource factors relate to yield and profit
4. **Cross-sectional analysis** — examined yield by crop×season and profit by state×season using pivot tables and heatmaps
5. **Statistical testing** — ran one-way ANOVA to test whether seasonal differences in yield and profit are statistically significant

## Key Findings

- **Kharif** is the strongest season overall: highest average yield, highest average profit, and the highest share of profitable farms (57.8%)
- **Zaid** is the weakest season: lowest yield, negative average profit, and only 35.5% of farms profitable, driven largely by the highest water usage combined with the lowest water efficiency
- Seasonal profit differences are statistically significant (ANOVA, p < 0.001), but raw yield differences are not (p = 0.212) once outliers are accounted for
- The Kharif > Rabi > Zaid yield ranking holds for every crop in the dataset with no exceptions
- Seasonal profitability patterns are not uniform across states — Zaid remains profitable in Punjab, Karnataka, and Madhya Pradesh, while Andhra Pradesh and Gujarat see heavy losses
- Fertilizer use and seed quality score show almost no correlation with yield or profit in this dataset

## Tools Used

- Python 3 (Google Colab / Jupyter Notebook)
- Pandas, NumPy — data cleaning and preparation
- Matplotlib, Seaborn — data visualization
- SciPy — statistical testing (ANOVA)

## Repository Structure

```
├── seasonal_agriculture_performance_dataset.csv   # Raw dataset
├── Seasonal_Agriculture_Performance_Analysis.ipynb # Full analysis notebook
└── README.md
```

## Author

Abhilash Pandey
College of Innovative Management and Sciences
VOIS AICTE Batch 2026-2027
