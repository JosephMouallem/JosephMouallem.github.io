---
title: 'A Minimal, Adiabatic Example of Sudden Stratospheric Warming'
summary: 'A minimal adiabatic example of sudden stratospheric warming (SSW) using idealized simulations in the GFDL FV3 dynamical core.'
card_subtitle: "Idealized stratospheric dynamics"
type: project
math: true
date: 2025-09-01
tags:
  - Dynamical Core
  - FV3
  - Stratosphere
  - Idealized Test Case
weight: 40

# image:
#   caption: 'Vortex displacement and vortex split SSW events in the idealized FV3 setup'
#   focal_point: Smart
image:
  placement: 1
  caption: 'Vortex displacement and vortex split SSW events in the idealized FV3 setup'
  focal_point: 'smart'
  preview_only: yes

banner:
  image: 'featured.png'
  caption: ""
  focal_point: 'center'
  


# links: []
# url_code: ''
# url_pdf: ''
# url_video: ''
---
## Motivation

Sudden stratospheric warmings have profound impacts on surface weather weeks later. This idealized modeling study isolates the key physical mechanisms driving SSW dynamics, building intuition and validating model representations of stratospheric-tropospheric coupling.


## Overview

Sudden Stratospheric Warmings (SSW) are extreme events that can significantly
impact weather patterns on short, subseasonal and seasonal timescales. In this
study we present a new **idealized test case** of an SSW event implemented in
GFDL's FV3 dynamical core.

## Setup

The initial condition features a wintertime stratospheric circulation with a
westerly jet in the Northern Hemisphere and an easterly jet in the Southern
Hemisphere. In the absence of tropospheric wave forcing, the model preserves this stratospheric circulation for approximately **200 days**, which makes it a clean baseline.

To induce an SSW, we introduce a *moving mountain* that generates planetary waves of a prescribed zonal wavenumber.

{{< video src="mountain.mp4" title="Animation of the moving mountain forcing used to generate planetary waves of a prescribed zonal wavenumber." >}}

The moving mountain is introduced through a time-dependent surface geopotential perturbation,

$$
\phi' =
g h_0
\sin\left(\frac{r\,\mathrm{time}}{20}\right)
\sin^2\left[
\frac{\pi(\phi-\phi_1)}{\phi_2-\phi_1}
\right]
\cos\left(
z_w\lambda+\frac{10sr\,\mathrm{time}}{360}
\right),
\qquad \phi_2\geq\phi\geq\phi_1.
$$

where \(g\) is gravitational acceleration, \($h_0$\) is the mountain height, \($\phi_1$\) and \($\phi_2$\) define its latitudinal extent, \($z_w$\) is the zonal wavenumber, \($s$\) controls the phase speed, and \($r$\) controls the temporal forcing frequency. The westward-moving mountain generates planetary waves that propagate upward into the stratosphere and interact with the polar vortex.

## Results

The Hovmöller diagram shows the temporal evolution of the zonal-wavenumber components of the 10 hPa zonal wind. The growth and propagation of the planetary-wave components illustrate how the imposed forcing develops and interacts with the stratospheric circulation leading up to the SSW.

{{< figure src="hovmoller_vel_zn1.png" title="Hovmoller diagram for decomposed zonal wind amplitudes at 10⁢ℎ⁡𝑃⁢𝑎 for a perturbed simulation, first row shows wavenumber 0, 1, 2, and 3. Time goes upward in days. Second row shows the decomposed wavenumber 1, 2, and 3 components in zonal winds in (m/s)" >}}

The animation shows the evolution of the zonal-mean Eliassen–Palm (EP) flux and its divergence. The upward propagation of EP flux demonstrates the transport of planetary-wave activity into the stratosphere, followed by enhanced wave–mean-flow interaction and deceleration of the polar-night jet.

{{< video src="EP_flux_zn1_anim.mp4" title="Zonal-mean Eliassen–Palm (EP) flux vectors (arrows) and EP flux divergence (shading, in m/s/day). Gray contours denote the zonal-mean zonal wind (in m/s), with solid lines for positive values and dashed lines for negative values." >}}

{{< figure src="vortex-displacement-split.png" title="Polar view of the two SSW regimes obtained in the idealized setup: wavenumber-1 forcing produces a vortex displacement event (left), while wavenumber-2 forcing produces a vortex split event (right)." >}}

- Wavenumber-1 forcing leads to a **vortex displacement** SSW.
- Wavenumber-2 forcing produces a **vortex split** SSW.

Both are consistent with observations and the published literature.

This minimal setup offers a controlled environment for studying SSW dynamics and
serves as a useful testbed for evaluating the ability of dynamical cores to
capture key stratospheric processes and troposphere-stratosphere interactions.

## Reference

Mouallem, J., Yao, W., Harris, L., Lin, S.-J., and Chen, X.: *A Minimal,
Adiabatic Example of Sudden Stratospheric Warming*, **Journal of Advances in
Modeling Earth Systems**, 17(9), 2025.
[https://doi.org/10.1029/2024MS004760](https://doi.org/10.1029/2024MS004760)
