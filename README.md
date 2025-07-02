# Predicting Gas Station Density Across North Carolina Counties

This repository contains the code and documentation for an econometric and machine learning project conducted as part of ECON 573 – Machine Learning and Econometrics at UNC Chapel Hill.

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
