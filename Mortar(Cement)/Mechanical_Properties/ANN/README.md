# ANN Analysis of Mortar Mechanical Properties

[Repository overview](../../../README.md) · [Mortar (Cement)](../../README.md)

This folder contains the Artificial Neural Network (ANN) analysis developed for predicting the mechanical properties of cement mortar mixtures.

## Analysis

The ANN model uses the following input variables:

- Sludge content
- Plasticizer dosage
- Density

The model predicts two target variables simultaneously:

- Maximum flexural stress
- Mean compressive strength

## ANN Model

A multi-output Artificial Neural Network is used to predict both mechanical responses within a single modelling framework.

The input and output variables are standardized before model training.

## Validation

Model performance is evaluated using Leave-One-Out Cross-Validation (LOOCV).

In each iteration, one specimen is held out for testing and the model is trained using the remaining observations.

Hyperparameter selection is performed using grid-search cross-validation.

## Model Performance

Prediction performance is evaluated separately for flexural strength and compressive strength using:

- R²
- RMSE
- MAE
- MAPE

## Input Data

Data file: [Final.xlsx](../Final.xlsx). Upload it to `/content/Final.xlsx` and keep `/content` as the working directory.

The analysis uses the unified experimental dataset containing:

- Sludge content
- Plasticizer dosage
- Density
- Maximum flexural stress
- Mean compressive strength

## Notebook

The complete ANN analysis is available in:

[ANN.ipynb](ANN.ipynb)

[Open in Google Colab](https://colab.research.google.com/github/Sadegh08/AI-Assisted-Analysis-for-Grinding-Sludge-Valorization/blob/main/Mortar%28Cement%29/Mechanical_Properties/ANN/ANN.ipynb) · [Execution and reproducibility guide](../../../docs/REPRODUCIBILITY.md)

## Outputs

The notebook generates:

- LOOCV predictions
- Flexural-strength performance metrics
- Compressive-strength performance metrics
- Selected ANN hyperparameters
- Measured-versus-predicted plots
- Final trained ANN model
- Numerical result export

## Reproducibility

The ANN workflow uses Leave-One-Out Cross-Validation and standardized input and output variables.

The same dataset and modelling framework are used for both mechanical response variables.
