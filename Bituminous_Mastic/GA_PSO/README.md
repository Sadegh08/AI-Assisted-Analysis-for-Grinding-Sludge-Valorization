# GA–PSO Analysis of Aging Index

[Repository overview](../../README.md) · [Bituminous mastic](../README.md)

This folder contains the Genetic Algorithm (GA) and Particle Swarm Optimization (PSO) analyses developed for estimating the coefficients of an empirical Aging Index model for bituminous mastics.

## Analysis

The notebook independently applies GA and PSO to estimate the coefficients of the Aging Index equation.

The empirical model considers:

- Filler-to-bitumen ratio by weight
- Logarithm of angular frequency
- Quadratic effect of filler-to-bitumen ratio
- Quadratic effect of logarithmic frequency
- Interaction between filler-to-bitumen ratio and logarithmic frequency
- Filler type

Rheofiller is used as the reference filler, while Cement and Chromium steel are represented using dummy variables.

## Empirical Model

The Aging Index is estimated using:

AI = β₀ + β₁(f/b) + β₂log₁₀(ω) + β₃(f/b)² + β₄[log₁₀(ω)]² + β₅(f/b)log₁₀(ω) + β₆D_Cement + β₇D_Chromium

where:

- AI is the Aging Index
- f/b is the filler-to-bitumen ratio by weight
- ω is the angular frequency
- D_Cement is the dummy variable for Cement
- D_Chromium is the dummy variable for Chromium steel

## Optimization Methods

Two optimization methods are applied independently:

- Genetic Algorithm (GA)
- Particle Swarm Optimization (PSO)

Each optimization method is executed over 20 independent runs using predefined random seeds.

The best solution is selected based on the lowest RMSE.

## Model Performance

The optimized models are evaluated using:

- R²
- RMSE
- MAE
- MAPE

The notebook also evaluates optimization stability using the mean, standard deviation, minimum, and maximum RMSE across the independent runs.

## Input Data

Upload the dataset to `/content/Aging index.xlsx` and keep `/content` as the working directory. Follow the execution guide linked below to prepare the runtime.

The analysis uses:

[Aging index.xlsx](../Aging%20index.xlsx)

The dataset contains experimental Aging Index measurements together with filler type, filler-to-bitumen ratio by weight, and angular frequency.

## Notebook

The complete analysis is available in:

[GA_and_PSO.ipynb](GA_and_PSO.ipynb)

[Open in Google Colab](https://colab.research.google.com/github/Sadegh08/AI-Assisted-Analysis/blob/main/Bituminous_Mastic/GA_PSO/GA_and_PSO.ipynb) · [Execution and reproducibility guide](../../docs/REPRODUCIBILITY.md)

## Outputs

The notebook generates:

- Best GA coefficients
- Best PSO coefficients
- GA and PSO performance metrics
- Multi-run optimization statistics
- Final empirical equations
- Experimental and predicted Aging Index values
- Optimization convergence plots
- Measured-versus-predicted plots
- Excel file containing the numerical results

## Reproducibility

The GA and PSO analyses use predefined random seeds for the independent optimization runs, allowing the optimization procedure and results to be reproduced.
