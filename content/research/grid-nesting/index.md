---
title: 'Multiple Same-Level and Telescoping Grid Nesting'
summary: "A flexible nesting implementation in GFDL's dynamical core enabling both same-level and telescoping grids for multi-scale simulations."
card_subtitle: "Multiscale simulation in FV3"
type: project
date: 2022-06-07
tags:
  - Dynamical Core
  - FV3
  - Grid Nesting
  - HPC
weight: 30

image:
  placement: 1
  caption: ''
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

Multi-scale modeling often requires simulations at many different resolutions. This work shows how to couple coarse and fine domains within a single dynamical core, enabling cost-effective high-resolution forecasts of localized phenomena like hurricanes.


## Overview

Two-way **multiple same-level** and **telescoping** grid nesting capabilities are
implemented in FV3 using GFDL's Flexible Modeling System (FMS).

A *nest* is an additional grid that zooms in over a region of interest to resolve
the small-scale structures needed for better forecasts of localized weather events
such as severe storms and hurricanes. A *telescoping nest* is a nest within a
nest, allowing resolution to be refined progressively over the target region.

{{< figure src="telescoping-nests.png" title="Multiple same-level and telescoping nests on the cubed-sphere. Nests can be placed side by side at the same level, or nested inside one another to form a hierarchy of refinement levels." >}}

## Progressive refinement

Nests can be used in both global and regional domains, and each level of the
hierarchy can refine the parent resolution by an arbitrary factor.

{{< figure src="nest-resolutions.png" title="A telescoping configuration refining a global ~13 km grid down to ~4.3 km, ~1.4 km and ~0.5 km over the region of interest." >}}

## Computational design

The nested grids run **concurrently** on different sets of processors and interact
two-way with their parent grids. This provides more accurate results on both the
nest and the parent, and reduces load imbalance between processors.

## Availability

Starting from the FV3 public release of 2021, multiple same-level and telescoping
nests are fully functional and available to the broader scientific community. This
drastically improves overall forecast performance and opens the door to numerous
research possibilities for scientists and meteorologists alike.

## Reference

Mouallem, J., Harris, L., and Benson, R.: *Multiple same-level and telescoping
nesting in GFDL's dynamical core*, **Geoscientific Model Development**, 15(11),
4355-4371, 2022.
[https://doi.org/10.5194/gmd-15-4355-2022](https://doi.org/10.5194/gmd-15-4355-2022)
