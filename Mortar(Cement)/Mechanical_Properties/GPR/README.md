# GPR Analysis of Mortar Mechanical Properties

[Repository overview](../../../README.md) · [Mortar (Cement)](../../README.md)

This folder contains the Gaussian Process Regression (GPR) analysis developed for predicting the mechanical properties of cement mortar mixtures.

## Analysis

The GPR models use the following input variables:

- Sludge content
- Plasticizer dosage
- Density

Two mechanical responses are predicted separately:

- Maximum flexural stress
- Mean compressive strength

## GPR Model

Gaussian Process Regression models are developed using different kernel functions:

- Radial Basis Function (RBF)
- Matérn
- Rational Quadratic

Separate GPR models are trained for flexural strength and compressive strength prediction.

## Validation

Model performance is evaluated using Leave-One-Out Cross-Validation (LOOCV).

In each iteration, one observation is used as the test sample and the remaining observations are used for model training.

## Model Performance

Prediction performance is evaluated using:

- R²
- RMSE
- MAE
- MAPE

The performance metrics are calculated separately for flexural strength and compressive strength.

## Input Data

Data file: [Final.xlsx](../Final.xlsx). Upload it to `/content/Final.xlsx` and keep `/content` as the working directory.

The analysis uses the experimental dataset containing:

- Sludge content
- Plasticizer dosage
- Density
- Maximum flexural stress
- Mean compressive strength

## Notebook

The complete GPR analysis is available in:

[GPR.ipynb](GPR.ipynb)

[Open in Google Colab](https://colab.research.google.com/github/Sadegh08/AI-Assisted-Analysis/blob/main/Mortar%28Cement%29/Mechanical_Properties/GPR/GPR.ipynb) · [Execution and reproducibility guide](../../../docs/REPRODUCIBILITY.md)

## Outputs

The notebook generates:

- Kernel comparison results
- LOOCV predictions
- Flexural strength performance metrics
- Compressive strength performance metrics
- Measured-versus-predicted plots
- Selected GPR models
- Numerical result export

## Reproducibility

The GPR workflow applies the same dataset and validation framework for both mechanical response variables.

Leave-One-Out Cross-Validation is used to evaluate the generalization performance of the models.
