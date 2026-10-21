---
published: false
title: "A kd-tree-accelerated hybrid data-driven/model-based approach for poroelasticity problems with multi-fidelity multi-physics data"
layout: publication
pub_id: kd-tree-poroelasticity
permalink: /publications/kd-tree-poroelasticity/
figure_caption: "The four formulations, from fully model-based to fully data-driven, defined by whether the solid and fluid constitutive laws are model-based or data-driven."
byline: "This page was summarized by AI (Claude by Anthropic)."
---

Poroelasticity models couple solid deformation with pore-fluid flow, but the two constitutive laws differ widely in fidelity. Elastic responses of rocks, soils and bone are often captured well by calibrated models, whereas porosity-permeability predictions carry much larger uncertainty, making hydraulic models a major bottleneck.

This paper extends the model-free, distance-minimizing data-driven framework to coupled diffusion-deformation problems. It introduces one fully data-driven and two hybrid formulations in which either the solid or the fluid solver can switch between a model-based law and direct use of data, depending on how much data is available and how reliable it is. A k-dimensional (k-d) tree nearest-neighbor search replaces brute-force search for the closest data points.

**Key findings**

- With enough data, all data-driven formulations converge to the conventional model-based finite element solution.
- The data-driven schemes captured the Poisson effect without an explicit constitutive law, even with a small database of 1000 points.
- The k-d tree search reduced a five-hour simulation to under ten minutes for the largest database tested.
- A porosity-dependent dataset variant handled a heterogeneous Berea sandstone problem with satisfactory solver performance.
