---
title: "Data-Driven Cohesive Zone Modeling within the Generalized Standard Materials Framework"
layout: publication
pub_id: data-driven-cohesive-zone-gsm
permalink: /publications/data-driven-cohesive-zone-gsm/
figure_caption: "A single learned cohesive model reproduces normal and tangential traction-separation curves across mode mixities, including held-out cases, and recovers the fracture energy as a function of mode mixity."
---

Cohesive zone models describe fracture and interfacial failure through a traction-separation law across a crack. Most formulations prescribe a problem-specific analytical law plus phenomenological unloading and reloading rules, so different cohesive behaviors call for separately built models, and fixed functional forms can miss plateaus, long softening tails or irregular, mode-dependent shapes.

This paper develops a single learnable cohesive formulation within the generalized standard materials framework, so the thermodynamic structure stays fixed while the constitutive functions are learned from data. The surface free energy is split into active and contact parts; the active energy is an input-convex neural network, and the inverse damage resistance, which depends on mode mixity, is a monotone neural network. Convexity, monotonicity, normalization and damage irreversibility are built into the networks, and the damage update is explicit, with no local nonlinear solve.

**Key findings**

- Material-point studies reproduce plateaus, extended softening tails, irregular softening, nonlinear unloading and distinct Mode I and Mode II behavior, with non-negative dissipation.
- Calibrated on several mode mixities, the model fits bilinear, exponential and PPR-type mixed-mode laws and predicts held-out intermediate mixities.
- With only pure-mode data, the intermediate mixed-mode response is not uniquely determined.
