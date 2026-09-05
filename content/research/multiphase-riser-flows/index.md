---
title: 'Macro-Scale Effects on Sub-Grid Closures in Gas-Solid Riser Flows'
summary: 'Macro-scale flow topology effects on sub-grid closure models in filtered two-fluid simulations of gas-solid riser flows.'
card_subtitle: "Sub-grid closures for gas-solid flows"
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
## Motivation

Sub-grid closures for two-fluid models are traditionally derived at a single scale, but this work demonstrates that flow topology at the system scale strongly affects closure accuracy. Accounting for these effects is essential for predictive industrial riser flow simulations.


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

## The drag closure is not scale separated

The drag coefficient correction H, the single most influential sub-grid term, is
the clearest evidence of the failure of scale separation. Correlating H against
the meso-scale filtered variables alone leaves a systematic spread that is set
entirely by the macro-scale state of the flow.

{{< figure src="drag-correction.png" title="Drag coefficient correction H against the filtered solid volume fraction. (a) Effect of the domain average gas Reynolds number at fixed solids loading; (b) effect of the domain average solid volume fraction at fixed Reynolds number. Curves that should collapse if scale separation held instead fan out by a factor of two or more." >}}

## The same holds for the stress closures

The effect is not limited to drag. The filtered solid pressure, which closes the
solid-phase momentum equation, shifts by roughly an order of magnitude across the
range of macro-scale conditions at an otherwise identical filtered state.

{{< figure src="filtered-solid-pressure.png" title="Dimensionless filtered solid pressure against the filtered solid volume fraction. (a) Varying the domain average gas Reynolds number; (b) varying the domain average solid volume fraction. The vertical spread at fixed filtered state is the macro-scale signature that traditional closures ignore." >}}

## Conclusion

Results show that **both** macro-scale parameters should be accounted for in
sub-grid correlations if higher accuracy is to be achieved.

## Reference

Mouallem, J., Chavez-Cussy, N., Niaki, S. R. A., Milioli, C. C., and Milioli,
F. E.: *On the effects of the flow macro-scale over meso-scale filtered parameters
in gas-solid riser flows*, **Chemical Engineering Science**, 182, 200-211, 2018.
[https://doi.org/10.1016/j.ces.2018.02.039](https://doi.org/10.1016/j.ces.2018.02.039)
