---
title: "Data-Driven Cohesive Zone Modeling within the Generalized Standard Materials Framework"
layout: publication
pub_id: data-driven-cohesive-zone-gsm
permalink: /publications/data-driven-cohesive-zone-gsm/
figure_in_body: true
section_style: numbered
figure_caption: "A single learned cohesive model reproduces normal and tangential traction-separation curves across mode mixities, including held-out cases, and recovers the fracture energy as a function of mode mixity."
byline: "This page was written by Sida Hao with the help of AI (Claude by Anthropic)."
---

## Overview

Cohesive zone models describe fracture and interfacial failure through a traction-separation law across a crack. Most formulations prescribe a problem-specific analytical law together with phenomenological rules for unloading and reloading, so different cohesive behaviors call for separately built models, and fixed functional forms can miss plateaus, long softening tails or irregular, mode-dependent shapes.

{% include pub-animation.html src="czm_schematic.png" width="640px" caption="A cohesive zone model: (a) a process zone ahead of the crack bridges its faces with a traction t that resists their separation δ; (b) the traction-separation law rises to a cohesive strength T and then softens to zero, with the area under the curve equal to the fracture energy Gc." %}

This paper develops a single learnable cohesive formulation within the generalized standard materials framework: the thermodynamic structure stays fixed, while the constitutive functions that generate the response are learned from data.

**Key features**

*One formulation, many cohesive laws.* Plateaus, extended softening tails, irregular softening, nonlinear unloading, distinct Mode I and Mode II behavior and several classical mixed-mode laws all come from the same thermodynamically structured representation, rather than from a law-specific model.

*Thermodynamic consistency by construction.* Convexity, monotonicity, normalization and damage irreversibility are built into the networks, so damage stays irreversible and dissipation non-negative throughout the loading history.

*Explicit damage update.* Parameterizing the inverse damage resistance directly avoids a local nonlinear inversion at every constitutive evaluation.

## Results

Calibrated on several mode mixities, one model reproduces three classical mixed-mode cohesive laws (an exponential law, a bilinear law with a power-law mixed-mode criterion, and the PPR potential) and predicts the held-out intermediate mixities, together with the fracture energy as a function of mode mixity.

{% include pub-animation.html src="mixed_mode.png" width="100%" caption="Exponential mixed-mode law: normal (left) and tangential (center) traction-separation responses colored by mode mixity β, with filled markers for calibration data and open markers for held-out mixities, and the predicted fracture energy against the analytical reference (right)." %}

Under non-proportional loading, where the mode mixity changes along the path, two paths that open the interface in opposite orders reach the same final separation, damage and traction state but dissipate different amounts of energy.

{% include pub-animation.html src="nonproportional.png" width="660px" caption="Non-proportional loading of the learned exponential-law model: (a) normal-then-shear (blue) and shear-then-normal (red) paths, (b) cumulative dissipation and damage, and (c, d) normal and shear tractions along each path." %}

## Methods

The surface free energy is split into active and contact contributions, and irreversible damage evolution is governed by a learned, mode-dependent damage resistance. The active energy is an input-convex neural network (ICNN), corrected so that energy and traction vanish at the undeformed state.

{% include pub-animation.html src="icnn.png" width="560px" caption="The input-convex neural network that represents the active energy as a function of the separation measures." %}

The inverse damage resistance is a monotone neural network (MNN) of the energy release rate and the mode mixity. Parameterizing the inverse directly gives an explicit damage update, with no local nonlinear solve during constitutive evaluation. Convexity, monotonicity, normalization and damage irreversibility are all built into the two networks.

{% include pub-animation.html src="mnn.png" width="560px" caption="The monotone neural network that represents the inverse damage resistance, increasing in the energy release rate Y and depending on the mode mixity β." %}
