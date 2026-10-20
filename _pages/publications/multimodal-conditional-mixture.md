---
title: "A Multimodal Conditional Mixture Model with Distribution-Level Physics Priors"
layout: publication
pub_id: multimodal-conditional-mixture
permalink: /publications/multimodal-conditional-mixture/
figure_caption: "A single network maps the inputs to the weights, means and spreads of a mixture distribution, trained on data together with prior physical knowledge to capture several solution branches at once."
---

Many physical systems have more than one admissible outcome for the same input, because of bifurcations, regime switching or non-unique mechanisms. Predicting the full conditional distribution of such outcomes is needed, but modern generative models are data-hungry, hard to constrain with physics, and often difficult to interpret.

This paper revisits mixture density networks, which represent a conditional distribution as a finite mixture of simple Gaussian components, as a physics-informed alternative. Physical knowledge, such as governing equations, thermodynamic monotonicity or known class labels, is added through regularization terms applied to each mixture component. The framework is tested on bifurcations, stochastic differential equations, shock Hugoniot data for silicon carbide and a reaction-diffusion equation, and is compared with conditional flow matching.

**Key findings**

- The mixture model matches conditional flow matching at similar model size and training effort, while being simpler to train and sample.
- Adding physics priors and class-conditioning improves agreement with known physical behavior without extra data or separate models.
- The closed-form mixture makes components interpretable and gives conditional means and variances directly, with no Monte Carlo sampling.
