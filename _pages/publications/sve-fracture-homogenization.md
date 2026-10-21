---
published: false
title: "Automated homogenization-based fracture analysis: Effects of SVE size and boundary condition"
layout: publication
pub_id: sve-fracture-homogenization
permalink: /publications/sve-fracture-homogenization/
---

Fracture in particulate composites is strongly affected by microscale inhomogeneities and varies from sample to sample. This paper uses statistical volume elements (SVEs) to capture these variations when homogenizing the elastic and fracture properties of ZrB2-SiC, a two-phase composite often used as a thermal coating.

At the mesoscale, 2D finite element models are built automatically with a non-iterative mesh generation algorithm (CISAMR). SVEs are analyzed under mixed, traction and minimal kinematic boundary conditions to obtain angle-dependent tensile and shear fracture strengths and elastic stiffnesses. At the macroscale, the homogenized strengths define an inhomogeneous strength field, and fracture under uniaxial tension and thermal strain is simulated with the asynchronous spacetime discontinuous Galerkin (aSDG) method.

**Key findings**

- Homogenized fracture strengths depend strongly on SVE size and on the specific arrangement of inclusions, even at similar volume fractions.
- Elastic properties depend mainly on the volume fraction.
- As SVE size increases, mean strength decreases while mean bulk modulus stays almost constant.
