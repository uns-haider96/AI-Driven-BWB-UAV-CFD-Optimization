# Surrogate Model Results

## Purpose

The surrogate-model comparison was performed to evaluate how different regression techniques captured performance trends from the sampled design data.

## Figures included

| Figure | File |
|---|---|
| Performance model comparison | `assets/figures/surrogate-models/model-comparison-performance.png` |
| Primary power-prediction comparison | `assets/figures/surrogate-models/power-prediction-model-comparison-primary.png` |
| Secondary power-prediction comparison | `assets/figures/surrogate-models/power-prediction-model-comparison-secondary.png` |
| MTOW model comparison | `assets/figures/surrogate-models/mtow-prediction-model-comparison.png` |
| Payload-capacity model comparison | `assets/figures/surrogate-models/payload-capacity-model-comparison.png` |
| Wing-span diagnostic comparison | `assets/figures/surrogate-models/wing-span-model-comparison.png` |

## Interpretation

The comparison figures show that different models performed differently depending on the target quantity. This is expected in small-data engineering problems because aerodynamic, structural, and mass-related responses have different levels of nonlinearity and sensitivity to the available features.

The final optimization workflow emphasizes Gaussian Process Regression because it provides uncertainty estimates required for Expected Improvement-based Bayesian optimization.
