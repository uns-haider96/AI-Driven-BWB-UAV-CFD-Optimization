# Surrogate-Assisted Optimization Workflow

This is pseudocode describing the research workflow. It is not a recovered source-code file.

```text
Define BWB geometric design variables
Define lower and upper bounds for each variable
Generate initial designs using Latin Hypercube Sampling

For each sampled design:
    Generate CAD geometry
    Create CFD mesh
    Run CFD simulation
    Extract CL, CD, L/D, and related outputs

Train regression/surrogate models
Evaluate models using validation metrics
Select Gaussian Process Regression for optimization

For each Bayesian optimization iteration:
    Use GPR to predict L/D across candidate space
    Compute Expected Improvement
    Select candidate with maximum Expected Improvement
    Run high-fidelity CFD for selected candidate
    Add new result to training dataset
    Retrain / update GPR model

Return best design based on validated L/D
Compare baseline and optimized geometry
Proceed to structural assessment and fabrication planning
```
