# Engineering Scope and Interpretation

This repository presents the project as a public research portfolio. The strongest public claims are based on the peer-reviewed journal article, the optimization results, and the documented CFD, fabrication, structural, and wind tunnel workflow.

## Main Aerodynamic Result

Use the baseline-to-optimized result as the headline quantitative outcome:

- Baseline L/D: approximately 9.9
- Optimized L/D: approximately 12.2
- Improvement: approximately 23%

## CFD Visualizations

The high-speed Fluent report and contour images are included as CFD visualization evidence. They are useful for showing mesh setup, pressure distribution, Mach contours, velocity fields, and root/body flow interaction.

The Mach 0.7 case should be treated as a high-speed flow-visualization case. It should not be confused with the primary low-speed endurance-focused UAV optimization condition.

## Surrogate-Model Figures

The surrogate-model figures document the model-selection process. They show that model performance depends on target variable and dataset structure. The final optimization workflow is presented as Gaussian Process Regression with Expected Improvement-based Bayesian optimization.

## Manufacturing and Wind Tunnel Testing

The manufacturing and wind tunnel images are central evidence that this project progressed beyond numerical simulation. They show 3D printed mold tooling, composite fabrication, carbon-fiber airframe realization, and wind tunnel testing.

The wind tunnel plots should be interpreted as prototype-level experimental characterization. Avoid claiming perfect CFD validation unless repeatability, uncertainty, calibration, and matching test conditions are fully documented.

## Public-Release Principle

The repository emphasizes credible, publication-backed results and curated engineering evidence. It avoids overstating any single figure or preliminary presentation value beyond what is supported by the final publication narrative.

The public repository intentionally excludes:

- Conference paper PDF
- Publisher-formatted journal PDF
- Journal manuscript DOCX
- Raw solver files
- Private drafts or supervisor-only files
