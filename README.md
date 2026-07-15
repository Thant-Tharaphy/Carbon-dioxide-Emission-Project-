# Carbon-dioxide-Emission-Project-


## Project Overview

This project explores global CO₂ emission patterns using clustering, machine learning and explainable AI.

The analysis combines country-level energy, economic and emission indicators to identify different energy-system profiles and examine the factors associated with CO₂ emissions.

## Project at a Glance

- 50,191 original records
- 79 variables
- 7,412 records after filtering
- Data analysed from 1990 onward
- 106 countries included in clustering analysis
- 2 energy-system clusters identified
- 4 regression models compared
- Best model R²: 0.99
- Best model MAE: 19.72

## Objectives

1. Identify distinct country energy-system profiles using clustering.
2. Compare machine learning models for CO₂ emission prediction.
3. Examine the drivers behind model predictions.
4. Combine clustering and explainability to better understand emission patterns.

## Dataset

The project uses the Our World in Data CO₂ dataset.

The original dataset contained:

- 50,191 rows
- 79 columns

The variables cover:

- CO₂ emissions
- Population
- GDP
- Coal emissions
- Oil emissions
- Gas emissions
- Energy consumption
- Energy intensity
- Greenhouse gases
- Temperature change indicators

After reviewing missing values, the data was filtered to countries with valid ISO codes and observations from 1990 onward.

Final analytical dataset:

7,412 records.

## Exploratory Data Analysis

The exploratory analysis included:

- Missing-value analysis
- Data completeness heatmaps
- Descriptive statistics
- CO₂ distribution analysis
- Outlier detection
- Log transformation
- Historical emission trends
- Geographic emission analysis

The analysis identified strong skewness in CO₂-related variables and large differences between countries.

## Country Clustering

K-Means clustering was used to identify countries with similar energy-system characteristics.

Features included:

- Coal share
- Oil share
- Gas share
- Energy per GDP
- Energy per capita

The optimal number of clusters was:

K = 2

Silhouette Score:

0.3461

### Cluster 0

- Coal share: 23.6%
- Oil share: 48.4%
- Gas share: 20.2%
- Energy intensity: 1.10
- Energy per capita: 22,622 kWh

### Cluster 1

- Coal share: 6.5%
- Oil share: 36.7%
- Gas share: 51.6%
- Energy intensity: 2.12
- Energy per capita: 79,659 kWh

PCA was also used to examine the statistical structure and visual separation of the clusters.

## Machine Learning Models

Four regression models were compared:

| Model | MAE | R² Score |
|------|------|----------|
| Linear Regression | 19.72 | 0.99 |
| Random Forest | 122.86 | 0.92 |
| XGBoost | 265.44 | 0.58 |
| Explainable Boosting Machine | 337.15 | 0.61 |

Linear Regression achieved the lowest MAE and highest R² score.

The result suggests strong persistence in historical emission behaviour within the analysed dataset.

## Explainable AI

Model explainability techniques were used to move beyond prediction and examine why emission estimates changed.

Methods included:

- SHAP
- Partial Dependence Plots
- Explainable Boosting Machine

GDP and historical emission trends appeared as important model drivers.

The analysis also explored differences in emission behaviour between country clusters.

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- XGBoost
- InterpretML
- SHAP
- PCA
- K-Means
- Matplotlib
- Seaborn
- Plotly
- GeoPandas

## Project Workflow

Data Collection
↓
Data Understanding
↓
Missing Value Analysis
↓
Data Filtering
↓
Exploratory Data Analysis
↓
Feature Engineering
↓
Country Clustering
↓
PCA Analysis
↓
Regression Modelling
↓
Model Comparison
↓
SHAP & PDP Explainability
↓
Cluster-Based Interpretation

## Key Learning

This project helped me connect exploratory data analysis, unsupervised learning, regression and model explainability within one analytical workflow.

A major focus was not only comparing model accuracy, but understanding how country energy structures and economic indicators relate to different emission patterns.
