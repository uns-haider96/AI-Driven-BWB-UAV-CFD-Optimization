# Surrogate Modeling

## Purpose

High-fidelity CFD simulations are computationally expensive. Surrogate modeling was used to approximate aerodynamic/performance outputs from geometric design variables, allowing rapid exploration of candidate designs.

## Inputs

The surrogate-model workflow used geometric design variables such as:

- Root chord
- Tip chord
- Sweep angle
- Taper ratio
- Wing twist
- Winglet cant angle
- Winglet sweep angle
- Winglet chord dimensions

## Outputs

Performance-related outputs included quantities such as:

- Lift-to-drag ratio
- Drag coefficient
- Power-related performance metrics
- Mass/structural estimates where available

## Models evaluated

The project evaluated multiple regression approaches, including:

- Multiple Linear Regression
- Support Vector Regression
- Random Forest Regression
- K-Nearest Neighbors Regression
- Multi-Layer Perceptron neural networks
- Gaussian Process Regression

## Final optimization model

Gaussian Process Regression was selected for the final optimization workflow because it provides both prediction and uncertainty estimation. This makes it suitable for Expected Improvement-based Bayesian optimization.

## Model-comparison figures

The repository includes model-comparison plots in:

`assets/figures/surrogate-models/`

These figures are useful for showing model selection and diagnostic comparison across different predicted quantities. They should be interpreted as part of the model-selection process rather than as a claim that all models performed equally well.
