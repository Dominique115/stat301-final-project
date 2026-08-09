# Predicting Restaurant Tip Percentage — STAT 301 Final Project

**Course**: STAT 301 — Statistical Modelling for Data Science  
**Team**: Group 3  
**Report**: [View Final Report](https://dominique115.github.io/stat301-final-project/)

## Research Question

> How are dining party size, the gender of the person paying, smoker status, time of day, and day of the week associated with the tip percentage of a customer's bill at a popular restaurant?

## Dataset

- **Source**: Restaurant tips dataset (Kaggle — Badole, S., 2024)
- **Size**: 244 unique transactions
- **Response variable**: `tip_percentage` = (tip / total_bill) × 100
- **Predictors**: `sex`, `smoker`, `day`, `time`, `size` (party size)

## Methods

| Step | Detail |
|------|--------|
| Variable selection | Forward selection guided by adjusted R² and p-values |
| Final model | Multiple Linear Regression (MLR) with `sex` and `day` |
| Rationale | Low-dimensional setting; forward selection balances interpretability and prevents overfitting on 244 observations |

## Key Findings

- The final model retained **sex** and **day of the week** as predictors after forward selection.
- The model explained only **~0.6% of variance** in tip percentage; neither predictor reached statistical significance.
- Demographic and contextual variables have **limited explanatory power** for tipping behavior in this dataset.
- Tipping appears driven by factors not captured here — service quality, customer mood, income, or cultural norms.

## Limitations & Future Directions

- Expand features: service ratings, customer income, bill type, interaction terms
- Explore non-linear models or regularization (LASSO/Ridge) to capture complex patterns
- Increase sample size beyond 244 observations for more reliable inference

## Repository Structure

```
stat301-final-project/
├── final_project.ipynb   # Source Jupyter notebook
├── final_project.html    # Rendered report (served via GitHub Pages)
└── README.md
```
