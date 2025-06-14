---
layout: archive
title: "Papers"
permalink: /publications/
author_profile: true
---
2025
----
1. [**Neural Chaos: A Spectral Stochastic Neural Operator**](https://arxiv.org/abs/2502.11835)\
   **B. Bahmani**, et al., arxiv.
2. [**A Resolution Independent Neural Operator**](https://www.sciencedirect.com/science/article/abs/pii/S0045782525003858)\
   **B. Bahmani**, et al., *Computer Methods in Applied Mechanics and Engineering*.

2024
----
1. [**Physics-constrained Symbolic Model Discovery for Polyconvex Incompressible Hyperelastic Material**](https://onlinelibrary.wiley.com/doi/full/10.1002/nme.7473)\
   **B. Bahmani** and W. Sun, *International Journal for Numerical Methods in Engineering*.
2. [**Discovering Interpretable Elastoplasticity Models via the Neural Polynomial Method enabled Symbolic Regression**](https://www.sciencedirect.com/science/article/pii/S0045782524000835)\
   **B. Bahmani**, et al., *Computer Methods in Applied Mechanics and Engineering*.
3. [**A Review on Data-Driven Constitutive Laws for Solids**](https://link.springer.com/article/10.1007/s11831-024-10196-2)\
   J. Fuhg, G. Padmanabha, N. Bouklas, **B. Bahmani**, et al., *Archives of Computational Methods in Engineering*.

2023
----
1. [**Manifold embedding data-driven mechanics**](https://www.sciencedirect.com/science/article/pii/S0022509622001259)\
   **B. Bahmani** and W. Sun, *Journal of Mechanics and Physics of Solids*.
2. [**Distance-preserving manifold de-noising for data-driven mechanics**](https://www.sciencedirect.com/science/article/pii/S0045782522008131)\
   **B. Bahmani** and W. Sun, *Computer Methods in Applied Mechanics and Engineering*.
3. [**Equivariant geometric learning for digital rock physics: estimating formation factor and effective permeability tensors from Morse graph**](https://www.dl.begellhouse.com/journals/61fd1b191cf7e96f,1f61097b2b8038e0,755c1ea40d25b4c7.html)\
   C. Cai, N. Vlassis, L. Magee, R. Ma, Z. Xiong, **B. Bahmani**, et al., *International Journal for Multiscale Computational Engineering*.

2022
----
1. [**Data-driven discovery of interpretable causal relations for deep learning material laws with uncertainty quantification**](https://link.springer.com/article/10.1007/s10035-021-01137-y)\
   X. Sun, **B. Bahmani**, et al., *Granular Matter*.
2. [**Synthesizing controlled microstructures of porous media using generative adversarial networks and reinforcement learning**](https://www.nature.com/articles/s41598-022-12845-7)\
   P. Nguyen, N. Vlassis, **B. Bahmani**, et al., *Scientific Reports*.

2021
----
1. [**A kd-tree-accelerated hybrid data-driven/model-based approach for poroelasticity problems with multi-fidelity multi-physics data**](https://www.sciencedirect.com/science/article/pii/S004578252100205X)\
   **B Bahmani** and W. Sun, *Computer Methods in Applied Mechanics and Engineering*.
2. [**Training multi-objective/multi-task collocation physics-informed neural network with student-teachers transfer learnings**](https://arxiv.org/abs/2107.11496)\
   **B Bahmani** and W. Sun, arxiv

2019
----
1. [**Automated homogenization-based fracture analysis: Effects of SVE size and boundary condition**](https://www.sciencedirect.com/science/article/pii/S0045782518305644)\
   **B. Bahmani**, et al., *Computer Methods in Applied Mechanics and Engineering*.
2. [**Asynchronous spacetime discontinuous Galerkin formulation for a hyperbolic time-delay bulk damage model**](https://ascelibrary.org/doi/10.1061/%28ASCE%29EM.1943-7889.0001656)\
   **B. Bahmani** and R. Abedi, *Journal of Engineering Mechanics*.
3. [**A stochastic bulk damage model based on Mohr-Coulomb failure criterion for dynamic rock fracture**](https://www.mdpi.com/2076-3417/9/5/830)\
   **B. Bahmani**, et al., *Applied Sciences*.
4. [**Effect of volume element geometry on convergence to a representative volume**](https://asmedigitalcollection.asme.org/risk/article/5/3/030907/725714/Effect-of-Volume-Element-Geometry-on-Convergence)\
   K. Acton, C. Sherod, **B. Bahmani**, and R. Abedi, *ASCE-ASME Journal of Risk and Uncertainty in Engineering Systems, Part B: Mechanical Engineering*.

2018
----
1. [**Voronoi tessellation based statistical volume element characterization for use in fracture modeling**](https://www.sciencedirect.com/science/article/pii/S0045782518301051)\
   K. Acton, S. Baxter, **B. Bahmani**, P. Clarke, and R. Abedi, *Computer Methods in Applied Mechanics and Engineering*.
2. [**Application of an enriched FEM technique in thermo-mechanical contact problems**](https://link.springer.com/article/10.1007/s00466-018-1555-z)\
   A. Khoei and **B. Bahmani**, *Computational Mechanics*.

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}
