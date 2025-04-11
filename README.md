# Rough Volatility Project (2025)

This repository contains the implementation and numerical results of a project on rough volatility models, with a particular focus on simulation, estimation, pricing, and calibration techniques for the Lifted Heston and Lifted Bergomi models.

The project investigates the approximation of rough volatility dynamics using finite-dimensional Markovian systems, enabling efficient numerical methods for option pricing and model calibration.

---

## Contents

### 1. Estimation of the Hurst Parameter

We simulate the variance process in the Lifted Heston model and estimate the Hurst parameter $H$ using a regression-based method on log-increments of log-variance. Estimation accuracy is assessed for:

- Brownian motion ($H = 0.5$)
- Fractional Brownian motion ($H = 0.1$)

We also study the impact of subsampling on the estimation procedure.

---

### 2. Implied Volatility in the Lifted Heston Model

- Derivation of the moment generating function
- Fourier-based pricing via the Carr-Madan formula
- Numerical solution of Riccati ODEs for the characteristic function
- Generation of implied volatility smiles across different numbers of factors and maturities

---

### 3. Implied Volatility in the Lifted Bergomi Model

A multi-factor approximation of the rough Bergomi model is implemented. Call prices and implied volatilities are computed using Monte Carlo simulation, investigating the effect of the number of factors on the accuracy of the smile.

---

### 4. Model Calibration

We perform a calibration of both the classical Heston model and the Lifted Heston model to SPX option data. The fit quality is evaluated in terms of both option prices and implied volatilities.

---

## Main Techniques

- Simulation of variance processes using implicit-explicit Euler schemes
- Estimation of roughness via structure functions of log-variance increments
- Fourier pricing methods based on characteristic functions
- Multi-factor kernel approximation of rough volatility models
- Monte Carlo methods for option pricing
- Calibration procedures for volatility models

---

## Authors

- Flavio Boccia  
- Ludovico Costa  
- Alessandro Pigato  
- Lorenzo Tolomelli
