# Start Here for Reviewers

This file is for professors, research supervisors, scholarship committees, recruiters, and technical reviewers who want to evaluate the project quickly.

## 1. What This Project Demonstrates

This project demonstrates an end-to-end aerospace engineering workflow for a one-meter blended-wing-body UAV:

- Conceptual aircraft design
- Parametric CAD modeling
- CFD-based aerodynamic analysis
- Machine-learning surrogate modeling
- Gaussian Process Regression
- Bayesian design optimization
- Composite fabrication and prototype manufacturing
- FEA-informed structural assessment
- Wind tunnel testing
- Peer-reviewed journal publication record
- Conference presentation record

## 2. Most Important Evidence

| Evidence | Location |
|---|---|
| Official journal publication | `README.md` and `PUBLICATION.md` |
| DOI and SAGE screenshot | `assets/figures/publication/` and `docs/publication/` |
| IBCAST certificate and presentation | `docs/conference/` |
| Final CAD geometry | `assets/figures/cad/` |
| CFD mesh, pressure, Mach, and velocity visuals | `assets/figures/cfd/` |
| Optimization convergence | `assets/figures/optimization/` |
| Design-space and model-comparison figures | `assets/figures/design-space/` and `assets/figures/surrogate-models/` |
| Manufacturing and wind tunnel images | `assets/figures/manufacturing/` and `assets/figures/wind-tunnel/` |
| Baseline vs optimized table | `results/baseline-vs-optimized.md` |
| Complete methodology | `methodology/` |

## 3. Core Technical Result

The optimized UAV design improved lift-to-drag ratio from approximately **9.9** to **12.2**, corresponding to an approximate **23% aerodynamic-efficiency improvement**.

## 4. Recommended Review Order

1. Read `README.md`.
2. Check `PUBLICATION.md` for DOI and authorship.
3. Review `results/baseline-vs-optimized.md`.
4. Review `methodology/03-cfd-methodology.md` and `methodology/05-bayesian-optimization.md`.
5. Review `methodology/06-composite-fabrication.md` and `methodology/07-wind-tunnel-testing.md`.
6. Browse `assets/figures/cfd/`, `assets/figures/manufacturing/`, and `assets/figures/wind-tunnel/`.
7. Open `docs/conference/` for IBCAST certificate and presentation material.

## 5. Repository Scope

This repository is built as a professional research portfolio. It emphasizes documentation, figures, methodology, publication evidence, and technical interpretation.

Original solver files, editable CAD files, raw scripts, journal manuscript files, publisher-formatted PDFs, and the conference paper PDF are not included in this public release.
