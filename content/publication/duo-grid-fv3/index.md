---
title: "Implementation of the Novel Duo-Grid in GFDL's FV3 Dynamical Core"
authors:
- admin
- Lucas Harris
- Xi Chen
date: "2023-12-01T00:00:00Z"
doi: "10.1029/2023MS003712"

# Schedule page publish date (NOT publication's date).
publishDate: "2023-12-01T00:00:00Z"

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["2"]

# Publication name and optional abbreviated publication name.
publication: "*Journal of Advances in Modeling Earth Systems, 15*(12)"
publication_short: "*JAMES*"

abstract: "The gnomonic cubed-sphere grid has excellent accuracy and uniformity, but the 'kink' in the coordinates at the cube edges in the halo region can leave an imprint of the cube in the solution, and requires special edge handling. To reduce grid imprinting, we implement the novel 'Duo-Grid' within FV3. The Duo-Grid remaps a cube face's data from neighboring face from kinked to natural locations along great circle lines using 1D piecewise linear interpolation. A 2D interpolation algorithm is used to fill correct data at the eight corners of the cubed-sphere needed for FV3's 2D advection scheme. The Duo-Grid was tested in idealized tests using the 2D shallow water solver and the 3D hydrostatic and non-hydrostatic solvers: Rossby-Haurwitz wave lasts longer and the southern hemisphere of the baroclinic wave test is noise free. We found that error norms are greatly reduced and grid imprinting is practically eliminated when employing the Duo-Grid. These results indicate that FV3's robustness has improved."

# Summary. An optional shortened abstract.
summary: "The Duo-Grid remaps halo data along great circle lines to remove the cube-edge kink, practically eliminating grid imprinting in FV3."

tags:
- FV3
- Dynamical Core
- Duo-Grid
- Cubed-Sphere
- Grid Imprinting
featured: true

url_pdf: ''
url_code: ''
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: 'https://doi.org/10.1029/2023MS003712'
url_video: ''

image:
  caption: ''
  focal_point: ''
  preview_only: false

projects: []
---
