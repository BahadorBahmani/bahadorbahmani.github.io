---
title: "Constitutive Priors for Inverse Design"
layout: publication
pub_id: constitutive-priors-inverse-design
permalink: /publications/constitutive-priors-inverse-design/
caption_align: left
figure_in_body: true
section_style: numbered
---

This page was written by Jinkyo Han with the help of AI (Claude by Anthropic).

## Overview
{: style="margin-top: 0.5em"}

Additive manufacturing and multimaterial fabrication make it possible to tune how each part of a structure responds to load. Inverse design methods usually fix a constitutive model and optimize its parameters, but often only stress-strain data are available, without the material or microstructural descriptors that explain differences between them. This work instead relaxes the constitutive model class itself and searches directly over a family of admissible constitutive behaviors learned from data.

{% include pub-animation.html src="/images/publications/constitutive-priors-inverse-design.png" width="85%" caption="A latent family of material responses is learned from stress-strain data alone, and inverse design picks responses from that family without needing the underlying material descriptors." %}

This paper introduces a constitutive prior: a low-dimensional latent representation of a family of thermodynamically admissible material laws, learned jointly from stress-strain responses with an energy-based, partially input-convex neural network that enforces constitutive constraints by construction. Spatially varying latent variables are then optimized, subject to equilibrium and with adjoint gradients, so that a deformed elastic network matches a target shape. This is not heterogeneous parameter identification within a single constitutive equation, but heterogeneous constitutive-model identification posed directly in function space. A correspondence-free point cloud objective, homotopy continuation and affine registration make this nonconvex problem more robust.

## Results

The training data are point clouds of material responses, and the latent coordinate is learned jointly with the parameters of the partially input-convex neural network.

{% include pub-animation-pair.html left="data.png" left_width="36%" left_offset="2.39%" right="model.png" right_width="38.18%" caption="Stress-strain data, which the trained model lifts to a smooth surface over a learned latent coordinate z." %}

Optimizing the latent variable of each truss member yields a truss design whose deformed shape matches the target.

{% include pub-animation.html src="truss_heart.gif" width="70%" caption="Heart-shaped target: the square truss is expanded toward the heart shape. The right panel shows the nonlinear material response of each element, colored to match the left panel." %}

The framework is also tested on other geometries, including a NACA 2412 airfoil and a cracked geometry with a notch.

{% include pub-animation-pair.html left="truss_airfoil.gif" left_width="32.12%" right="truss_fracture.gif" right_width="40%" right_offset="3.53%" %}

## Methods

The inverse design is a PDE-constrained optimization problem: the adjoint state method is applied at the equilibrium state to obtain the gradient. The shape mismatch is measured directly on point sets through the Chamfer distance, so the target and deformed configurations can have different discretizations, resolutions or even topologies.

{% include pub-animation.html src="main_scheme_r2.png" width="80%" caption="Illustration of the framework." %}

Letting the constitutive behavior vary in space makes the optimization challenging, so homotopy continuation is applied to the target shape, moving it gradually from the initial geometry to the final target.

{% include pub-animation.html src="homotopy.gif" width="34%" %}

When an initial target shape is not available, it is approximated by affine registration: an affine map matches the point cloud of the final target shape to the reference shape by minimizing the Chamfer distance.

{% include pub-animation.html src="affine_map.gif" width="40%" caption="Affine registration of the cracked shape onto the reference square." %}

## Key findings

- The framework recovers spatially varying material distributions that produce prescribed global deformations in several nonlinear elastic network examples.
- The point cloud objective lets target and design geometries use different discretizations, with no nodal correspondence or interpolation.
- Compared with the commonly used MMA optimizer, the approach needs fewer iterations and reaches lower objective values.

## Related work

The idea of the present work has since been applied to fracture modeling:

- [A Differentiable Framework for Inverse Identification of Heterogeneous Cohesive Laws]({{ '/publications/differentiable-heterogeneous-cohesive-laws/' | relative_url }})
- [Data-Driven Cohesive Zone Modeling within the Generalized Standard Materials Framework]({{ '/publications/data-driven-cohesive-zone-gsm/' | relative_url }})
