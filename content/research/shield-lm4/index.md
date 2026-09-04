---
title: 'SHiELD-LM4: High-Resolution Coupled Atmosphere-Land Modeling'
summary: A high-resolution coupled atmosphere-land model integrating SHiELD and LM4 through the FMS coupler to represent precipitation, land-surface processes, runoff, and river discharge.
date: 2026-09-01
tags:
  - Coupled Modeling
  - SHiELD
  - LM4
  - FV3
  - HPC
weight: 1

image:
  placement: 1
  caption: 'Atmosphere-land interactions and hydrological response in the coupled SHiELD-LM4 model'
  focal_point: 'smart'
  preview_only: yes

banner:
  image: 'Global_zoomed_precip_runoff_river.gif'
  caption: ""
  focal_point: 'center'
---

## Overview

We present a high-resolution coupled atmosphere-land modeling framework, SHiELD-LM4, which integrates GFDL's System for High-resolution modeling for Earth-to-Local Domain (SHiELD) atmospheric model with the LM4 land model through the Flexible Modeling System (FMS) coupler.

The atmospheric component is based on the non-hydrostatic Finite-Volume Cubed-Sphere Dynamical Core (FV3) and the SHiELD physics suite, while LM4 provides a physically based representation of land-surface processes and terrestrial hydrology. The coupling framework enables two-way interactions between the atmosphere and land surface, allowing precipitation, soil water, surface fluxes, runoff, and river discharge to evolve consistently across the coupled system.

The resulting framework provides a foundation for high-resolution simulations of weather, land-surface processes, and hydrological extremes, with applications ranging from regional precipitation and flooding to global weather and climate modeling.

## Atmosphere–land coupling

SHiELD-LM4 uses the FMS coupler to exchange atmospheric and land-surface quantities between the two model components. This coupling provides a consistent pathway for the exchange of energy and water between the atmosphere and land, including precipitation, surface fluxes, soil moisture, and runoff.

{{< figure src="atm_ice_land.png" title="Schematic of the atmosphere–land coupling framework. The FMS coupler facilitates the exchange of atmospheric forcing and land-surface fluxes between SHiELD and LM4." >}}

## Soil water and land-surface response

The coupled model represents the evolution of terrestrial water through the land surface and soil column. Precipitation is partitioned between infiltration, soil-water storage, and runoff, allowing the land surface to respond dynamically to atmospheric forcing.

{{< figure src="soil_water.png" title="Simulated soil-water distribution in the coupled SHiELD-LM4 system, illustrating the spatial structure of terrestrial water storage and its response to atmospheric precipitation." >}}

## Precipitation, runoff, and rivers

One of the key capabilities of SHiELD-LM4 is the consistent representation of the full hydrological pathway from atmospheric precipitation to surface runoff and river discharge.

The animation below illustrates the evolution of precipitation, runoff, and river flow across the global domain, highlighting the connection between atmospheric rainfall and the downstream hydrological response.

{{< figure src="Global_zoomed_precip_runoff_river.gif" title="Precipitation, surface runoff, and river discharge in the coupled SHiELD-LM4 simulation. The animation illustrates the progression of atmospheric precipitation into terrestrial runoff and river flow." >}}

## Hurricane Helene (2024)

The coupled model is also evaluated for extreme precipitation and hydrological response during Hurricane Helene (2024). The event produced widespread heavy precipitation across the southeastern United States, providing a useful test of the model's ability to represent the coupled atmospheric and terrestrial response to an extreme weather event.

The animation below follows the evolution of precipitation, runoff, and river discharge associated with Hurricane Helene, illustrating how intense rainfall is translated into a downstream hydrological response.

{{< figure src="Runoff_river_helene_26_slow.gif" title="Hurricane Helene (2024): evolution of surface runoff and river discharge following the storm's precipitation. The simulation illustrates the propagation of the hydrological response from rainfall to river flow." >}}

## Key results
The coupled framework enables consistent two-way exchange of water and energy between the atmosphere and land surface.
High-resolution precipitation is translated into a dynamically evolving terrestrial hydrological response, including soil-water storage, runoff, and river discharge.
The model captures the spatial and temporal evolution of hydrological responses to extreme precipitation events.
The coupled atmosphere-land framework provides a foundation for studying high-resolution weather, hydrology, and compound precipitation–flooding events.

SHiELD-LM4 provides a unified framework for connecting atmospheric processes with terrestrial hydrology, enabling high-resolution simulations of the interactions between weather, land-surface processes, and extreme hydrological events.

## Reference

Mouallem, J., Malyshev, S., Tan, Z., Shevliakova, E., Gao, K., Harris, L., Benson R., Cooke, W., Zadeh, N., Chilutti, L.: Development of a high-resolution coupled SHiELD-MOM6-LM4 – Part 2: Model overview, coupling technique, and evaluation of hydrological extremes during Hurricane Helene, Geoscientific Model Development, (accepted))

<!-- https://doi.org/10.5194/gmd-18-6461-2025 -->