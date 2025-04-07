# Rough Volatility Project 2025

This repository contains the implementation and results for the **"Rough Volatility Models"** project.

Group members:
- Flavio Boccia
- Ludovico Costa
- Alessandro Pigato
- Lorenzo Tolomelli

---

## Project Description

The objective of this project is to explore the modeling, simulation, and pricing implications of rough volatility in financial markets. In particular, we study the Lifted Heston and Lifted Bergomi models, which aim to replicate the observed irregularity and short-memory effects in volatility time series while preserving tractability.

The project is structured in three main parts. In the first part, we focus on the estimation of the Hurst parameter \( H \), which characterizes the roughness of the volatility path. We simulate a variance trajectory under the Lifted Heston model, estimate \( H \) via scaling properties of log-increments, and compare the outcome with benchmark processes such as standard Brownian motion and fractional Brownian motion. We also investigate the effect of subsampling on the accuracy of the estimation.

The second part is dedicated to the pricing of European options in the Lifted Heston model. We demonstrate that a specific exponential transform of the log-price, augmented with auxiliary factors, defines a local martingale. We then implement a pricing algorithm based on Fourier methods using the characteristic function derived from the model. Numerical results illustrate how the implied volatility smile evolves as the number of factors increases, both for long and short maturities.

In the third part, we turn our attention to the Lifted Bergomi model. We approximate the fractional kernel by a sum of exponentials and simulate the model using an Euler scheme. European option prices are computed using Monte Carlo methods, and implied volatility smiles are obtained for different configurations of the model parameters. The results confirm the model's ability to generate steep skews and capture realistic features of implied volatility surfaces.

All simulations and numerical analyses are implemented in Python.
