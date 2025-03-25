# SIR Model Calibration using Maximum Likelihood Estimation (MLE)

This repository contains an R script for calibrating an SIR (Susceptible-Infectious-Recovered) epidemiological model to flu outbreak data using Maximum Likelihood Estimation (MLE). The model accounts for underreporting and visualizes the fit to both reported and total infection cases.

## Overview
- **Objective**: Estimate transmission (`beta`) and recovery (`gamma`) rates of the SIR model by fitting it to reported flu case data.
- **Key Features**:
  - Poisson log-likelihood function for MLE.
  - Optimization of model parameters (`beta` and `gamma`).
  - Visualization of model fit against real-world data.
- **Data**: Includes reported and total infection counts from a flu outbreak.

## Dependencies
- R (version 3.5.1 or later)
- R packages:
  - `deSolve` (for ODE integration)
  - `ggplot2` (for plotting)
  - `stats` (for optimization)

## Usage
1. **Load Data**: The script reads flu case data from `Graphics_and_Data/idm2_sir_data.csv`.
2. **Define Model**: The SIR model is implemented as a system of ODEs.
3. **MLE Calibration**: The `optim` function maximizes the log-likelihood to estimate parameters.
4. **Visualization**: The fitted model is plotted against the observed data.

## Results
- Estimated parameters: `beta = 1.69`, `gamma = 0.48`.
- The model provides a good fit to both reported and total infections, demonstrating its utility for outbreak prediction.

## Files
- `Performing_Maximum_Likelihood_Estimation.ipynb`: R script with code and outputs.
- `Graphics_and_Data/idm2_sir_data.csv`: Dataset used for calibration.

