---
title: "Constitutive Priors for Inverse Design"
layout: publication
pub_id: constitutive-priors-inverse-design
permalink: /publications/constitutive-priors-inverse-design/
caption_align: left
figure_width: "85%"
figure_caption: "A latent family of material responses is learned from stress-strain data alone, and inverse design picks responses from that family without needing the underlying material descriptors."
---


Additive manufacturing and multimaterial fabrication make it possible to tune how each part of a structure responds to load. Inverse design methods usually fix a constitutive model and optimize its parameters, but often only stress-strain data are available, without the material or microstructural descriptors that explain differences between them. This work instead relaxes the constitutive model class itself and searches directly over a family of admissible constitutive behaviors learned from data.

This paper introduces a constitutive prior: a low-dimensional latent representation of a family of thermodynamically admissible material laws, learned jointly from stress-strain responses with an energy-based, partially input-convex neural network that enforces constitutive constraints by construction. Spatially varying latent variables are then optimized, subject to equilibrium and with adjoint gradients, so that a deformed elastic network matches a target shape. This is not heterogeneous parameter identification within a single constitutive equation, but heterogeneous constitutive-model identification posed directly in function space. A correspondence-free point cloud objective, homotopy continuation and affine registration make this nonconvex problem more robust.

## Results

{% include pub-animation-pair.html left="data.png" left_width="40%" left_offset="1.12%" right="model.png" right_width="38.18%" %}

{% include pub-animation.html src="truss_heart.gif" width="70%" caption="Heart-shaped target: the square truss is expanded toward the heart shape. The right panel shows the nonlinear material response of each element, colored to match the left panel." %}

{% include pub-animation-pair.html left="truss_airfoil.gif" left_width="32.12%" right="truss_fracture.gif" right_width="40%" right_offset="3.53%" caption="Results on other geometries: a NACA 2412 airfoil (left) and a cracked geometry with a notch (right)." %}

## Methods

The inverse design is a PDE-constrained optimization problem: the adjoint state method is applied at the equilibrium state to obtain the gradient. The shape mismatch is measured directly on point sets through the Chamfer distance, so the target and deformed configurations can have different discretizations, resolutions or even topologies.

{% include pub-animation.html src="main_scheme_r2.png" width="80%" caption="Illustration of the framework." %}

Letting the constitutive behavior vary in space makes the optimization challenging, so homotopy continuation is applied to the target shape, moving it gradually from the initial geometry to the final target.

{% include pub-animation.html src="homotopy.gif" width="40%" %}

When an initial target shape is not available, it is approximated by affine registration.

{% include pub-animation.html src="affine_map.gif" width="40%" caption="Affine registration of the cracked shape onto the reference square." %}



**Key findings**

- The framework recovers spatially varying material distributions that produce prescribed global deformations in several nonlinear elastic network examples.
- The point cloud objective lets target and design geometries use different discretizations, with no nodal correspondence or interpolation.
- Compared with the commonly used MMA optimizer, the approach needs fewer iterations and reaches lower objective values.

## Related work

The same idea has since been applied to fracture modeling:

- [A Differentiable Framework for Inverse Identification of Heterogeneous Cohesive Laws]({{ '/publications/differentiable-heterogeneous-cohesive-laws/' | relative_url }})
- [Data-Driven Cohesive Zone Modeling within the Generalized Standard Materials Framework]({{ '/publications/data-driven-cohesive-zone-gsm/' | relative_url }})
