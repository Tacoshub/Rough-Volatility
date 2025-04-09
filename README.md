# Rough Volatility Project (2025)

This repository contains the implementation and results of the Rough Volatility Project, focusing on simulation, estimation, and pricing within the Lifted Heston and Lifted Bergomi models. The work explores volatility modeling with a special emphasis on the approximation of rough volatility using finite-dimensional Markovian models.

## Contents

### 1. Estimation of the Hurst Parameter

We simulate the variance process in the Lifted Heston model and estimate the Hurst parameter $H$ using a two-step regression on log-increments of log-variance. Estimation is benchmarked against:

- Brownian motion (benchmark: $H = 0.5$)
- Fractional Brownian motion (benchmark: $H = 0.1$)

For each case, subsampling effects on the estimation accuracy are investigated.

### 2. Implied Volatility in the Lifted Heston Model

- Derivation of the moment generating function $M_t$
- Carr-Madan pricing formula implementation
- Fourier-based pricing via characteristic function approximated through Riccati ODEs
- Smile generation for different factor counts $n$ and maturities

### 3. Implied Volatility in the Lifted Bergomi Model

A multi-factor approximation of the rough Bergomi model is implemented. Monte Carlo simulations are used to compute call prices and implied volatilities.

### 4. Model Calibration

- Calibration of the classical Heston model to SPX call options
- Comparison with the Lifted Heston model on the same dataset
- Assessment of fit quality both in prices and implied volatilities

## Notable Techniques and Concepts

- **Lifted Heston Model**: Markovian approximation of the rough Heston model
- **Hurst Estimation**: Regression on structure functions of log-variance increments
- **Fourier Pricing**: Carr-Madan formula using characteristic functions
- **Multi-Factor Approximation**: Kernel fitting via Laplace transforms
- **Monte Carlo Simulation**: Used for Lifted Bergomi pricing

## Authors

- Flavio Boccia  
- Ludovico Costa  
- Alessandro Pigato  
- Lorenzo Tolomelli
