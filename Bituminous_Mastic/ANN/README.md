# ANN Analysis of Aging Index

[Repository overview](../../README.md) · [Bituminous mastic](../README.md)

This folder contains the Artificial Neural Network (ANN) analysis developed for predicting the Aging Index of bituminous mastics.

## Analysis

The ANN model uses the following input variables:

- Filler type
- Filler-to-bitumen ratio by mass
- Logarithm of angular frequency

The target variable is:

- Aging Index

Filler type is treated as a categorical variable, while the numerical variables are standardized before model training.

## ANN Model

The prediction model is based on a multilayer perceptron neural network.

The hyperparameter search evaluates different:

- Hidden-layer sizes
- Activation functions
- Solvers
- Regularization parameters

## Validation

Model performance is evaluated using Nested Leave-One-Mastic-Out Cross-Validation.

In each outer fold, one complete mastic formulation is held out for evaluation. Hyperparameter selection is performed on the remaining mastics using an inner Leave-One-Mastic-Out cross-validation procedure.

This approach evaluates the ability of the ANN model to predict the Aging Index of an unseen mastic formulation.

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

The complete ANN analysis is available in:

[ANN.ipynb](ANN.ipynb)

[Open in Google Colab](https://colab.research.google.com/github/Sadegh08/AI-Assisted-Analysis-for-Grinding-Sludge-Valorization/blob/main/Bituminous_Mastic/ANN/ANN.ipynb) · [Execution and reproducibility guide](../../docs/REPRODUCIBILITY.md)

## Outputs

The notebook generates:

- Nested Leave-One-Mastic-Out predictions
- Overall prediction metrics
- Individual mastic performance metrics
- Selected ANN hyperparameters
- Actual-versus-predicted plot
- Residual plot
- Experimental-versus-predicted Aging Index curves
- Final trained ANN model
- Excel file containing the numerical results

## Reproducibility

The ANN workflow uses grouped cross-validation based on mastic formulation and a fixed random state.

The final model is selected using grouped Leave-One-Mastic-Out cross-validation on the complete dataset and saved for subsequent use.
