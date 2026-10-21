---
published: false
title: "Synthesizing controlled microstructures of porous media using generative adversarial networks and reinforcement learning"
layout: publication
pub_id: gan-rl-porous-microstructures
permalink: /publications/gan-rl-porous-microstructures/
figure_caption: "Overview of the GAN-AC framework: an actor network tunes the inputs of a 3D GAN generator until the synthetic microstructure reaches the user's target properties."
---

Synthetic microstructures act as digital twins for material modeling, supplying samples on which direct numerical simulations can populate material databases. Generating microstructures that are both realistic and have specified physical properties is difficult, so they are often built from rough approximations that misrepresent real materials.

This paper combines a 3D generative adversarial network (GAN), extended to produce realistic microstructures of arbitrary size, with actor-critic reinforcement learning. The actor tunes the GAN's morphology parameters, and the critic judges how close the resulting quantities of interest are to the targets, so that generated samples both look real and match user-defined properties. The framework is validated on micro-CT scans of Bentheim sandstone.

**Key findings**

- On 500 held-out tests, generated microstructures matched targeted porosity, specific surface area and effective permeability with average errors of about 2.5%, 3.5% and 4.1%.
- The synthetic microstructures are diverse and realistic in both qualitative and quantitative comparisons with real samples.
- Compared with Bayesian optimization, the actor-critic approach reached similar solution quality with about three times fewer objective function evaluations.
