# CFD Visualization Results

## Mesh

![Wing surface mesh](../assets/figures/cfd/mesh/wing-surface-mesh.png)

The mesh uses local refinement around the BWB body and wing surface to capture aerodynamic gradients, boundary-layer behavior, and wake-region effects.

## Pressure contours

| Lower Surface | Upper Surface |
|---|---|
| ![Lower surface pressure](../assets/figures/cfd/pressure/static-pressure-lower-surface.png) | ![Upper surface pressure](../assets/figures/cfd/pressure/static-pressure-upper-surface.png) |

The pressure contours show the pressure difference between the lower and upper surfaces, supporting lift generation across the blended wing-body configuration.

## Mach contours

| Root | Mid | Tip |
|---|---|---|
| ![Mach root](../assets/figures/cfd/mach-contours/mach-contour-root-section.png) | ![Mach mid](../assets/figures/cfd/mach-contours/mach-contour-mid-section.png) | ![Mach tip](../assets/figures/cfd/mach-contours/mach-contour-tip-section.png) |

The Mach plots show flow acceleration and wake development from the root to the tip. The root/body blending region shows stronger three-dimensional effects, which is expected in BWB aircraft because the body and lifting surface are integrated.

## Velocity vectors

Velocity-vector plots are included in:

`assets/figures/cfd/velocity-vectors/`

These figures show the direction and relative magnitude of the flow around sectional slices of the geometry.

## X-velocity contours

X-velocity plots are included in:

`assets/figures/cfd/x-velocity/`

These figures help identify streamwise acceleration, wake development, and local low-speed regions.
