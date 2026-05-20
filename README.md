# AI-Driven BWB UAV CFD Optimization

![Project Preview](assets/figures/social-preview.png)

## Design and Optimization of a Blended Wing Body UAV Using AI-Driven Surrogate Modeling and CFD Analysis

This repository presents a complete research portfolio for the design, CFD analysis, AI-assisted aerodynamic optimization, composite manufacturing, and wind tunnel testing of a **1-meter blended wing body (BWB) unmanned aerial vehicle (UAV)**.

The project was developed as a Final Year Design Project in Mechanical Engineering and later resulted in a peer-reviewed journal publication in the **Proceedings of the Institution of Mechanical Engineers, Part G: Journal of Aerospace Engineering**.

---

## Project Summary

The objective of this research was to improve the aerodynamic efficiency and endurance potential of a small-scale BWB UAV operating under low-power propulsion constraints.

The project combined:

- Blended wing body UAV design
- CAD modeling and geometry refinement
- High-fidelity CFD simulations
- Latin Hypercube Sampling for design-space exploration
- Surrogate modeling for rapid aerodynamic prediction
- Gaussian Process Regression
- Bayesian optimization
- Composite airframe manufacturing
- Finite Element Analysis-based structural validation
- Prototype fabrication
- Wind tunnel testing

This repository is organized as a public-facing engineering research portfolio for reviewers, professors, recruiters, and researchers interested in UAV design, CFD, and AI-driven aerodynamic optimization.

---

## Final UAV Geometry

![Final BWB UAV CAD Model](assets/figures/cad/final-bwb-uav-cad-model.png)

The final UAV configuration is a 1-meter blended wing body platform designed for improved aerodynamic efficiency and low-power endurance-oriented operation.

### Final Design Parameters

| Parameter | Value |
|---|---:|
| Wingspan | 1.0 m |
| Root chord | 0.30 m |
| Tip chord | 0.15 m |
| Sweep angle | 30° |
| Taper ratio | 0.50 |
| Wing twist | -2° |
| Aspect ratio | 7 |
| Winglet root chord | 0.11 m |
| Winglet tip chord | 0.05 m |
| Winglet cant angle | 15° |
| Winglet sweep angle | 20° |
| Root/center airfoil | Selig S1223 |
| Mid airfoil | NACA 1408 |
| Wing airfoil | NACA 0012 |

---

## Key Research Contribution

The core contribution of this work is an end-to-end workflow for improving the aerodynamic performance of a small BWB UAV using CFD-driven AI optimization and experimental prototype validation.

```text
CAD Geometry
    ↓
CFD Simulation
    ↓
Design-Space Sampling
    ↓
Surrogate Modeling
    ↓
Bayesian Optimization
    ↓
Optimized UAV Geometry
    ↓
Composite Manufacturing
    ↓
FEA / Structural Checks
    ↓
Wind Tunnel Testing
```

---

## Optimization Result

The Bayesian optimization process improved the aerodynamic efficiency of the UAV by increasing the lift-to-drag ratio.

| Metric | Baseline Design | Optimized Design |
|---|---:|---:|
| Lift coefficient, CL | 0.330 | 0.365 |
| Drag coefficient, CD | 0.0335 | 0.0300 |
| Lift-to-drag ratio, L/D | 9.9 | 12.2 |
| Improvement in L/D | — | ~23% |

![Bayesian Optimization Convergence](assets/figures/optimization/bayesian-optimization-convergence.png)

The optimization curve shows the best observed lift-to-drag ratio increasing from approximately **9.9** to approximately **12.2**, while the Expected Improvement criterion decreases as the optimizer converges.

---

## Design-Space Exploration

Latin Hypercube Sampling was used to explore the BWB UAV design space. The dataset included geometric variables such as root chord, tip chord, sweep angle, taper ratio, wing twist, winglet cant angle, winglet sweep angle, and winglet chord parameters.

### Sampled Parameter Distributions

![LHS Parameter Histograms](assets/figures/design-space/lhs-parameter-histograms.png)

### Pair Plot of Sampled Design Parameters

![Design Parameter Pair Plot](assets/figures/design-space/design-parameter-pairplot.png)

### Correlation Analysis

![Correlation Coefficient Heatmap](assets/figures/design-space/correlation-coefficient-heatmap.png)

![P-Value Heatmap](assets/figures/design-space/p-value-heatmap.png)

The correlation and p-value heatmaps indicate that most sampled variables were weakly correlated, supporting the space-filling behavior of the design-space sampling strategy.

---

## Surrogate Modeling

Several regression models were evaluated as preliminary surrogate models for aerodynamic and performance-related prediction tasks.

The tested models included:

- Multiple Linear Regression
- Support Vector Regression
- Random Forest Regression
- K-Nearest Neighbors Regression
- Multi-Layer Perceptron models
- Gaussian Process Regression

![Model Comparison](assets/figures/surrogate-models/model-comparison-performance.png)

The preliminary regression models showed mixed performance depending on the target variable. For the final optimization loop, **Gaussian Process Regression** was selected because it provides both predictive capability and uncertainty estimates, making it suitable for Expected Improvement-based Bayesian optimization.

---

## CFD Methodology

CFD simulations were performed using ANSYS Fluent to evaluate aerodynamic behavior around the BWB UAV geometry.

The CFD work included:

- 3D external-flow simulation
- Pressure-based solver
- SST k-omega turbulence model
- Pressure-farfield boundary conditions
- Mesh refinement around the UAV body and wake region
- Static pressure, Mach number, X-velocity, and velocity-vector visualization

### Mesh

![Volume Mesh](assets/figures/cfd/mesh/volume-mesh.png)

![Wing Surface Mesh](assets/figures/cfd/mesh/wing-surface-mesh.png)

The high-speed CFD visualization case used a mesh of approximately **1.29 million cells**, with local refinement around the UAV surface and wake region.

### Static Pressure Contours

![Static Pressure Lower Surface](assets/figures/cfd/pressure/static-pressure-lower-surface.png)

![Static Pressure Upper Surface](assets/figures/cfd/pressure/static-pressure-upper-surface.png)

The static pressure contours show pressure differences between upper and lower surfaces, indicating lift-generating behavior over the BWB geometry.

### Mach Number Contours

![Mach Contour Root Section](assets/figures/cfd/mach-contours/mach-contour-root-section.png)

![Mach Contour Mid Section](assets/figures/cfd/mach-contours/mach-contour-mid-section.png)

![Mach Contour Tip Section](assets/figures/cfd/mach-contours/mach-contour-tip-section.png)

The Mach number contours show acceleration over the wing-body surface and wake development behind the trailing edge.

### Velocity Vector Fields

![Velocity Vector Root Section](assets/figures/cfd/velocity-vectors/velocity-vector-root-section.png)

![Velocity Vector Mid Section](assets/figures/cfd/velocity-vectors/velocity-vector-mid-section.png)

![Velocity Vector Tip Section](assets/figures/cfd/velocity-vectors/velocity-vector-tip-section.png)

The root section shows stronger three-dimensional flow interaction near the blended body region, which is an important aerodynamic design area for BWB aircraft.

---

## Manufacturing and Wind Tunnel Testing

The optimized UAV was not limited to numerical simulation. A physical prototype was manufactured and tested.

The manufacturing and testing process included:

- CAD-based mold design
- 3D printed matched mold tooling
- Mold sanding and surface preparation
- Carbon fiber/epoxy composite layup
- Vacuum-assisted fabrication process
- Demolding and trimming
- Prototype assembly
- Wind tunnel mounting
- Lift, drag, side force, pitch, yaw, and roll measurement

![Manufacturing and Wind Tunnel Validation](assets/figures/manufacturing-wind-tunnel-validation-collage.jpg)

### 3D Printed Mold Tooling

![Mold 3D Printing Full View](assets/figures/manufacturing/01-mold-3d-printing-full-view.jpg)

![Mold 3D Printing Closeup](assets/figures/manufacturing/02-mold-3d-printing-closeup.jpg)

### Mold Assembly and Preparation

![Assembled Mold Halves](assets/figures/manufacturing/03-assembled-3d-printed-mold-halves.jpg)

![Mold Closeup](assets/figures/manufacturing/04-assembled-mold-closeup.jpg)

![Prepared Mold Top View](assets/figures/manufacturing/05-mold-sanded-and-prepared-top-view.jpg)

![Prepared Mold Closeup](assets/figures/manufacturing/06-mold-sanded-and-prepared-closeup.jpg)

### Composite Airframe

![Carbon Fiber Composite Airframe](assets/figures/manufacturing/07-carbon-fiber-composite-airframe-and-winglet.jpg)

![Composite Airframe Side View](assets/figures/manufacturing/08-composite-airframe-side-view.jpg)

### Carbon Fiber Layup

![Carbon Fiber Layup in Mold](assets/figures/manufacturing/09-carbon-fiber-layup-in-mold.jpg)

![Carbon Fiber Layup Second View](assets/figures/manufacturing/10-carbon-fiber-layup-mold-second-view.jpg)

### Wind Tunnel Testing

![Wind Tunnel Results](assets/figures/wind-tunnel/01-wind-tunnel-force-and-moment-results.jpg)

![Wind Tunnel Mounted Prototype](assets/figures/wind-tunnel/02-wind-tunnel-mounted-prototype-test-setup.png)

The wind tunnel testing provided experimental support and prototype-level aerodynamic characterization. The results include lift, drag, side force, pitch, yaw, and roll behavior across multiple test cases.

---

## Repository Structure

```text
AI-Driven-BWB-UAV-CFD-Optimization/
│
├── README.md
├── START_HERE_FOR_REVIEWERS.md
├── PUBLICATION.md
├── CITATION.cff
├── LICENSE
├── ENGINEERING_SCOPE_AND_INTERPRETATION.md
├── GITHUB_UPLOAD_GUIDE.md
│
├── assets/
│   └── figures/
│       ├── cad/
│       ├── cfd/
│       ├── design-space/
│       ├── optimization/
│       ├── surrogate-models/
│       ├── publication/
│       ├── manufacturing/
│       └── wind-tunnel/
│
├── docs/
│   ├── conference/
│   ├── publication/
│   └── cfd/
│
├── methodology/
│   ├── 01-project-overview.md
│   ├── 02-uav-configuration-and-design-space.md
│   ├── 03-cfd-methodology.md
│   ├── 04-surrogate-modeling.md
│   ├── 05-bayesian-optimization.md
│   ├── 06-composite-fabrication.md
│   └── 07-wind-tunnel-testing.md
│
├── results/
│   ├── baseline-vs-optimized.md
│   ├── optimization-results.md
│   ├── cfd-visualization-results.md
│   ├── surrogate-model-results.md
│   ├── experimental-and-structural-results.md
│   └── wind-tunnel-results.md
│
├── workflow/
│   ├── surrogate-optimization-pseudocode.md
│   └── reproducibility-notes.md
│
└── code/
    └── README.md
```

---

## Documentation Guide

For a quick review, start here:

- [`START_HERE_FOR_REVIEWERS.md`](START_HERE_FOR_REVIEWERS.md)
- [`PUBLICATION.md`](PUBLICATION.md)
- [`ENGINEERING_SCOPE_AND_INTERPRETATION.md`](ENGINEERING_SCOPE_AND_INTERPRETATION.md)

Detailed methodology:

- [`methodology/01-project-overview.md`](methodology/01-project-overview.md)
- [`methodology/02-uav-configuration-and-design-space.md`](methodology/02-uav-configuration-and-design-space.md)
- [`methodology/03-cfd-methodology.md`](methodology/03-cfd-methodology.md)
- [`methodology/04-surrogate-modeling.md`](methodology/04-surrogate-modeling.md)
- [`methodology/05-bayesian-optimization.md`](methodology/05-bayesian-optimization.md)
- [`methodology/06-composite-fabrication.md`](methodology/06-composite-fabrication.md)
- [`methodology/07-wind-tunnel-testing.md`](methodology/07-wind-tunnel-testing.md)

Results:

- [`results/baseline-vs-optimized.md`](results/baseline-vs-optimized.md)
- [`results/optimization-results.md`](results/optimization-results.md)
- [`results/cfd-visualization-results.md`](results/cfd-visualization-results.md)
- [`results/surrogate-model-results.md`](results/surrogate-model-results.md)
- [`results/experimental-and-structural-results.md`](results/experimental-and-structural-results.md)
- [`results/wind-tunnel-results.md`](results/wind-tunnel-results.md)

---

## Publication

### Journal Publication

**Title:** Design and optimization of a blended wing body UAV using AI-driven surrogate modeling and CFD analysis

**Journal:** Proceedings of the Institution of Mechanical Engineers, Part G: Journal of Aerospace Engineering

**Publisher:** SAGE / Institution of Mechanical Engineers

**Publication type:** Research article

**Status:** Published OnlineFirst

**First published online:** April 28, 2026

**DOI:** [10.1177/09544100261447561](https://doi.org/10.1177/09544100261447561)

![SAGE OnlineFirst Publication Page](assets/figures/publication/sage-onlinefirst-publication-page.png)

---

## Conference Presentation

This work was presented at:

**22nd International Bhurban Conference on Applied Sciences & Technology — IBCAST 2025**

**Dates:** August 19–22, 2025  
**Location:** Pakistan  
**Track:** Fluid Dynamics / Applied Sciences & Technology  

Conference participation certificate and presentation material are included for documentation purposes.

Included:

- [`docs/conference/IBCAST-2025-participation-certificate.pdf`](docs/conference/IBCAST-2025-participation-certificate.pdf)
- [`docs/conference/IBCAST-2025-presentation.pptx`](docs/conference/IBCAST-2025-presentation.pptx)

Not included:

- Conference paper PDF
- Publisher-formatted journal PDF
- Journal manuscript DOCX

These files are intentionally excluded from the public repository to avoid copyright and publisher-policy issues.

---

## Code Availability

This repository is currently structured as a documentation-first research portfolio.

The original project workflow involved CFD simulations, surrogate-model training, and optimization. Since the original working scripts are not included in this public release, the `code/` directory provides availability notes and the `workflow/` directory provides reproducibility-level pseudocode and workflow documentation.

See:

- [`code/README.md`](code/README.md)
- [`workflow/surrogate-optimization-pseudocode.md`](workflow/surrogate-optimization-pseudocode.md)
- [`workflow/reproducibility-notes.md`](workflow/reproducibility-notes.md)

---

## Engineering Scope and Interpretation

This repository is intended to present the engineering workflow, methodology, visual evidence, and publication record of the project.

Important interpretation notes:

- The main aerodynamic optimization result is the improvement of L/D from approximately 9.9 to 12.2.
- The Mach 0.7 CFD case is treated as a high-speed flow-visualization case, not the primary low-speed UAV endurance condition.
- Wind tunnel testing is presented as prototype-level experimental characterization, not as perfect CFD validation.
- Some early exploratory plots are retained as part of the research development process but should not be interpreted as final proof of all performance claims.
- The public repository intentionally avoids uploading publisher-controlled manuscript files.

See:

[`ENGINEERING_SCOPE_AND_INTERPRETATION.md`](ENGINEERING_SCOPE_AND_INTERPRETATION.md)

---

## Technical Areas

This project is relevant to:

- Aerospace engineering
- Mechanical engineering
- UAV design
- Blended wing body aircraft
- Computational Fluid Dynamics
- Surrogate modeling
- Gaussian Process Regression
- Bayesian optimization
- Composite manufacturing
- Finite Element Analysis
- Wind tunnel testing
- Low-power aircraft design

---

## Suggested Citation

If you use or refer to this work, please cite the associated journal article:

```bibtex
@article{naseem2026bwb,
  title={Design and optimization of a blended wing body UAV using AI-driven surrogate modeling and CFD analysis},
  journal={Proceedings of the Institution of Mechanical Engineers, Part G: Journal of Aerospace Engineering},
  publisher={SAGE},
  year={2026},
  doi={10.1177/09544100261447561}
}
```

A machine-readable citation file is also provided:

[`CITATION.cff`](CITATION.cff)

---

## Authors and Contributors

This project was completed as part of an undergraduate Final Year Design Project in Mechanical Engineering at COMSATS University Islamabad, Wah Campus.

Published article authors:

- Muhammad Shoaib Naseem
- Muhammad Uns Haider Shah
- Muhammad Nasih Ul Hassan
- Rimsha Zubair
- Ayman Afzal
- Shakeel Afzal
- Mujahid Naseem

---

## Repository Owner

**Muhammad Uns Haider Shah**  
Mechanical Engineer | BWB UAV Design | CFD | Surrogate Modeling | Optimization  

GitHub: [uns-haider96](https://github.com/uns-haider96)

---

## Disclaimer

This repository is an academic and research portfolio. It is intended to document the project methodology, engineering workflow, visual results, publication record, and prototype development process.

Publisher-formatted journal papers, journal manuscript files, and conference paper PDFs are not uploaded unless explicit permission and copyright clearance are available. For the official journal article, please refer to the DOI link.

---

## License

This repository is released for academic portfolio and documentation purposes.

See:

[`LICENSE`](LICENSE)
