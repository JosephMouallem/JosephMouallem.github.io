---
title: 'The Duo-Grid and Cubed-Sphere Grid Imprinting'
summary: 'An efficient refinement strategy for the cubed-sphere grid that enables regional simulations in the global FV3 dynamical core without regridding.'
card_subtitle: "Eliminating grid imprinting in FV3"
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
## Motivation

Addressing the challenge of running localized high-resolution simulations within a global model, the duo-grid imprints a finer mesh over a region of interest, reducing computational cost by an order of magnitude compared to traditional regridding approaches.


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

{{< figure src="kinkduo.png" title="C8 cubed-sphere grid with a three-cell halo. Left: “kinked” grid showing halo updated directly from the neighboring face. Right: “extended” grid for the forward face showing data remapped onto the extended grid. Note that the great circle coordinate lines extend from the compute domain into the grid halo without interruption.." >}}



## Validation
The Duo-Grid was evaluated across a comprehensive suite of idealized test cases spanning both two-dimensional shallow-water dynamics and three-dimensional hydrostatic and non-hydrostatic flows. These tests were designed to assess the impact of the Duo-Grid on grid imprinting, numerical errors, and the overall behavior of the FV3 dynamical core.

The steady-state geostrophic balance test provides a direct assessment of cubed-sphere grid imprinting. When the flow is oriented perpendicular to the cubed-sphere edges, the conventional kinked grid produces errors aligned with the cube geometry. With the Duo-Grid, these grid-aligned errors are substantially reduced.

{{< figure src="case2.gif" title=" Meridional velocity errors of the C48 steady state geostrophic balance flow with a flow oriented perpendicular to the cubed-sphere edges. Duo-Grid significantly reduces these errors." >}}


The improvement extends to fully three-dimensional dynamics. In the baroclinic wave test, the Duo-Grid suppresses the development of cubed-sphere imprinting and errors in the southern hemisphere while maintaining the evolution of the solution over time.

{{< figure src="case13_glob_C48_dpi100.gif" title=" Time evolution of meridional winds in the three-dimensional baroclinic wave test, demonstrating the reduced cubed-sphere errors in the southern hemisphere with the Duo-Grid. " >}}

The Duo-Grid was further evaluated using a broad suite of standard idealized tests, including shallow-water steady-state geostrophic flow, the splash test, Rossby–Haurwitz wave, colliding modons, cosine-bell advection, and the three-dimensional non-hydrostatic baroclinic wave.

{{< figure src="duo-grid-tests.gif" title="Idealized test suite run on the Duo-Grid: shallow-water steady-state geostrophic flow, splash test, Rossby-Haurwitz wave, colliding modons, cosine bell advection, and the 3D non-hydrostatic baroclinic wave." >}}

Across these tests, the Duo-Grid consistently reduces grid imprinting and numerical errors while preserving the accuracy and numerical characteristics of the original FV3 formulation.
## Key results

- Grid imprinting of the cubed sphere is greatly reduced in idealized tests and practically eliminated.
- Duo-Grid decreases the growth rate of error norms in all cases compared to the kinked grid, up to one order of magnitude.
- Order of accuracy of FV3’s horizontal discretization is conserved.
- Dispersion and dissipation properties are identical to those of the original FV3 algorithm.
- Edge handling code is eliminated -> significant performance gain in current/future GPU development
- FV3’s robustness and accuracy have increased.


These results indicate a clear improvement in FV3's robustness.

## Reference

Mouallem, J., Harris, L., and Chen, X.: *Implementation of the Novel Duo-Grid in
GFDL's FV3 Dynamical Core*, **Journal of Advances in Modeling Earth Systems**,
15(12), 2023.
[https://doi.org/10.1029/2023MS003712](https://doi.org/10.1029/2023MS003712)
