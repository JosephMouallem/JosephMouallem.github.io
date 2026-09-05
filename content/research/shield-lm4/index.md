---
title: 'SHiELD-LM4: High Resolution Coupled Land-Atmosphere Modeling'
summary: "Extending SHiELD into a fully coupled atmosphere-land system to improve precipitation, runoff, and hydrological extremes at kilometer-scale resolution."
card_subtitle: "Coupled land-atmosphere modeling"
type: project
date: 2026-09-04
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
  image: 'Global_zoomed_precip_runoff_river.mp4'
  caption: ""
  focal_point: 'center'

---


## Motivation
This system integrates advanced high-resolution atmospheric and land processes to capture how soil moisture, vegetation, and runoff feedback on regional weather patterns, advancing forecast skill for hydrological extremes.


## Overview

We present a new high-resolution coupled atmosphere-land model, **SHiELD-MOM6-LM4**,
which integrates GFDL's advanced atmospheric model (SHiELD) with the Geophysical
Fluid Dynamics Laboratory Land Model (LM4) through the Flexible Modeling System
(FMS) coupler. This coupled system enables accurate representation of 
land-atmosphere interactions, including soil moisture feedbacks, runoff 
generation, and hydrological extremes.

The model captures critical processes such as precipitation-driven runoff, soil 
water dynamics, river discharge, and their impacts on atmospheric evolution during extreme weather 
events. High-resolution representation is essential for resolving the complex 
interactions between atmospheric convection and land surface hydrology.

## Coupling Infrastructure

The SHiELD-LM4 model employs the Flexible Modeling System (FMS) coupler to 
facilitate bidirectional exchange between the atmospheric and land components. 
The exchange grid ensures accurate conservation of water and energy fluxes at 
the atmosphere-land interface.

{{< figure src="atm_ice_land.png" title="Schematic of atmosphere (Atm), exchange grid (Xgrid), and land/ice components showing multi-level coupling infrastructure and flux exchange pathways." >}}

## Hurricane Helene (2024): Precipitation, Soil Saturation, Runoff and River Discharge

Hurricane Helene provides a demanding test of the coupled SHiELD-LM4 system. Extreme precipitation over the southern Appalachians rapidly saturated the soil, triggering localized runoff and subsequent river flooding across western North Carolina. The case study illustrates the complete hydrological response from precipitation forcing to soil moisture evolution, runoff generation, and downstream river discharge.

## Soil Moisture Response

The first step in this response is the rapid evolution of soil moisture following the arrival of extreme precipitation. As Helene moves across western North Carolina, soil liquid water content increases rapidly, with the upper soil layers reaching saturation within a few hours. At Asheville/Buncombe, water propagates downward through the soil column, with all layers approaching saturation at approximately 400 kg/m³.

Following peak saturation, the soil column exhibits depth-dependent drainage. Near-surface layers lose water relatively quickly, while deeper layers retain elevated moisture for much longer. This provides a detailed view of how extreme precipitation is absorbed, redistributed, and retained within the land surface.

{{< figure src="soil_water.png" title="Time series of soil liquid content (kg/m³) at four observation locations (Asheville, Buncombe; Busick, Yancey; Boone, Watauga; Jefferson, Ashe) showing hourly evolution during extreme precipitation event." >}}

## Runoff and River Response

Once the soil approaches saturation, additional precipitation is converted into surface runoff. The runoff response is sharply localized over the southern Appalachians, with the strongest signal concentrated around Buncombe, Yancey, Watauga, Ashe, and surrounding counties, the region that experienced catastrophic flooding during Helene.

The resulting runoff is then transferred into the river network. River discharge increases rapidly but with a several-hour delay relative to the runoff response, reflecting water travel through the routing network. Unlike the short-lived runoff signal, river flow remains elevated for several days before gradually declining, demonstrating how the river-routing component integrates and redistributes upstream runoff over longer timescales.

{{< video src="Runoff_river_helene_26_slow.mp4" title="Animation showing runoff and river discharge response during Hurricane Helene (2024)." >}}


## A Global Simulation of Hydrological Extremes
The Helene case is part of a **single** fully coupled global simulation, allowing hydrological extremes to be represented **simultaneously** across different regions of the world. At the same time that the model captures Hurricane Helene and its associated precipitation, runoff, and river response over the southeastern United States, it also resolves an **independent** extreme rainfall event over Nepal and northeastern India.

In South Asia, the simulation produces an intense band of rainfall along the Himalayan front, with surface runoff concentrated near the Nepal–India border. The river-flow response extends across the dense drainage network of the Ganges–Brahmaputra system, providing a second example of how atmospheric forcing is translated into a land-surface and hydrological response.

This highlights a key advantage of **global** coupled modeling: **multiple, geographically independent extreme events can be simulated within one simulation**, without changing the model configuration or computational domain.


{{< video src="Global_zoomed_precip_runoff_river.mp4" title="Global precipitation (mm/hr), surface runoff, and river discharge (kg/m³/s) during Hurricane Helene (2024). The model simultaneously captures Hurricane Helene over the southeastern United States and an independent extreme rainfall and flooding event over Nepal and northeastern India." >}}



## Key Results

- Two-way land-atmosphere coupling effectively captures soil moisture-precipitation 
  feedbacks during extreme events.
- Runoff generation and river discharge are accurately simulated at high resolution.
- Soil water dynamics show realistic response to precipitation forcing with 
  multi-hour memory effects.
- The model demonstrates capability to simulate coupled hydro-atmospheric extremes 
  with kilometer-scale detail.

This work extends coupled modeling capabilities at high resolution to include detailed land surface 
hydrology, with implications for weather forecasting, hydrological prediction, 
and climate research.

## Reference

Mouallem, J., Malyshev, S., Tan, Z., Shevliakova, E., Gao, K., Harris, L., 
Benson, R., Cooke, W., Zadeh, N., and Chilutti, L.: *Development of a 
high-resolution coupled SHiELD-MOM6-LM4 – Part 2: Model overview, coupling 
technique, and evaluation of hydrological extremes during Hurricane Helene*, 
**Geoscientific Model Development** (accepted), 2026.
