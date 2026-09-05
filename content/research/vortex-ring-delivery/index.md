---
title: 'Targeted Particle Delivery via Vortex Ring Reconnection'
summary: 'A conceptual model for targeted particle delivery using controlled vortex ring reconnection in a duct.'
card_subtitle: "Vortex dynamics and particle transport"
type: project
date: 2021-10-01
tags:
  - CFD
  - Vortex Dynamics
  - Multiphase Flows
weight: 50

image:
  placement: 1
  caption: 'Reconnection of a pair of particle-laden vortex rings'
  focal_point: 'smart'
  preview_only: yes

banner:
  image: 'vortex-ring-reconnection.gif'
  caption: ""
  focal_point: 'center'

links: []
url_code: ''
url_pdf: ''
url_video: ''
---
## Motivation

Precise particle targeting is important in manufacturing, propulsion, and medical applications. This work shows how vortex ring dynamics can coherently transport particles to specific wall locations, with design parameters (ring size, Stokes number) controlling delivery accuracy.


## Concept

A conceptual model for **targeted particle delivery** is proposed using controlled
vortex ring reconnection. Particles entrained in the core of a vortex ring are
efficiently transported as the ring advects by self-induction.

{{< figure src="particle-delivery.png" title="Left: initial particle seeding within the cores of the two vortex rings. Right: the reconnection sequence — first reconnection, second reconnection, and pinch off — that redirects the particles toward the sidewalls." >}}

## Mechanism

A pair of these particle-transporting vortex rings traveling in the streamwise
direction along parallel trajectories will mutually interact, resulting in a pair
of **vortex reconnection events**. The reconnection causes a topological change to
the ring, accompanied by a rapid repulsion in the plane perpendicular to the
direction of travel. This effectively transports the particles toward the desired
location on the sidewalls of a ducted flow.

{{< figure src="vortex-ring-reconnection.gif" title="Simulation of the two particle-laden vortex rings advecting, interacting, and reconnecting inside the duct." >}}

In addition to proposing this conceptual model, we identify the dominant physics
of the process and the design considerations required to achieve targeted
delivery.

## Particle inertia sets the delivery

Whether the particles actually follow the rings is governed by the Stokes number.
Low-inertia particles stay locked to the ring cores and are carried coherently
through both reconnections, while high-inertia particles decouple from the
vortex and disperse before reaching the wall.

{{< figure src="stokes-number.png" title="Mean streamwise particle position (left) and mean wall-normal particle position (right) for St = 0.1, 1 and 10. Shaded bands show one standard deviation and the dashed lines mark the two reconnection events. At St = 0.1 and St = 1 the particles track the rings and are delivered together; at St = 10 they lag and spread widely." >}}

## Design considerations

The ring radius, relative to the channel width, controls how strongly the rings
repel after reconnection and therefore where on the sidewall the particles
arrive. This makes ring size the primary design parameter for aiming the
delivery.

{{< figure src="ring-size.png" title="Spreading angle θ after reconnection for three ring sizes, with R set by the channel width W: R = 0.15W (blue), R = 0.125W (green) and R = 0.1W (red). Larger rings separate more aggressively, moving the impact point further upstream." >}}

## Reference

Mouallem, J., Daryan, H., Wawryk, J., Pan, Z., and Hickey, J.-P.: *Targeted
particle delivery via vortex ring reconnection*, **Physics of Fluids**, 33(10),
2021.
[https://doi.org/10.1063/5.0066443](https://doi.org/10.1063/5.0066443)
