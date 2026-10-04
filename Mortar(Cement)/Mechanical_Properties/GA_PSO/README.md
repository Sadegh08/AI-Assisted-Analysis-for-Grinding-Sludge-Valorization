# GA and PSO Analysis of Mortar Mechanical Properties

[Repository overview](../../../README.md) · [Mortar (Cement)](../../README.md)

This folder contains the Genetic Algorithm (GA) and Particle Swarm Optimization (PSO) analysis developed for predicting the mechanical properties of cement mortar mixtures.

## Analysis

GA and PSO are used to optimize the coefficients of empirical models for predicting:

- Maximum flexural stress
- Mean compressive strength

The input variables are:

- Sludge content
- Plasticizer dosage
- Density

## Optimization Method

Second-order empirical equations are optimized using two population-based optimization algorithms:

- Genetic Algorithm (GA)
- Particle Swarm Optimization (PSO)

Each candidate solution represents a possible set of model coefficients, and the optimization objective is minimizing the difference between experimental and predicted values.

The same equation structure, dataset, coefficient bounds, and objective function are used for both optimization methods to enable consistent comparison.

## Validation

The predictive performance of the GA- and PSO-based models is evaluated using Leave-One-Out Cross-Validation (LOOCV).

In each iteration, one observation is held out for testing and the remaining observations are used for model calibration.

## Model Performance

Prediction performance is evaluated using:

- R²
- RMSE
- MAE
- MAPE

Metrics are calculated separately for:

- Maximum flexural stress
- Mean compressive strength

## Input Data

Data file: [Final.xlsx](../Final.xlsx). Upload it to `/content/Final.xlsx` and keep `/content` as the working directory.

The analysis uses the experimental dataset containing:

- Sludge content
- Plasticizer dosage
- Density
- Maximum flexural stress
- Mean compressive strength

## Notebook

The complete GA and PSO analysis is available in:

[GA_and_PSO.ipynb](GA_and_PSO.ipynb)

[Open in Google Colab](https://colab.research.google.com/github/Sadegh08/AI-Assisted-Analysis/blob/main/Mortar%28Cement%29/Mechanical_Properties/GA_PSO/GA_and_PSO.ipynb) · [Execution and reproducibility guide](../../../docs/REPRODUCIBILITY.md)

## Outputs

The notebook generates:

- Optimized empirical model coefficients
- GA prediction results
- PSO prediction results
- LOOCV performance metrics
- Measured-versus-predicted comparisons
- Numerical result export

## Reproducibility

The same dataset, equation structure, optimization objective, and validation framework are applied to both GA and PSO methods.
