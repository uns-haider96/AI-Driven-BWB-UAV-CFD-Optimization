# CFD Methodology

## CFD software

ANSYS Fluent was used for aerodynamic simulation and flow visualization.

## Simulation model

The available Fluent report documents a high-speed CFD case with the following setup:

| Item | Value |
|---|---:|
| Solver | 3D, steady, pressure-based |
| Turbulence model | SST k-omega |
| Heat transfer | Enabled |
| Freestream condition | Pressure-farfield |
| Mach number | 0.7 for the documented high-speed visualization case |
| Temperature | 300 K |
| Flow direction | Positive X direction |
| Turbulence intensity | 5% |
| Turbulent viscosity ratio | 10 |
| Fluid | Air, ideal gas |

## Mesh statistics

| Quantity | Value |
|---|---:|
| Cells | 1,291,222 |
| Faces | 5,568,328 |
| Nodes | 3,118,737 |
| Minimum orthogonal quality | 0.0508 |
| Maximum aspect ratio | 264.6 |

## CFD visualizations included

The repository includes:

- Surface mesh images
- Volume mesh image
- Static pressure contours
- Mach number contours at root, mid-span, and tip sections
- X-velocity contours
- Velocity-vector plots

## Interpretation

The pressure contours demonstrate lift-producing pressure differences between the upper and lower surfaces. The Mach and velocity plots show flow acceleration over the wing-body geometry, wake development near the trailing region, and stronger three-dimensional effects near the root/body blending region.

## Engineering scope

The Mach 0.7 Fluent case is presented as high-speed aerodynamic visualization. The low-speed endurance result of the UAV should be interpreted through the baseline-to-optimized aerodynamic results and the Bayesian optimization outcome.
