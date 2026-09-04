---
title: 'The Duo-Grid: Eliminating Cubed-Sphere Grid Imprinting in FV3'
summary: A novel halo-remapping technique that removes the cube-edge kink of the gnomonic cubed-sphere grid, practically eliminating grid imprinting in FV3.
type: project
date: 2023-12-01
tags:
  - Dynamical Core
  - FV3
  - Duo-Grid
  - Numerical Methods
weight: 20

image:
  placement: 1
  caption: ''
  focal_point: 'smart'
  preview_only: yes

banner:
  image: 'featured_cropped.gif'
  caption: ""
  focal_point: 'center'

links: []
url_code: ''
url_pdf: ''
url_video: ''
---

## The problem: grid imprinting

The gnomonic cubed-sphere grid has excellent accuracy and uniformity, but the
coordinates have a *kink* at the cube edges. In the halo region this kink leaves
a visible imprint of the cube in the solution and requires special edge handling
throughout the solver.

## The Duo-Grid

To reduce grid imprinting, we implemented the novel **Duo-Grid** within FV3. The
Duo-Grid remaps a cube face's data from the neighboring face, moving it from the
kinked locations to natural locations along great circle lines using 1D piecewise
linear interpolation. A separate 2D interpolation algorithm fills the correct
data at the eight corners of the cubed-sphere, which FV3's 2D advection scheme
requires.

## Validation

The Duo-Grid was tested in idealized cases using the 2D shallow water solver and
the 3D hydrostatic and non-hydrostatic solvers.

{{< figure src="duo-grid-tests.gif" title="Idealized test suite run on the Duo-Grid: shallow-water steady-state geostrophic flow, splash test, Rossby-Haurwitz wave, colliding modons, cosine bell advection, and the 3D non-hydrostatic baroclinic wave." >}}

## Key results

- The Rossby-Haurwitz wave remains coherent for substantially longer.
- The southern hemisphere of the baroclinic wave test is noise free.
- Error norms are greatly reduced and grid imprinting is practically eliminated.

These results indicate a clear improvement in FV3's robustness.

## Reference

Mouallem, J., Harris, L., and Chen, X.: *Implementation of the Novel Duo-Grid in
GFDL's FV3 Dynamical Core*, **Journal of Advances in Modeling Earth Systems**,
15(12), 2023.
[https://doi.org/10.1029/2023MS003712](https://doi.org/10.1029/2023MS003712)
