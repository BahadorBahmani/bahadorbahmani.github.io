---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
---

## Uncertainty Quantification in Stochastic Systems

<div style="text-align: justify;">
Neural Chaos is a neural-network-based formulation inspired by Polynomial Chaos Expansion (PCE) for modeling stochastic processes involving high-dimensional and statistically dependent inputs. While PCE is widely used in engineering applications, it may require special treatment when handling dependent random variables and can face scalability challenges due to its reliance on polynomial basis functions and tensor product structures. Neural Chaos, grounded in the same spectral representation formalism, replaces polynomial bases with neural-network–parameterized functions learned directly from data. Built on the RINO framework, it constructs basis functions that are orthogonal with respect to the underlying probability measure, enabling efficient spectral representations for uncertainty quantification in stochastic systems.
</div>

<p align="center">
  <img src="/images/UQ/neural_chaos.png" alt="uq" width="800px" />
</p>

<!--
Polynomial Chaos Expansion (PCE) is a well-established method for modeling stochastic processes in many engineering applications. However, it requires special treatment when dealing with random variables that exhibit statistical dependence. Additionally, due to its reliance on polynomial basis functions and tensor product spaces, PCE often faces challenges in handling high-dimensional random variables—an area where neural networks are known to perform well. To address these limitations, we introduce Neural Chaos, a method grounded in the same formalism as PCE—namely, the spectral representation theorem—but with a key difference: the basis functions are parameterized by neural networks and are not predefined. Building on the RINO framework, we propose an algorithm to learn these basis functions over joint random variables without requiring a tensor product structure or prior knowledge of their independence. The learned basis functions remain orthogonal with respect to the data-driven probability measure. This approach opens up new possibilities for simulating stochastic processes governed by complex, high-dimensional random variables.
-->

## Operator Learning and Reduced Order Modeling

<div style="text-align: justify;">
Most operator learning methods require input or output function spaces to be discretized on the same grid, limiting their applicability when data is defined on varying grids across realizations, such as in multiscale simulations. Our method, Resolution-Independent Neural Operator (RINO), addresses this by introducing a dictionary learning algorithm that extracts orthogonal, smooth basis functions from irregularly discretized data. These functions serve to project arbitrary discretized fields onto a finite-dimensional embedding space in which operator learning is conducted. This approach is interpretable from classical approximation theory and provides a natural error metric for detecting out-of-distribution samples.
</div>

<p align="center">
  <img src="/images/operator_rom/summary_methods_website.png" alt="opr-learn-rom" width="800px" />
</p>

## Interpretable Material Model Discovery with Machine Learning

<div style="text-align: justify;">
Traditional constitutive models in mechanics rely on handcrafted equations rooted in phenomenological assumptions. While recent approaches using neural networks have enabled learning such models directly from data—experimental or computational—they often result in black-box or, at best, gray-box formulations, making it difficult to interpret how inputs (e.g., strains) are mapped to outputs (e.g., stress or strain energy). In this research, we introduce a scalable and interpretable framework that combines neural networks and symbolic regression for material model discovery. The key idea is a two-step decomposition of high-dimensional constitutive functions. First, we learn a low-rank representation by expressing the target function as an additive combination of univariate basis functions, each parameterized by a neural network. This step allows easy integration of physical constraints via differentiable programming. Second, we generate synthetic data from the learned basis functions and apply symbolic regression to extract concise, human-readable equations. The final constitutive model is assembled from these symbolic components, yielding interpretable and thermodynamically consistent formulations that reflect the kind of equations an expert mechanician might derive. We have demonstrated the effectiveness of this neural-symbolic scheme in discovering material models for a range of complex materials, including soft materials under large deformations, plastic yield surfaces of porous metals, granular materials, and others. This approach bridges the gap between black-box learning and classical theory, offering a principled pathway toward transparent, data-driven constitutive modeling.
</div>

<p align="center">
  <img src="/images/interp_ai/hybrid.png" alt="interp_ai" width="800px" />
</p>

## Manifold-Embedding Data-Driven Mechanics

<div style="text-align: justify;">
Model-free distance-minimization methods provide a data-driven alternative to classical constitutive modeling by directly incorporating stress-strain data into field equations—without assuming an explicit stress-strain relationship. In this formulation, the governing equations become optimization problems that minimize the distance between material data and balance laws. Earlier approaches relied on energy-based Euclidean distances in phase space, which can misrepresent the geometry of nonlinear materials, especially with sparse or noisy data. To address this, we propose a new formulaiton that embeds the data into a latent space specifically constructed to admit a Euclidean structure. This enables the optimization to be performed via linear projection, reducing computational cost. The framework remains hybrid: local data searches can still be conducted within the latent space when needed. To better preserve the material data geometry, we design an isometric embedding that maintains local distances between data points before and after projection. This manifold-embedded approach offers a flexible continuum between model-based and model-free paradigms, adapting to the quality and availability of data. We extend the method to coupled multiphysics problems such as poroelasticity, introducing an additive distance metric over the joint phase space. This allows selective modeling—using data-driven approaches for some fields and traditional models for others. Finally, to ensure scalability, we develop a KD-tree–based spectral search algorithm tailored to the model-free setting, achieving orders-of-magnitude improvements in data retrieval efficiency.
</div>

<p align="center">
  <img src="/images/model-free/model-free.png" alt="interp_ai" width="800px" />
</p>

## Stochastic Multiscale Fracture Modeling with Discontinuous Galerkin Method

To be added

<p align="center">
  <img src="/images/DG/dg-damage-fracture.png" alt="dg" width="800px" />
</p>


## Multiphysics Contact Mechanics in Fractured Media with the Extended Finite Element Method

<div style="text-align: justify;">
The eXtended Finite Element Method (XFEM) is a powerful numerical technique for solving partial differential equations with discontinuous solutions. By allowing the computational mesh to remain independent of discontinuities or sharp gradients, XFEM significantly simplifies mesh generation and interface tracking compared to standard FEM approaches. This makes it particularly effective for simulating fractured domains and contact mechanisms, where interfaces are implicitly represented using level set functions. In this work, we present a new XFEM-based formulation to model contact, bonding, and debonding phenomena across fracture surfaces under fully coupled thermo-mechanical loading. Specifically, we introduce an efficient algorithm to capture nonlinear interactions between mechanical and thermal fields at fracture interfaces. A key feature of our approach is the incorporation of pressure-dependent heat conduction across crack surfaces, enabling more accurate simulation of heat transfer in fractured materials.
</div>

<p align="center">
  <img src="/images/xfem/xfem-tm-contact.png" alt="interp_ai" width="800px" />
</p>

