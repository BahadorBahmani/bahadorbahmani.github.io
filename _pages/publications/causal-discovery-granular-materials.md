---
published: false
title: "Data-driven discovery of interpretable causal relations for deep learning material laws with uncertainty quantification"
layout: publication
pub_id: causal-discovery-granular-materials
permalink: /publications/causal-discovery-granular-materials/
figure_caption: "Causal graph discovered for a granular assembly, linking strain, microstructural and topological measures, and stress, with edge inclusion probabilities."
---

Machine-learned material laws often lack interpretability: it is hard to tell why a model makes a given prediction. Causal graphs offer a human-readable way to represent how physical quantities influence one another, but discovering them from non-stationary, path-dependent simulation data is difficult.

This paper develops a framework that first infers causal relations among time-history data from representative volume element simulations, expressed as a directed acyclic graph, while allowing known physical knowledge to be included. Predictions are then propagated along the discovered graph using deep neural networks with dropout layers as a Bayesian approximation, giving ensemble predictions with uncertainty quantification. The method is tested on traction-separation laws for frictional interfaces and on the elastoplasticity of granular assemblies.

**Key findings**

- For granular matter, the method rediscovers known mechanisms, such as void-space changes driving coordination number and the dominant role of the strong fabric tensor on stress.
- It also suggests relations not previously reported, such as average clustering affecting the local efficiency of particle connectivity.
- Stress predictions for true triaxial tests showed notable over-fitting, indicating that more data or regularization is needed for unconventional loading paths.
