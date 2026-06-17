# Sparse Orthogonal Regression Technique

This repository contains code used to reproduce the experiments in the paper

**“Sparse Orthogonal Regression Technique: A Spectral Framework for Equation Discovery, Approximation, and Integration.”**

The paper develops the Sparse Orthogonal Regression Technique (SORT), a sparse spectral workflow for learning orthonormal expansion coefficients from sampled data and reusing them for dynamical-system reconstruction, numerical integration, and nonlinear approximation.

## Structure

The experiments are organized as Jupyter notebooks corresponding to the main experimental applications in the paper.

3.1 Equation discovery.ipynb
3.2 Integral estimation.ipynb
3.3 Spectral recovery and approximation.ipynb

The notebooks reproduce the following figures:

Figure 1  Lotka--Volterra sampling-degradation experiment
Figure 2  Thomas and Bessel-driven equation-discovery experiments
Figure 3  Integral estimation by coefficient readout
Figure 4  Spectral recovery and order-consistent approximation

## Experiment overview

### Equation discovery

The equation-discovery notebook compares SORT with SINDy-style sparse identification baselines on dynamical systems learned from time-series data.

It includes:

- Lotka--Volterra sampling degradation using finite-difference derivatives.
- Thomas attractor experiments under noise and subsampling.
- Bessel-driven cyclic dynamics testing representation mismatch.

### Integral estimation

The integral-estimation notebook evaluates SORT as a data-driven integral estimator. The method learns a sparse orthonormal expansion from pointwise samples and estimates the integral by reading off the coefficient associated with the integration functional.

The experiments include:

- one-dimensional Fresnel-type integrals,
- one-dimensional Gaussian integrals,
- higher-dimensional separable Fresnel-type integrals,
- higher-dimensional Gaussian integrals.

### Spectral recovery and approximation

The spectral-recovery and approximation notebook studies how sparse orthogonal expansions behave under noise, subsampling, and increasing model order.

It includes:

- recovery of the known Fourier sine coefficient decay for `f(x) = x` on `[-pi, pi]`,
- approximation of `f(x1, x2) = exp(x1 cos(2 x2))` on `[-1, 5]^2`,
- comparisons with OLS, RBF ridge regression, random Fourier features, and gradient boosting.

## Requirements

The notebooks use standard Python scientific-computing libraries, including:

numpy
scipy
scikit-learn
matplotlib

## Usage

Open the notebooks in Jupyter or JupyterLab and run the cells sequentially to reproduce the experiments and figures.

Generated figures are saved by the notebooks in their corresponding output directories.

## Review status

This repository is provided for anonymous peer review. Additional documentation, cleanup, and citation information will be added after publication.
