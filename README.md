# Predicting Gas Station Density Across North Carolina Counties

This repository contains the code and documentation for an econometric and machine learning project conducted as part of **ECON 573 – Machine Learning and Econometrics** at UNC Chapel Hill.

The project explores the extent to which socioeconomic, demographic, and infrastructural variables can predict gas station density across all 100 counties in North Carolina using 2020 data. By applying a wide range of models — from linear regression and variable selection techniques to regularization and non-linear methods — we evaluate which factors most accurately and parsimoniously predict gas station distribution.

### Key modeling approaches:
- Linear regression with VIF-based variable reduction
- Best subset, forward, and backward stepwise selection
- LASSO, Ridge, and Elastic Net regularization
- Principal Components Regression (PCR)
- Natural Splines and Generalized Additive Models (GAMs)
- Regression Trees and Random Forests

### Highlight:
The best-performing model, selected via 10-fold cross-validation, used only **four predictors** and achieved an RMSE of **10.49**, outperforming more complex models. This demonstrates that a compact and interpretable linear model can offer both strong predictive performance and clear insights for infrastructure planning.

---
