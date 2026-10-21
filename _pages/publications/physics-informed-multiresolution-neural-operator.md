---
published: false
title: "A Physics-informed Multi-resolution Neural Operator"
layout: publication
pub_id: physics-informed-multiresolution-neural-operator
permalink: /publications/physics-informed-multiresolution-neural-operator/
figure_caption: "The two-step PI-RINO pipeline: irregularly sampled inputs are embedded with learned basis functions, then an MLP is trained against physics-based losses."
---

Neural operators learn maps between functions, but they usually need large sets of high-fidelity input-output pairs and require every input to be sampled at the same fixed sensor locations. In practice, data often come from simulations on different or adaptive grids, or from experiments with misaligned sensors, which makes such datasets hard to use.

This paper extends the Resolution Independent Neural Operator (RINO) to a fully data-free, physics-informed setting called PI-RINO. Arbitrarily discretized input functions are projected onto pre-trained basis functions, giving a fixed-size latent code. A simple multi-layer perceptron takes this code together with space-time coordinates and predicts the solution, while the governing PDEs are enforced through a finite difference solver in the physical space.

**Key findings**

- PI-RINO learns accurate solution operators from input functions sampled at mixed coarse and fine resolutions, on benchmarks including an antiderivative problem, 2D heat conduction and Biot consolidation.
- Finite difference enforcement of the physics gives errors comparable to automatic differentiation while running about 2 times faster in 1D and up to 10 times faster in 2D.
- The approach points toward physics-informed operator learning with sparse, missing, multi-fidelity or mixed simulation and experimental data.
