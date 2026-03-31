# Housing Price Prediction — Ames, Iowa

ECON 491, University of Illinois at Urbana-Champaign | Spring 2026

## Overview
Predicting residential sale prices using 1,460 observations and 81 variables from the Ames Housing dataset. 4-person team project; I owned Part 4 (feature engineering + model comparison).

## Files
- `Econ_491_-_Housing_4_-_Step_1_-_EDA___Graph.pdf` — EDA: 50+ visualizations across all 53 variables (boxplots, scatter plots, correlation heatmaps)
- `Econ_491_-_Housing_4_-_Step_4_-_OLS_Benchmark_Model.Rmd` — Data preprocessing + OLS benchmark model (Adj. R² = 0.83, RMSE = $27,348)
- `Housing4_Other_Models_Approach_A.Rmd` — LASSO, log-LASSO, and interaction models; best model RMSE = $24,620

## Methods
- Data cleaning: reduced 81 raw variables to 53 usable predictors
- EDA: 50+ ggplot2 visualizations guiding feature selection
- OLS benchmark with VIF screening, Breusch-Pagan test, robust standard errors
- Model comparison: OLS → LASSO → log+LASSO → log+LASSO+interactions
- Best model: 10% RMSE improvement over baseline ($24,620 vs $27,348)

## Key Finding
BedroomAbvGr has a negative marginal effect on price conditional on living area (p < 0.001) — a "room crowding" effect consistent with hedonic pricing theory.

## Tools
R (tidyverse, ggplot2, glmnet, stargazer)
