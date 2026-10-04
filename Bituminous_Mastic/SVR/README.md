# SVR Analysis of Aging Index

[Repository overview](../../README.md) · [Bituminous mastic](../README.md)

This folder contains the Support Vector Regression (SVR) analysis developed for predicting the Aging Index of bituminous mastics.

## Analysis

The SVR model uses the following input variables:

- Filler type
- Filler-to-bitumen ratio by mass
- Logarithm of angular frequency

The target variable is:

- Aging Index

Filler type is treated as a categorical variable, while the numerical variables are standardized before model training.

## SVR Model

Support Vector Regression is used to model the relationship between mastic composition, frequency, and Aging Index.

The hyperparameter search evaluates different kernel functions, including:

- Linear
- Radial Basis Function (RBF)
- Polynomial

The search also evaluates different values of model parameters such as C, epsilon, gamma, polynomial degree, and coef0 where applicable.

## Validation

Model performance is evaluated using Nested Leave-One-Mastic-Out Cross-Validation.

In each outer fold, one complete mastic formulation is held out for independent evaluation.

Hyperparameter selection is performed on the remaining mastics using an inner Leave-One-Mastic-Out cross-validation procedure.

This approach evaluates the ability of the SVR model to predict the Aging Index of an unseen mastic formulation.

## Model Performance

Prediction performance is evaluated using:

- R²
- RMSE
- MAE
- MAPE
- sMAPE

Metrics are calculated for the complete set of held-out predictions and for individual mastic formulations.

## Input Data

Upload the dataset to `/content/Aging index.xlsx` and keep `/content` as the working directory. Follow the execution guide linked below to prepare the runtime.

The analysis uses:

[Aging index.xlsx](../Aging%20index.xlsx)

## Notebook

The complete SVR analysis is available in:

[SVR.ipynb](SVR.ipynb)

[Open in Google Colab](https://colab.research.google.com/github/Sadegh08/AI-Assisted-Analysis-for-Grinding-Sludge-Valorization/blob/main/Bituminous_Mastic/SVR/SVR.ipynb) · [Execution and reproducibility guide](../../docs/REPRODUCIBILITY.md)

## Outputs

The notebook generates:

- Nested Leave-One-Mastic-Out predictions
- Overall prediction metrics
- Individual mastic performance metrics
- Selected SVR hyperparameters
- Grouped grid-search results
- Actual-versus-predicted plot
- Residual plot
- Experimental-versus-predicted Aging Index curves
- Final trained SVR model
- Excel file containing the numerical results

## Reproducibility

The SVR workflow uses grouped cross-validation based on mastic formulation.

The final SVR model is selected using grouped Leave-One-Mastic-Out cross-validation on the complete dataset and saved for subsequent use.
