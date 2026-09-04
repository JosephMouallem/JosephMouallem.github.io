---
title: 'Induction Heating of Dispersed Metallic Particles in a Turbulent Flow'
summary: Direct Numerical Simulation of inductively heated metallic particles dispersed in a decaying isotropic turbulent carrier gas.
type: project
date: 2020-11-01
tags:
  - DNS
  - Turbulence
  - Multiphase Flows
  - Heat Transfer
weight: 60

image:
  caption: 'Particle clustering and gas temperature field during induction heating'
  focal_point: Smart

links: []
url_code: ''
url_pdf: ''
url_video: ''
---

## Overview

Inductively heated solid particles dispersed within a decaying isotropic turbulent
carrier gas are investigated via **Direct Numerical Simulation (DNS)**. The
multiphase simulations account for the compressibility and temperature-dependent
viscosity of the carrier gas.

We develop a semi-empirical model for solid particle heating through hysteresis
and Joule mechanisms, as these dispersed particles are heated by an external
high-frequency alternating magnetic field.

{{< figure src="heating-model-validation.png" title="Validation of the semi-empirical induction heating model against the experimental data of Bae et al. (2015). Symbols are measurements for four particle loadings (5 to 20 phr); solid lines are the model, each with its own induction heating timescale. Higher loading heats faster and reaches a higher equilibrium temperature." >}}

{{< figure src="induction-heating.png" title="Gas temperature field (colors) and particle positions (black dots) in a 2D slice of the domain at t = 10, for increasing particle thermal response time (left to right). Hotter gas develops around the particle-laden regions as the thermal fluctuations grow." >}}

## Key results

- The growth of the Kolmogorov length scale is due to a simultaneous **increase in
  viscosity** and **decrease in the dissipation rate**.
- The temperature-dependent viscosity of the gas leads to a faster decay of the gas
  turbulent kinetic energy, mainly through a loss of energy at intermediate
  wavenumbers.
- The gas and particle thermal fluctuations are **inversely correlated**, set by the
  relative thermodynamic timescales.
- Two regimes appear in the temperature spectrum: while thermal fluctuations grow,
  thermal energy increases monotonically in the low-wavenumber range; once they
  decay, the decay occurs across the entire spectrum.
- Aggressive heating (shorter induction heating timescales) **reduces particle
  clustering**, whereas the particle thermal response time shows no such effect.

## Heating de-clusters the particles

Preferential concentration is measured with the radial distribution function.
The unheated case shows the strongest clustering at small separations, and the
clustering weakens monotonically as the induction heating becomes more
aggressive, while changing the particle thermal response time leaves the
distribution essentially unchanged.

{{< figure src="particle-clustering-rdf.png" title="Radial distribution function of the particles at t = 30 for all cases, with a zoom on the small-separation limit. The unheated reference (I∞T0) clusters the most; shorter induction heating timescales (I10T10 to I01T10) progressively reduce clustering, while varying the thermal response time (I1T10, I1T100, I1T1000) has little effect." >}}

## Reference

Mouallem, J. and Hickey, J.-P.: *Induction heating of dispersed metallic particles
in a turbulent flow*, **International Journal of Multiphase Flow**, 132, 103414,
2020.
[https://doi.org/10.1016/j.ijmultiphaseflow.2020.103414](https://doi.org/10.1016/j.ijmultiphaseflow.2020.103414)
