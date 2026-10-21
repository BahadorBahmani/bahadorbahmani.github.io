---
published: false
title: "Manifold embedding data-driven mechanics"
layout: publication
pub_id: manifold-embedding-data-driven-mechanics
permalink: /publications/manifold-embedding-data-driven-mechanics/
figure_caption: "The classical distance-minimization solver (left) compared with the new approach (right), which searches for the closest material state in a learned Euclidean embedding of the data."
---

Model-free, data-driven mechanics replaces constitutive laws by searching a material database for the data points closest to states that satisfy the balance laws. How this distance is measured matters: standard weighted energy norms treat the data as if they lie in a flat Euclidean space, which is often unrealistic when data are sparse, unevenly spread or lie on a curved constitutive manifold.

This paper trains an invertible neural network to map material data from the constitutive manifold onto a lower-dimensional Euclidean vector space and back. The closest-point search is then carried out in this learned space, which gives a notion of distance more consistent with the geometry of the data and avoids an expensive combinatorial search.

**Key findings**

- The embedding makes model-free simulations more robust and accurate when data are limited or unevenly distributed.
- It can significantly speed up simulations when data are abundant and high-dimensional.
- Examples with a 1D bar, a truss system, nonlinear conduction and nonlinear elasticity compare the method against classical energy norms.
