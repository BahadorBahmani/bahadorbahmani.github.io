---
title: "A Differentiable Framework for Inverse Identification of Heterogeneous Cohesive Laws"
layout: publication
pub_id: differentiable-heterogeneous-cohesive-laws
permalink: /publications/differentiable-heterogeneous-cohesive-laws/
figure_caption: "A double-cantilever beam with a spatially varying cohesive interface: the load drops and recovers as the crack crosses tougher and weaker segments."
animations:
  - src: "/images/publications/differentiable-heterogeneous-cohesive-laws/dcb_inverse.gif"
    caption: "Inverse identification on the double-cantilever beam: over training, the predicted force-displacement curve converges to the data and the identified traction-separation laws converge to the truth."
  - src: "/images/publications/differentiable-heterogeneous-cohesive-laws/c3f_forward.gif"
    caption: "Three-fiber composite with heterogeneous fiber-matrix interfaces, each carrying a spatially varying latent coordinate, debonding under applied displacement."
  - src: "/images/publications/differentiable-heterogeneous-cohesive-laws/c3f_inverse.gif"
    caption: "Identification on the composite: the latent field and the Mode I and Mode II traction-separation laws converge to the truth over training."
  - src: "/images/publications/differentiable-heterogeneous-cohesive-laws/c3f_error.gif"
    caption: "Force data alone reproduce the force-displacement curve but leave large errors in the interface laws; adding DIC strain data recovers them."
  - src: "/images/publications/differentiable-heterogeneous-cohesive-laws/c3f_bilinear.gif"
    caption: "A conventional bilinear cohesive model versus the learned prior: the prior reaches a far lower loss and much smaller interface errors."
  - src: "/images/publications/differentiable-heterogeneous-cohesive-laws/c3f_bo.gif"
    caption: "Bayesian optimization versus adjoint-based identification: the adjoint gradients drive the loss several orders of magnitude lower."
---

Traction-separation laws govern fracture and debonding in bonded structures and composites, but they can rarely be measured directly. They must instead be inferred from structural data such as force-displacement curves and deformation fields, and this inverse problem can be badly ill-posed because different cohesive laws may give nearly identical global responses.

This paper develops a differentiable finite element framework, built on an intrinsic cohesive-zone formulation, that identifies cohesive laws from global force-displacement histories and sparse strain measurements. Physics-constrained neural networks represent flexible, thermodynamically structured cohesive laws, and gradients come from automatic differentiation and a discrete adjoint that tracks history-dependent damage. To capture spatially varying interfaces, the paper extends learned constitutive priors to irreversible damage: a shared low-dimensional family of cohesive laws, with local variation described by latent coordinates.

**Key findings**

- In double-cantilever beam and fiber-matrix composite examples, matching the global force-displacement response does not guarantee recovery of the true cohesive laws.
- Adding spatially resolved strain measurements substantially improves identification, even when responses are restricted by a learned prior.
- The learned representation with adjoint-based identification compares favorably with conventional bilinear cohesive models and Bayesian optimization.
