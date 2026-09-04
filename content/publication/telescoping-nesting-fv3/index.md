---
title: "Multiple same-level and telescoping nesting in GFDL's dynamical core"
authors:
- admin
- Lucas Harris
- Rusty Benson
date: "2022-06-07T00:00:00Z"
doi: "10.5194/gmd-15-4355-2022"

# Schedule page publish date (NOT publication's date).
publishDate: "2022-06-07T00:00:00Z"

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["2"]

# Publication name and optional abbreviated publication name.
publication: "*Geoscientific Model Development, 15*(11), 4355-4371"
publication_short: "*Geosci. Model Dev.*"

abstract: "Two-way multiple same-level and telescoping grid nesting capabilities are implemented in FV3 using GFDL's Flexible Modeling System (FMS). A nest is an additional grid that zooms in over a region of interest to resolve small-scale structures necessary to get a better forecast of localized weather events such as severe storms and hurricanes. A telescoping nest is a nest within a nest. The nested grids run concurrently on different sets of processors and interact with their parent grids, thus providing more accurate results on both grids and reducing load imbalances between different processors. Nests could be used in global and regional domains. Starting from the latest FV3 public release of 2021, multiple same level and telescoping nests are now fully functional and available for use by the broader scientific community. This will drastically improve the overall forecast performance, bringing unprecedented accuracy, and open the door to numerous research possibilities for scientists and meteorologists alike."

# Summary. An optional shortened abstract.
summary: "Two-way multiple same-level and telescoping grid nesting implemented in FV3 via GFDL's Flexible Modeling System, available since the 2021 public release."

tags:
- FV3
- Dynamical Core
- Grid Nesting
- HPC
featured: true

url_pdf: ''
url_code: ''
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: 'https://doi.org/10.5194/gmd-15-4355-2022'
url_video: ''

image:
  caption: ''
  focal_point: ''
  preview_only: false

projects:
  - grid-nesting
---
