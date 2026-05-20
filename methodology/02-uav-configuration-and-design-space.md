# UAV Configuration and Design Space

## Final BWB UAV configuration

| Parameter | Value |
|---|---:|
| Wingspan | 1.0 m |
| Root chord | 0.30 m |
| Tip chord | 0.15 m |
| Sweep angle | 30° baseline / 28° optimized |
| Taper ratio | 0.50 baseline / 0.48 optimized |
| Wing twist | -2° baseline / -3° optimized |
| Aspect ratio | Approximately 7 |
| Winglet root chord | 0.11 m |
| Winglet tip chord | 0.05 m |
| Winglet cant angle | 15° baseline / 20° optimized |
| Winglet sweep | 10° baseline / 15° optimized |
| Airfoils | Selig S1223, NACA 1408, NACA 0012 |

## Design variables

The design-space study considered geometric parameters including:

- Root chord
- Tip chord
- Wing sweep angle
- Taper ratio
- Wing twist
- Winglet cant angle
- Winglet sweep angle
- Winglet root chord
- Winglet tip chord
- Wingspan and winglet twist as constrained/fixed design parameters in the available sampling plots

## Design-space sampling

Latin Hypercube Sampling was used to distribute candidate geometries across the design space. This helped avoid clustered samples and provided broad coverage for surrogate model training.

## Figures

- `assets/figures/design-space/lhs-parameter-histograms.png`
- `assets/figures/design-space/design-parameter-pairplot.png`
- `assets/figures/design-space/correlation-coefficient-heatmap.png`
- `assets/figures/design-space/p-value-heatmap.png`

## Interpretation

The histogram and pairplot figures show that the main geometric variables were broadly sampled. The correlation and p-value heatmaps show mostly weak pairwise correlation, which supports the use of the sampled dataset for surrogate model development.
