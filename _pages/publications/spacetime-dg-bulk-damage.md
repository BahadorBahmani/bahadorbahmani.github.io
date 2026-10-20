---
title: "Asynchronous spacetime discontinuous Galerkin formulation for a hyperbolic time-delay bulk damage model"
layout: publication
pub_id: spacetime-dg-bulk-damage
permalink: /publications/spacetime-dg-bulk-damage/
---

Simulating failure of brittle materials under dynamic loading with continuum damage models is hampered by mesh sensitivity, and many existing remedies are computationally expensive. This paper presents a bulk damage formulation for dynamic fracture that addresses this issue at lower cost.

Damage evolution is governed by a time-delay ordinary differential equation, driven by the difference between a target static damage value and the current damage. The model's intrinsic relaxation time, combined with elastic wave speeds, defines a damage length scale. The resulting hyperbolic system is solved with the asynchronous spacetime discontinuous Galerkin (aSDG) method, which offers a local, asynchronous solution process, cost that scales linearly with the number of elements, local balance properties, and high orders of accuracy in space and time.

**Key findings**

- The length scale introduced by the time-delay model addresses mesh sensitivity with less computational effort than some existing approaches.
- Numerical examples demonstrate mesh-insensitive results.
- Boundary conditions have a visible effect on dynamic fracture patterns.
