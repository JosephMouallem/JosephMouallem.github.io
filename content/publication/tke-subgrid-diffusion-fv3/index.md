---
title: "Integrating a Three-Dimensional TKE-Based Subgrid Diffusion Scheme Into GFDL FV3"
authors:
- Kun Gao
- Lucas Harris
- Ping Zhu
- Linjiong Zhou
- admin
date: "2026-06-01T00:00:00Z"
doi: "10.1029/2026MS005916"

# Schedule page publish date (NOT publication's date).
publishDate: "2026-06-01T00:00:00Z"

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["2"]

# Publication name and optional abbreviated publication name.
publication: "*Journal of Advances in Modeling Earth Systems, 18*(6), e2026MS005916"
publication_short: "*JAMES*"

abstract: "We present the implementation of an inline three-dimensional (3D) turbulent kinetic energy (TKE)-based subgrid diffusion scheme in the Geophysical Fluid Dynamics Laboratory (GFDL) Finite-Volume Cubed-Sphere (FV3) dynamical core. This scheme addresses the need for a unified and physically grounded treatment of turbulence as FV3 is increasingly used across the gray zone and large-eddy simulation scales. Building on the 3D TKE framework introduced in Zhu et al. (2025), we embed the full TKE budget calculations, including the 3D shear production, and TKE-informed horizontal and vertical diffusion directly into the FV3 core. Key features include computation of 3D TKE shear production based on FV3 D-grid winds, updating of TKE and diffusion coefficients within the FV3 time-stepping loop, and extension of TKE-based horizontal diffusion to all dynamical fields."

# Summary. An optional shortened abstract.
summary: "An inline 3D TKE-based subgrid diffusion scheme is embedded directly in the FV3 dynamical core, giving a unified turbulence treatment across the gray zone and large-eddy scales."

tags:
- FV3
- Turbulence
- Sub-grid Modeling
- Dynamical Core
featured: false

url_pdf: ''
url_code: ''
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: 'https://doi.org/10.1029/2026MS005916'
url_video: ''

image:
  caption: ''
  focal_point: ''
  preview_only: false

projects: []
---
