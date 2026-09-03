---
title: 'A Minimal, Adiabatic Example of Sudden Stratospheric Warming'
summary: An idealized, adiabatic test case of Sudden Stratospheric Warming in FV3 that reproduces both vortex displacement and vortex split events.
type: project
date: 2025-09-01
tags:
  - Dynamical Core
  - FV3
  - Stratosphere
  - Idealized Test Case
weight: 40

image:
  caption: 'Vortex displacement and vortex split SSW events in the idealized FV3 setup'
  focal_point: Smart

links: []
url_code: ''
url_pdf: ''
url_video: ''
---

## Overview

Sudden Stratospheric Warmings (SSW) are extreme events that can significantly
impact weather patterns on short, subseasonal and seasonal timescales. In this
study we present a new **idealized test case** of an SSW event implemented in
GFDL's FV3 dynamical core.

## Setup

The initial condition features a wintertime stratospheric circulation with a
westerly jet in the Northern Hemisphere and an easterly jet in the Southern
Hemisphere. In the absence of tropospheric wave forcing, the model preserves this
stratospheric circulation for approximately **200 days**, which makes it a clean
baseline.

To induce an SSW, we introduce a *moving mountain* that generates planetary waves
of a prescribed zonal wavenumber.

## Results

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
