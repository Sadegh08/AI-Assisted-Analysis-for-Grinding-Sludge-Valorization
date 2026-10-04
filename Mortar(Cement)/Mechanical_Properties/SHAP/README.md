# SHAP Analysis of Mortar Mechanical Properties

[Repository overview](../../../README.md) · [Mortar (Cement)](../../README.md)

This folder contains the SHAP (SHapley Additive exPlanations) analysis developed for interpreting the Gaussian Process Regression (GPR) models used for predicting the mechanical properties of cement mortar mixtures.

## Analysis

SHAP is applied to explain the contribution of input variables to the predictions of GPR models.

The interpreted input variables are:

- Sludge content
- Plasticizer dosage
- Density

The analysed target responses are:

- Maximum flexural stress
- Mean compressive strength

## SHAP Method

Kernel SHAP is used to calculate feature contributions for the GPR predictions.

Separate SHAP analyses are performed for:

- Flexural strength prediction
- Compressive strength prediction

## Model Interpretation

The SHAP analysis provides:

- Feature contribution values
- Global feature importance based on mean absolute SHAP values
- Summary plots showing the effect of input variables on model predictions

The SHAP results describe the behaviour of the trained GPR models and do not represent direct causal relationships.

## Input Data

Data file: [Final.xlsx](../Final.xlsx). Upload it to `/content/Final.xlsx` and keep `/content` as the working directory.

The analysis uses the experimental dataset containing:

- Sludge content
- Plasticizer dosage
- Density
- Maximum flexural stress
- Mean compressive strength

## Notebook

The complete SHAP analysis is available in:

[SHAP_GPR.ipynb](SHAP_GPR.ipynb)

[Open in Google Colab](https://colab.research.google.com/github/Sadegh08/AI-Assisted-Analysis/blob/main/Mortar%28Cement%29/Mechanical_Properties/SHAP/SHAP_GPR.ipynb) · [Execution and reproducibility guide](../../../docs/REPRODUCIBILITY.md)

## Outputs

The notebook generates:

- SHAP values for flexural strength
- SHAP values for compressive strength
- Feature importance analysis
- SHAP summary plots
- Numerical SHAP result export

## Reproducibility

This notebook fits the GPR models used for interpretation within its own workflow. It requires `Final.xlsx` and does not load a saved model from the separate GPR notebook.

The same input variables and dataset are used for interpretation of both mechanical responses.
