# Predicting Gas Station Density Across North Carolina Counties

> Predictive modeling project analyzing the socioeconomic and infrastructural drivers of gas station density across North Carolina counties using R.

This repository contains the code and documentation for an econometric and machine learning project conducted as part of ECON 573 – Machine Learning and Econometrics at UNC Chapel Hill.

The project explores the extent to which socioeconomic, demographic, and infrastructural variables can predict gas station density across all 100 counties in North Carolina using 2020 data. By applying a wide range of models — from linear regression and variable selection techniques to regularization and non-linear methods — we evaluate which factors most accurately and parsimoniously predict gas station distribution.

---

## Repository Structure

| File | Description |
|------|-------------|
| `data-visualization-linear-manual-selection.Rmd` | RMarkdown script for data visualization and linear regression modeling using manual variable selection (including VIF-based removal and diagnostic plots). |
| `data-visualization-linear-manual-selection.pdf` | Rendered output of the above `.Rmd`, showing results, plots, and interpretations. |
| `master-code-sheet.Rmd` | Combined reference file containing key functions and model implementations across the project. Serves as a centralized code base. |
| `non-linear-methods.Rmd` | RMarkdown file implementing and comparing non-linear modeling techniques, including splines, GAMs, regression trees, and random forests. |
| `non-linear-methods.pdf` | Rendered output of non-linear modeling results with visualizations and performance summaries. |
| `presentation.pdf` | Slides from the final class presentation, summarizing the project motivation, methodology, key results, and conclusions. |
| `research-paper.pdf` | Full academic-style research report, including introduction, methodology, results, and references. |
| `variable-selection.Rmd` | RMarkdown script exploring variable selection approaches: Best Subset Selection, Forward and Backward Stepwise Selection, and PCA. |
| `variable-selection.pdf` | Rendered output of the variable selection analysis with figures, tables, and model evaluation. |

---

## Methods Overview

We implemented the following modeling techniques:

- **Linear Regression**: Baseline model using all 33 predictors, followed by VIF-based manual variable reduction.
- **Best Subset Selection, Forward/Backward Stepwise Selection**: Used to identify smaller, high-performing linear models based on adjusted R², BIC, Cp, and cross-validation.
- **Regularization**:  
  - **LASSO** for sparse variable selection  
  - **Ridge** to reduce multicollinearity  
  - **Elastic Net** as a balance between both
- **Principal Component Regression (PCR)**: Dimension reduction using uncorrelated linear components.
- **Non-Linear Models**:  
  - **Natural Splines & GAMs** to capture curved predictor relationships  
  - **Decision Trees & Random Forests** to uncover nonlinear interactions and variable importance

---

## Results Summary

- The best-performing model (based on 10-fold CV RMSE) was a **4-variable linear regression** selected via **Best Subset Selection**, achieving:
  - **RMSE**: 10.49  
  - **Adjusted R²**: 0.974  
  - **Predictors**:  
    - Families Below Poverty (`fpov`)  
    - Average Weekly Pay (`awpw`)  
    - Average Annual Employment (`aaepw`)  
    - Total State Highway Miles (`shigh`)  

| Model                    | RMSE  | R²     | Notes                                     |
|--------------------------|-------|--------|-------------------------------------------|
| Best Subset (4 vars)     | 10.49 | 0.9743 | Best predictive performance + simplicity  |
| LASSO (6 vars)           | 11.16 | 0.966  | Balanced sparsity and accuracy            |
| Elastic Net (11 vars)    | 13.04 | 0.954  | Broader variable inclusion                |
| Ridge (all vars)         | 28.41 | 0.782  | Worst predictive accuracy                 |
| Random Forest            | 8.85  | 0.899  | Best accuracy, but limited interpretability |
| GAM (Best Subset vars)   | 10.76 | 0.976  | Captured non-linear effects               |

---

## Key Findings

- **Socioeconomic and infrastructural variables are strong predictors** of gas station density.
- A **simple 4-variable linear model** can outperform more complex models in predictive accuracy.
- **Poverty rates, employment, wages, and road infrastructure** consistently emerged as top predictors.
- **Random forests and GAMs** revealed non-linearities but sacrificed some interpretability.
- These results offer actionable insights for **urban planning and infrastructure investment** across rural and urban counties.

---

## How to Run

To reproduce the results:

1. Install required R packages:
```r
install.packages(c("tidyverse", "leaps", "glmnet", "pls", "gam", "rpart", "randomForest", "caret", "e1071", "splines"))
```

2. Open and knit the `.Rmd` files in RStudio:
- Start with `data-visualization-linear-manual-selection.Rmd`
- Follow with `variable-selection.Rmd` and `non-linear-methods.Rmd`

3. Ensure that all datasets and figures are either included or downloaded from the sources listed below.

## Data Sources

| Source | Variables |
|--------|-----------|
| NC Department of Agriculture & Consumer Services | Gas station locations (2020) |
| U.S. Census Bureau (ACS) | Income, population, education, employment |
| NC Department of Transportation | Highway and road mileage |
| NC Association of County Commissioners | Housing values and taxes |
| American Community Survey (2019–2023) | Poverty statistics |

---

## Acknowledgments

This project was completed as part of **ECON 573 – Machine Learning and Econometrics** at the University of North Carolina at Chapel Hill, under the guidance of **Professor Andrii Babii**.

**Team members**:
- Sergiy Mouradkhanian  
- Max Dethlefs  
- Eleanor Curley  
- Juan Mateo Alvarez

