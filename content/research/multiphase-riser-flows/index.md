---
title: 'Macro-Scale Effects on Sub-Grid Closures in Gas-Solid Riser Flows'
summary: Filtered two-fluid modeling of gas-solid riser flows, showing that macro-scale flow topology must be accounted for in sub-grid closure correlations.
type: project
date: 2018-06-01
tags:
  - CFD
  - Multiphase Flows
  - Two-Fluid Model
  - Sub-grid Modeling
weight: 70

image:
  caption: 'Solid volume fraction fields across solids loadings and gas Reynolds numbers'
  focal_point: Smart

links: []
url_code: ''
url_pdf: ''
url_video: ''
---

## Background

Filtered two-fluid formulations of gas-solid fluidized flows require closure
models to deal with sub-grid filtered parameters. These closures are derived by
filtering the results of meso-scale highly resolved simulations (HRS) with
two-fluid modeling, and then applying them on the coarse large-scale simulation
(LSS) grid.

{{< figure src="filtered-parameters.png" title="Closure strategy: a highly resolved simulation with the two-fluid model and microscopic closures is filtered to provide sub-grid closures for the coarse, large-scale filtered two-fluid model." >}}

## The question

Trusting in scale separation, the correlation of filtered parameters has
traditionally been performed against meso-scale filtered data only, disregarding
any macro-scale effects. **In this work, the correctness of that practice is
tested — and it fails.**

## Approach

Two macro-scale parameters associated with flow topology are considered for their
effects on the relevant filtered parameters: the average solid volume fraction and
the average gas Reynolds number. Highly resolved simulations are filtered while
holding each of these macro-scale parameters constant at various levels. The
interest is directed toward the dilute conditions typical of riser flows.

{{< figure src="riser-flow.png" title="Instantaneous solid volume fraction for increasing solids loading (left to right) and increasing gas Reynolds number (top to bottom). The cluster structure — and therefore the sub-grid closure — depends strongly on both macro-scale parameters." >}}

## Conclusion

Results show that **both** macro-scale parameters should be accounted for in
sub-grid correlations if higher accuracy is to be achieved.

## Reference

Mouallem, J., Chavez-Cussy, N., Niaki, S. R. A., Milioli, C. C., and Milioli,
F. E.: *On the effects of the flow macro-scale over meso-scale filtered parameters
in gas-solid riser flows*, **Chemical Engineering Science**, 182, 200-211, 2018.
[https://doi.org/10.1016/j.ces.2018.02.039](https://doi.org/10.1016/j.ces.2018.02.039)
