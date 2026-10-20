---
title: "A Differentiable Framework for Inverse Identification of Heterogeneous Cohesive Laws"
layout: publication
pub_id: differentiable-heterogeneous-cohesive-laws
permalink: /publications/differentiable-heterogeneous-cohesive-laws/
---

Traction-separation laws govern fracture and debonding in bonded structures and composites, but they can rarely be measured directly. They must instead be inferred from structural data such as force-displacement curves and deformation fields, and this inverse problem can be badly ill-posed because different cohesive laws may give nearly identical global responses.

This paper develops a differentiable finite element framework, built on an intrinsic cohesive-zone formulation, that identifies cohesive laws from global force-displacement histories and sparse strain measurements. Physics-constrained neural networks represent flexible, thermodynamically structured cohesive laws, and gradients come from automatic differentiation and a discrete adjoint that tracks history-dependent damage. To capture spatially varying interfaces, the paper extends learned constitutive priors to irreversible damage: a shared low-dimensional family of cohesive laws, with local variation described by latent coordinates.

**Key findings**

- In double-cantilever beam and fiber-matrix composite examples, matching the global force-displacement response does not guarantee recovery of the true cohesive laws.
- Adding spatially resolved strain measurements substantially improves identification, even when responses are restricted by a learned prior.
- The learned representation with adjoint-based identification compares favorably with conventional bilinear cohesive models and Bayesian optimization.
