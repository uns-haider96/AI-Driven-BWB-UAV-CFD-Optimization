# Bayesian Optimization

## Objective

The optimization objective was to maximize the UAV lift-to-drag ratio at the target cruise-design condition.

## Method

The optimization used a surrogate-assisted Bayesian optimization workflow:

1. Generate initial design candidates using Latin Hypercube Sampling.
2. Evaluate candidates with CFD.
3. Train a Gaussian Process Regression surrogate model.
4. Use Expected Improvement to select promising new candidates.
5. Validate selected candidates with high-fidelity CFD.
6. Update the surrogate and repeat until improvement converges.

## Optimization result

The best observed lift-to-drag ratio improved from approximately **9.9** to approximately **12.2**, corresponding to an approximate **23% increase** in aerodynamic efficiency.

## Figure

`assets/figures/optimization/bayesian-optimization-convergence.png`

This figure shows the increase in best observed L/D and the reduction in Expected Improvement as the optimization process converged.
