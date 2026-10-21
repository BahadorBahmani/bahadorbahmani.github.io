---
title: "A Multimodal Conditional Mixture Model with Distribution-Level Physics Priors"
layout: publication
pub_id: multimodal-conditional-mixture
permalink: /publications/multimodal-conditional-mixture/
figure_in_body: true
caption_align: left
section_style: numbered
---

## Overview

Many physical systems have more than one admissible outcome for the same input, because of bifurcations, regime switching or non-unique mechanisms. Predicting the full conditional distribution of such outcomes is needed, but modern generative models are data-hungry, hard to constrain with physics, and often difficult to interpret.

{% include pub-animation-pair.html left="circle_left.png" left_width="28%" center="circle_center.png" center_width="28%" right="circle_right.png" right_width="28%" caption="On the circle data (left), the mixture components compete to cover the samples (center). After training, samples drawn from the closed-form mixture cover the circle (right)." %}

This paper revisits mixture density networks (MDNs), which represent a conditional distribution as a finite mixture of simple Gaussian components, as a physics-informed alternative. Physical knowledge, such as governing equations, thermodynamic monotonicity or known class labels, is added through regularization terms applied to each mixture component. The framework is tested on bifurcations, stochastic differential equations, shock Hugoniot data for silicon carbide and a reaction-diffusion equation, and is compared with conditional flow matching.

{% include pub-animation.html src="schematic.png" width="80%" caption="Illustration of the MDN architecture and the proposed multimodal conditional modeling framework." %}

## Results

On bifurcation data, each mixture component follows one branch, and the component weights shift as new branches appear past the bifurcation point.

{% include pub-animation-pair.html left="ex1_mu_sigma.png" left_width="35%" right="ex1_pi.png" right_width="35%" caption="Trained mixture components on the bifurcation diagram data: the learned means and standard deviations of each component (left) and the component weights (right)." %}

Under comparable model capacity, the MDN resolves the distinct response modes, compared here with conditional flow matching.

{% include pub-animation-pair.html left="ex1_samples_mdn.png" left_width="30%" center="ex1_samples_cfm.png" center_width="30%" right="ex1_conditional_lam0.8.png" right_width="30%" caption="Samples from the trained MDN (left) and from conditional flow matching, which requires iterative inference to sample (center). The MDN output is analytic and agrees well with the data, shown here at λ = 0.8 (right)." %}

Prior knowledge of the physical system can be incorporated into MDN training to improve the behavior of the learned components.

{% include pub-animation-pair.html left="shock_left.gif" left_width="40%" right="shock_right.gif" right_width="40%" caption="Training of the MDN on shock Hugoniot data, without prior knowledge (left) and with prior knowledge (right)." %}


## Key findings

- The mixture model matches conditional flow matching at similar model size and training effort, while being simpler to train and sample.
- Adding physics priors and class-conditioning improves agreement with known physical behavior without extra data or separate models.
- The closed-form mixture makes components interpretable and gives conditional means and variances directly, with no Monte Carlo sampling.
