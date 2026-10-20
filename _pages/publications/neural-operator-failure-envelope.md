---
title: "Neural Operator Representation of Granular Micromechanics-based Failure Envelope"
layout: publication
pub_id: neural-operator-failure-envelope
permalink: /publications/neural-operator-failure-envelope/
figure_caption: "A DeepONet-based surrogate maps microstructure parameters and a polar angle to a positive radius, which traces out the predicted failure envelope."
---

Granular micromechanics models predict failure in porous and particulate materials such as concrete, soils, foams and biological tissues. However, the link from microstructure parameters to a macroscopic failure envelope is implicit: each point on the envelope requires a costly nonlinear, non-smooth simulation along a loading path. This cost grows further in inverse problems, where one searches for microstructures that give a target failure response.

This paper proposes a differentiable neural operator, based on DeepONet, that maps microstructure configurations directly to failure envelopes, enabling fast forward prediction and gradient-based inverse identification. A curvature penalty motivated by Drucker's postulate pushes the predicted envelopes to be convex. The operator learns from envelopes given as irregular point clouds at varying resolutions, and an ensemble-based active learning strategy picks new simulations where the model is most uncertain.

**Key findings**

- The convexity regularization removes non-physical, non-convex artifacts in both forward predictions and inverse identification.
- Finite differences evaluate the curvature penalty faster than automatic differentiation at the problem sizes of interest.
- Beyond a small initial dataset, 160 adaptively chosen samples gave lower mean error than 320 Latin hypercube samples.
