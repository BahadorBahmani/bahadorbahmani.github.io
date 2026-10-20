---
title: "A Differentiable Framework for Inverse Identification of Heterogeneous Cohesive Laws"
layout: publication
pub_id: differentiable-heterogeneous-cohesive-laws
permalink: /publications/differentiable-heterogeneous-cohesive-laws/
figure_caption: "A double-cantilever beam with a spatially varying cohesive interface: the load drops and recovers as the crack crosses tougher and weaker segments."
---

<figure class="pub-figure">
  <img src="{{ '/images/publications/differentiable-heterogeneous-cohesive-laws/dcb_inverse.gif' | relative_url }}" alt="Inverse identification on the double-cantilever beam: over training, the predicted force-displacement curve converges to the data and the identified traction-separation laws converge to the truth." loading="lazy">
  <figcaption>Inverse identification on the double-cantilever beam: over training, the predicted force-displacement curve converges to the data and the identified traction-separation laws converge to the truth.</figcaption>
</figure>

Cohesive laws, the traction-separation relations that govern how interfaces debond, can rarely be measured directly. They must be inferred from remote measurements such as force-displacement histories and sparse strain fields. This inverse problem is often ill-posed, and spatially heterogeneous interfaces make it harder still, since quite different interface laws can produce nearly the same global response.

Building on recent work on [data-driven constitutive priors]({{ '/publications/constitutive-priors-inverse-design/' | relative_url }}), this paper regularizes the problem by searching over a low-dimensional manifold of physically admissible cohesive responses rather than an unconstrained parameter space. The cohesive laws are formulated within the generalized standard materials framework and represented by structure-preserving neural networks, which guarantee thermodynamic consistency by construction while keeping the flexibility of neural networks. Latent coordinates let the cohesive behavior vary along the interface.

<figure class="pub-figure">
  <img src="{{ '/images/publications/differentiable-heterogeneous-cohesive-laws/c3f_forward.gif' | relative_url }}" alt="Three-fiber composite with heterogeneous fiber-matrix interfaces, each carrying a spatially varying latent coordinate, debonding under applied displacement." loading="lazy">
  <figcaption>Three-fiber composite with heterogeneous fiber-matrix interfaces, each carrying a spatially varying latent coordinate, debonding under applied displacement.</figcaption>
</figure>
<figure class="pub-figure">
  <img src="{{ '/images/publications/differentiable-heterogeneous-cohesive-laws/c3f_inverse.gif' | relative_url }}" alt="Identification on the composite: the latent field and the Mode I and Mode II traction-separation laws converge to the truth over training." loading="lazy">
  <figcaption>Identification on the composite: the latent field and the Mode I and Mode II traction-separation laws converge to the truth over training.</figcaption>
</figure>

**Key capabilities**

*Local measurements matter.* Reproducing the global force-displacement response does not by itself guarantee that the true cohesive laws are recovered. Adding spatially resolved strain measurements, such as digital image correlation (DIC), substantially improves identification.

<figure class="pub-figure">
  <img src="{{ '/images/publications/differentiable-heterogeneous-cohesive-laws/c3f_error.gif' | relative_url }}" alt="Force data alone reproduce the force-displacement curve but leave large errors in the interface laws; adding DIC strain data recovers them." loading="lazy">
  <figcaption>Force data alone reproduce the force-displacement curve but leave large errors in the interface laws; adding DIC strain data recovers them.</figcaption>
</figure>

*Beyond classical cohesive laws.* The learned constitutive prior overcomes the representational limits of conventional cohesive models, even when their parameters are allowed to vary spatially.

<figure class="pub-figure">
  <img src="{{ '/images/publications/differentiable-heterogeneous-cohesive-laws/c3f_bilinear.gif' | relative_url }}" alt="A spatially varying bilinear cohesive model versus the learned prior: the prior reaches a far lower loss and much smaller interface errors." loading="lazy">
  <figcaption>A spatially varying bilinear cohesive model versus the learned prior: the prior reaches a far lower loss and much smaller interface errors.</figcaption>
</figure>

*Efficient inverse identification.* The intrinsic cohesive finite element formulation is fully differentiable, so sensitivities come from a discrete adjoint that accounts for the history-dependent evolution of interfacial damage. In high-dimensional inverse problems, this adjoint-based identification outperforms derivative-free Bayesian optimization.

<figure class="pub-figure">
  <img src="{{ '/images/publications/differentiable-heterogeneous-cohesive-laws/c3f_bo.gif' | relative_url }}" alt="Bayesian optimization versus adjoint-based identification on a fiber-matrix composite: the adjoint gradients drive the loss several orders of magnitude lower and recover the interface laws." loading="lazy">
  <figcaption>Bayesian optimization versus adjoint-based identification on a fiber-matrix composite: the adjoint gradients drive the loss several orders of magnitude lower and recover the interface laws.</figcaption>
</figure>
