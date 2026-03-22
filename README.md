# MMR-MSDS-Capstone
# Predicting Maternal Mortality Using Socioeconomic, Demographic, and Environmental Indicators

## Overview
Maternal mortality remains a major global health challenge, with substantial disparities across countries, regions, and levels of economic development. Despite progress in maternal healthcare, many countries remain above the United Nations Sustainable Development Goal (SDG) target of fewer than 70 maternal deaths per 100,000 live births by 2030.

This capstone develops a reproducible data science framework to analyze, predict, and forecast maternal mortality using country-year panel data. The project integrates socioeconomic, demographic, healthcare, and environmental indicators to identify key drivers of maternal mortality, compare machine learning models, interpret model predictions, and evaluate future outcomes under multiple policy scenarios.

## Research Questions
1. Which socioeconomic, demographic, healthcare, and environmental indicators are most strongly associated with maternal mortality?
2. How do linear, tree-based, kernel-based, and neural network models compare in predicting maternal mortality?
3. What do model interpretation methods reveal about the relative importance of these predictors?
4. How does maternal mortality change under baseline, health investment, climate stress, and development progress scenarios through 2030?
5. What potential causal relationships are supported by fixed-effects panel analysis?

## Data Sources
This project uses publicly available aggregate country-level data, including:
- World Bank World Development Indicators
- World Health Organization maternal mortality estimates
- Environmental and climate indicators such as PM2.5 exposure, heat index days, and cooling degree days

## Methodology
The project follows a full data science workflow:
- Data cleaning and merging into a country-year panel dataset
- Exploratory data analysis and correlation analysis
- Feature preprocessing, imputation, and log transformation of maternal mortality
- Model comparison across:
  - Linear Regression
  - Ridge Regression
  - Lasso Regression
  - Random Forest
  - Gradient Boosting
  - Support Vector Regression (SVR)
  - K-Nearest Neighbors
  - Multilayer Perceptron (MLP)
- Model interpretation using:
  - SHAP
  - Permutation importance
  - Partial dependence plots
- Forecasting maternal mortality to 2030 under multiple scenarios
- Causality analysis using fixed-effects panel regression

## Key Findings
- Support Vector Regression (SVR) was surpassed by Random Forest in which it achieved the best predictive performance among the models tested.
- Fertility rate and GDP per capita emerged as the most influential predictors of maternal mortality.
- Development progress scenarios produced the strongest projected reductions in maternal mortality by 2030.
- Climate stress scenarios slowed progress toward the SDG 3.1 target.
- Fixed-effects panel regression showed significant relationships between fertility, GDP per capita, skilled birth attendance, and maternal mortality.

## Repository Structure
Run notebooks **in numeric order** when possible: Notebook **01** writes `data/processed/country_year_modeling_panel_cleaned.csv`, which **02–06** expect as input. Notebook **01** accepts a merged input from `data/interim/` (see `data/interim/README.md`) or falls back to `data/country_year_modeling_dataset.csv`.

```text
MMR-MSDS-Capstone/
├── README.md
├── requirements.txt
├── data/
│   ├── raw/
│   ├── interim/
│   └── processed/
│   └── data dictionary/
├── notebooks/
│   ├── 01_data_prep_and_preprocessing.ipynb
│   ├── 02_eda_and_feature_analysis.ipynb
│   ├── 03_model_development_and_interpretability.ipynb
│   ├── 04_forecasting_and_conclusions.ipynb
├── figures/
├── outputs/
└── docs/
