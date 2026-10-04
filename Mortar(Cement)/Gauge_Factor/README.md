# Mortar Gauge Factor – AI-Assisted Analysis

[Repository overview](../../README.md) · [Mortar (Cement)](../README.md)

This folder contains the AI-assisted analysis developed for predicting the average final gauge factor (GFend) of cement mortar mixtures.

## Analysis

The predictive models use the following input variables:

- Sludge content
- Plasticizer dosage

The target variable is:

- Average final gauge factor (GFend)

## Interpolation

The original experimental dataset contains nine distinct mixture conditions.

Two interpolation methods are applied to generate intermediate representations between consecutive experimental conditions:

- Piecewise Cubic Hermite Interpolating Polynomial (PCHIP)
- Akima interpolation

Each interpolation method generates eight intermediate points, resulting in a dataset containing 17 observations:

- 9 original observations
- 8 interpolated observations

The interpolated points are numerical estimates and are not treated as additional experimental measurements.

## Machine Learning Models

Three nonlinear regression models are evaluated:

- Artificial Neural Network (ANN)
- Gaussian Process Regression (GPR)
- Support Vector Regression (SVR)

Model hyperparameters are optimized separately for the PCHIP and Akima datasets.

## Validation

Model performance is evaluated using Nested Leave-One-Out Cross-Validation (LOOCV).

In each outer fold, one observation is held out for evaluation.

Hyperparameter selection is performed on the remaining observations using an inner Leave-One-Out Cross-Validation procedure.

## Model Performance

Prediction performance is evaluated using:

- R²
- RMSE
- MAE
- MAPE

MAPE is calculated after excluding observations with a measured GFend equal to zero to avoid division by zero.

The complete model-performance results are provided in the notebook.

## Model Interpretation

SHAP analysis is applied to the PCHIP–GPR model to evaluate the contribution of:

- Sludge content
- Plasticizer dosage

The SHAP results are used to interpret model behavior rather than causal relationships.

## Input Data

The numerical input data are defined in the notebook. No external Excel input is required; run the notebook cells in their existing order.

The analysis uses nine averaged experimental mixture conditions containing:

- Sludge content
- Plasticizer dosage
- Average GFend

## Notebook

The complete analysis is available in:

[GFend.ipynb](GFend.ipynb)

[Open in Google Colab](https://colab.research.google.com/github/Sadegh08/AI-Assisted-Analysis/blob/main/Mortar%28Cement%29/Gauge_Factor/GFend.ipynb) · [Execution and reproducibility guide](../../docs/REPRODUCIBILITY.md)

## Outputs

The notebook generates:

- PCHIP and Akima interpolated datasets
- ANN, GPR, and SVR predictions
- Optimized model configurations
- Nested LOOCV performance metrics
- Model comparison results
- Measured-versus-predicted plots
- SHAP interpretation

## Reproducibility

The same modeling and validation framework is applied separately to the PCHIP and Akima datasets.

Nested Leave-One-Out Cross-Validation is used to keep model evaluation separate from hyperparameter selection.
