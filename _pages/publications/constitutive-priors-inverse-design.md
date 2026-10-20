---
title: "Constitutive Priors for Inverse Design"
layout: publication
pub_id: constitutive-priors-inverse-design
permalink: /publications/constitutive-priors-inverse-design/
figure_caption: "A latent family of material responses is learned from stress-strain data alone, and inverse design picks responses from that family without needing the underlying material descriptors."
---

Additive manufacturing and multimaterial fabrication make it possible to tune how each part of a structure responds to load. Inverse design methods usually fix a constitutive model and optimize its parameters, but often only stress-strain data are available, without the material or microstructural descriptors that explain differences between them.

This paper introduces a constitutive prior: a low-dimensional latent representation of a family of material laws, learned jointly from stress-strain responses with an energy-based, partially input-convex neural network that enforces constitutive constraints by construction. Spatially varying latent variables are then optimized, subject to equilibrium and with adjoint gradients, so that a deformed elastic network matches a target shape. A correspondence-free point cloud objective, homotopy continuation and affine registration make this nonconvex problem more robust.

**Key findings**

- The framework recovers spatially varying material distributions that produce prescribed global deformations in several nonlinear elastic network examples.
- The point cloud objective lets target and design geometries use different discretizations, with no nodal correspondence or interpolation.
- Compared with the commonly used MMA optimizer, the approach needs fewer iterations and reaches lower objective values.
