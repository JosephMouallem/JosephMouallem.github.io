---
title: "Development of a high-resolution coupled SHiELD-MOM6-LM4 – Part 2: Model overview, coupling technique, and evaluation of hydrological extremes during Hurricane Helene"
authors:
- admin
- Sergey Malyshev
- Zhihong Tan
- Elena Shevliakova
- Kun Gao
- Lucas Harris
- Rusty Benson
- William Cooke
- Niki Zadeh
- Lauren Chilutti
date: "2026-05-19T00:00:00Z"
doi: "10.5194/egusphere-2026-2014"

# Schedule page publish date (NOT publication's date).
publishDate: "2026-05-19T00:00:00Z"

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["2"]

# Publication name and optional abbreviated publication name.
publication: "*Geoscientific Model Development* (accepted)"
publication_short: "*Geosci. Model Dev.*"

abstract: "This work describes the implementation strategy and technical challenges involved in integrating the Geophysical Fluid Dynamics Laboratory (GFDL)'s Land Model (LM4) with dynamic subgrid tiling capabilities within the atmospheric model, System for High-resolution modeling for Earth-to-Local Domains (SHiELD), capable of kilometer-scale global simulations. A key challenge addressed in this effort is coupling LM4, which was designed for implicit surface flux coupling, with SHiELD's explicit physics solver. We achieve this through a refactoring of the atmospheric physics suite and code drivers, enabling implicit land-atmosphere coupling of heat and moisture within the well established FMS coupler infrastructure. The resulting flexible architecture supports multiple model configurations from a single executable without recompilation. This extends SHiELD from an uncoupled atmospheric model, in which land processes are treated as a part of the atmospheric physics package, to a fully coupled high resolution atmosphere-ocean-land-ice model. We demonstrate the new system through a high-resolution global simulation of Hurricane Helene's landfall where the land component realistically captures the rapid soil saturation, localized runoff generation and multi-day river flooding concentration in Western North Carolina. These results validate the technical coupling strategy, unlock new forecast capabilities, and highlight the importance of interactive land-atmosphere coupling for simulating extreme weather and hydrological events."

# Summary. An optional shortened abstract.
summary: "Implicit land-atmosphere coupling of GFDL's LM4 land model within SHiELD, extending it to a fully coupled atmosphere-ocean-land-ice system, evaluated on Hurricane Helene's flooding."

tags:
- Land-Atmosphere Coupling
- SHiELD
- LM4
- Coupled Modeling
- Hydrology
featured: true

url_pdf: ''
url_code: ''
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: 'https://doi.org/10.5194/egusphere-2026-2014'
url_video: ''

image:
  caption: ''
  focal_point: ''
  preview_only: false

projects: [shield-lm4]
---
