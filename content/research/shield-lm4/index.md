---
title: 'SHiELD-LM4: Coupled Land-Atmosphere Modeling'
summary: High-resolution coupled atmosphere-land model integrating SHiELD with GFDL's Land Model (LM4) through the FMS coupler, with applications to extreme precipitation and land-atmosphere interactions.
type: project
date: 2025-09-26
tags:
  - Coupled Modeling
  - SHiELD
  - Land-Atmosphere Coupling
  - Hydrology
  - HPC
weight: 38

image:
  placement: 1
  caption: 'Global precipitation, runoff, and river discharge during Hurricane Helene (2024)'
  focal_point: 'smart'
  preview_only: yes

banner:
  image: 'Global_zoomed_precip_runoff_river.gif'
  caption: ""
  focal_point: 'center'

---

## Overview

We present a new high-resolution coupled atmosphere-land model, **SHiELD-LM4**,
which integrates GFDL's advanced atmospheric model (SHiELD) with the Geophysical
Fluid Dynamics Laboratory Land Model (LM4) through the Flexible Modeling System
(FMS) coupler. This coupled system enables accurate representation of 
land-atmosphere interactions, including soil moisture feedbacks, runoff 
generation, and hydrological extremes.

The model captures critical processes such as precipitation-driven runoff, soil 
water dynamics, and their impacts on atmospheric evolution during extreme weather 
events. High-resolution representation is essential for resolving the complex 
interactions between atmospheric convection and land surface hydrology.

## Coupling Infrastructure

The SHiELD-LM4 model employs the Flexible Modeling System (FMS) coupler to 
facilitate bidirectional exchange between the atmospheric and land components. 
The exchange grid ensures accurate conservation of water and energy fluxes at 
the atmosphere-land interface.

{{< figure src="atm_ice_land.png" title="Schematic of atmosphere (Atm), exchange grid (Xgrid), and land/ice components showing multi-level coupling infrastructure and flux exchange pathways." >}}

## Hurricane Helene (2024): Precipitation and Runoff

A key application of the coupled SHiELD-LM4 system is realistic simulation of 
extreme precipitation and its hydrological consequences during tropical cyclones. 
The animation below shows global precipitation and runoff during Hurricane Helene's 
landfall, zoomed on the southeastern United States to reveal localized hydrological 
response.

{{< figure src="Global_zoomed_precip_runoff_river.gif" title="Global precipitation (mm/hr), surface runoff, and river discharge (kg/m³/s) during Hurricane Helene (2024). Zoomed panels show detailed runoff and river flow in the southeastern U.S. during landfall." >}}

## Soil Moisture and Land Surface Response

The coupling captures soil moisture evolution and its feedback to atmospheric 
conditions. The animation shows soil liquid water content evolution during an 
extreme precipitation event, with time series of observed vs. modeled soil moisture 
at multiple locations.

{{< figure src="Runoff_river_helene_26_slow.gif" title="Time series of soil liquid water content (kg/m³) at multiple observation sites during Hurricane Helene, illustrating the rapid soil water response to extreme precipitation and subsequent drainage." >}}

## Soil Column Interactions

The detailed representation of soil-atmosphere interactions is illustrated through 
the vertical exchange of water and energy between atmospheric columns and land model 
soil layers.

{{< figure src="soil_water.png" title="Time series of soil liquid content (kg/m³) at four observation locations (Asheville, Buncombe; Busick, Yancey; Boone, Watauga; Jefferson, Ashe) showing hourly evolution during extreme precipitation event." >}}

## Key Results

- Two-way land-atmosphere coupling effectively captures soil moisture-precipitation 
  feedbacks during extreme events.
- Runoff generation and river discharge are accurately simulated at high resolution.
- Soil water dynamics show realistic response to precipitation forcing with 
  multi-hour memory effects.
- The model demonstrates capability to simulate coupled hydro-atmospheric extremes 
  with kilometer-scale detail.

This work extends coupled modeling capabilities to include detailed land surface 
hydrology, with implications for weather forecasting, hydrological prediction, 
and climate research.

## Reference

Mouallem, J., Malyshev, S., Tan, Z., Shevliakova, E., Gao, K., Harris, L., 
Benson, R., Cooke, W., Zadeh, N., and Chilutti, L.: *Development of a 
high-resolution coupled SHiELD-MOM6-LM4 – Part 2: Model overview, coupling 
technique, and evaluation of hydrological extremes during Hurricane Helene*, 
**Geoscientific Model Development** (accepted), 2025.
