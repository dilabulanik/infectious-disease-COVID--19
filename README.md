# COVID-19 Hospitalisation Forecasting — Italian Regions

Short-term ensemble forecasting of COVID-19 hospitalisations across 
Italian regions (September 2021 – March 2023).

## Overview

This project develops and evaluates multiple forecasting models for 
COVID-19 hospitalisations across Italian regions. The best-performing 
models are combined into an ensemble with adaptive weights, updated 
for each prediction window based on recent performance.

## Models Evaluated

- **INGARCH** — stationary, linear, quadratic, and cubic variants
- **GLM** — flexible generalised linear model with cubic splines of time
- **GAM** — generalised additive model with a smooth function of time
- **BSTS** — Bayesian structural time series with linear and seasonal trends
- **ANN** — artificial neural network with 2 hidden layers, 10 repetitions

## Ensemble

The three best-performing models (GAM, BSTS, ANN) were selected for 
the ensemble. Ensemble weights vary by prediction window, assigned 
according to each model's performance in the preceding period.

## Data

Daily hospitalisation data across Italian regions, 
June 2021 – July 2023. Data were cleaned and preprocessed 
with automated pipelines.

## Requirements

- R 
- Packages: nloptr, rms, mgcv, bsts, tscount, fastDummies, neuralnet

## Authors

Dila Bulanik — University of Bologna
Supervisors: Prof. Rossella Miglio, Dr. Anna Vesely
