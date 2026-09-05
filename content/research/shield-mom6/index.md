---
title: 'SHiELD-MOM6: High-Resolution Coupled Atmosphere-Ocean Modeling'
summary: "High-resolution coupled atmosphere-ocean-ice modeling. I developed the coupling framework connecting SHiELD, MOM6, and SIS2 through FMS and the exchange-grid infrastructure, enabling two-way air-sea feedback at kilometer scales."
type: project
date: 2025-09-26
tags:
  - Coupled Modeling
  - SHiELD
  - MOM6
  - FV3
  - HPC
weight: 40

image:
  placement: 1
  caption: 'Hurricane Helene (2024) in the coupled SHiELD-MOM6 North Atlantic configuration'
  focal_point: 'smart'
  preview_only: yes

banner:
  # image: 'featured_old.png'
  image: 'helene-slp-sst.gif'
  caption: ""
  focal_point: 'center'
  

# links: []
# url_code: ''
# url_pdf: ''
# url_video: ''
---
## What I developed

- The coupling framework connecting SHiELD, MOM6, and SIS2 through FMS
- Exchange-grid infrastructure for conservative flux exchange between components
- High-resolution coupled atmosphere-ocean-ice model configurations
- Evaluation of hurricane-ocean interaction, including Hurricane Helene (2024)

## Motivation

Air-sea interactions drive storm intensity and ocean response. This coupled system captures two-way feedback between the atmosphere and ocean at kilometer scales, enabling accurate simulations of hurricane-ocean interactions and coastal impacts.


## Overview

We present a new high-resolution coupled atmosphere-ocean model, **SHiELD-MOM6**,
which integrates GFDL's advanced atmospheric model, the System for High-resolution
modeling for Earth-to-Local Domain (SHiELD), the Modular Ocean Model version 6
(MOM6), and the Sea Ice Simulator (SIS2).

The model leverages the Flexible Modeling System (FMS) coupler and its innovative
exchange grid to enable a robust and scalable two-way interaction between the
atmosphere and ocean. The atmospheric component is built on the non-hydrostatic
Finite-Volume Cubed-Sphere Dynamical Core (FV3) with the latest version of the
SHiELD physics parametrization suite, while the ocean component is the latest
version of MOM, supporting kilometer-scale high-resolution and regional
applications.

## Coupling infrastructure


The SHiELD-MOM6 model employs the Flexible Modeling System (FMS) coupler, which facilitates the exchange of information between the atmospheric and oceanic components. The exchange grid ensures accurate and efficient communication, enabling the two-way interaction necessary for realistic coupled simulations.

{{< figure src="atm_ocn.png" title="Schematic of a one-dimensional exchange grid and communication map between the atmosphere and ice components at different resolutions. The red sides of the arrow indicate the step where variables are projected from the exchange grid. The light-blue and mauve sides of the arrows represent the projection of variables onto the exchange grid from the atmosphere or ice components, respectively." >}}

## Hurricane Helene (2024)

Validation is demonstrated through a suite of experiments, including idealized
hurricane simulations and a realistic North Atlantic case study featuring
Hurricane Helene 2024. The animation below shows the simulated sea level pressure
and 10 m winds (left) alongside the sea surface temperature anomaly and ocean
surface currents (right) as the storm crosses the Gulf.

{{< figure src="helene-slp-sst.gif" title="Hurricane Helene (2024): sea level pressure and surface winds (left); sea surface temperature change and ocean currents (right). The cold wake and upwelling behind the storm are captured by the two-way coupling." >}}


## Scalability

Scalability tests have been conducted to evaluate the model's performance on massively parallel computing systems. The results demonstrate that SHiELD-MOM6 maintains high computational efficiency as the number of processors increases, ensuring that high-resolution coupled simulations can be performed within practical timeframes

{{< figure src="scaling_strong_weak.png" title="Strong scaling (a) and weak scaling (b): actual speedup/efficiency (red circles) compared to ideal speedup/efficiency (black squares) as a function of the number of PEs." >}}


## Key results

- Air-sea interactions are effectively captured, both in storm intensity and
  structure and in the ocean response.
- The coupling reproduces ocean phenomena such as storm-induced upwelling, the
  cold wake, and sea level changes.
- Scalability tests confirm the model's computational efficiency on
  massively parallel systems.

This work establishes a unified, modular cornerstone for advancing
high-resolution coupled modeling, with significant implications for weather
forecasting and climate research.

## Reference

Mouallem, J., Gao, K., Reichl, B. G., Chilutti, L., Harris, L., Benson, R.,
Zadeh, N., Chen, J., Chen, J.-H., and Zhang, C.: *Development of a
high-resolution coupled SHiELD-MOM6 model – Part 1: Model overview, coupling
technique, and validation in a regional setup*, **Geoscientific Model
Development**, 18(18), 6461-6478, 2025.
[https://doi.org/10.5194/gmd-18-6461-2025](https://doi.org/10.5194/gmd-18-6461-2025)
