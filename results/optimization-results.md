# Optimization Results

## Bayesian optimization outcome

The Bayesian optimization process improved the best observed lift-to-drag ratio from approximately **9.9** to **12.2**.

## Convergence figure

![Bayesian optimization convergence](../assets/figures/optimization/bayesian-optimization-convergence.png)

## Engineering interpretation

The blue curve shows the improvement in the best observed L/D as the optimizer searched the design space. The Expected Improvement curve decreases as the optimizer converges, indicating that the model gradually identified the strongest design region.

## Why Bayesian optimization was suitable

Bayesian optimization is suitable for CFD-driven design because every high-fidelity simulation is expensive. Instead of testing every possible design, the surrogate model guides the search toward promising candidates and balances exploration with exploitation.
