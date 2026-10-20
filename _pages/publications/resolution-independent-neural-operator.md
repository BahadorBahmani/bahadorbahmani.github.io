---
title: "A Resolution Independent Neural Operator"
layout: publication
pub_id: resolution-independent-neural-operator
permalink: /publications/resolution-independent-neural-operator/
figure_caption: "Vanilla DeepONet needs input functions sampled at the same fixed points, while the resolution-independent version projects arbitrarily sampled inputs onto a learned dictionary of basis functions before the branch network."
---

DeepONet is a simple and flexible neural operator for learning maps between function spaces, and it can evaluate the output anywhere in the domain. However, it requires every input function to be sampled at the same fixed sensor locations, which limits its use with real data collected at varying numbers and positions of points.

This paper introduces a framework for operator learning from input and output data sampled at arbitrary locations. Two dictionary learning algorithms learn continuous basis functions, parameterized as sinusoidal implicit neural representations (SIRENs), from point cloud data. Projecting each input onto this dictionary gives a fixed-size embedding that DeepONet can use without architectural changes. Applying the same idea to the outputs gives the Resolution Independent Neural Operator (RINO), which maps input basis coefficients to output basis coefficients.

**Key findings**

- RINO handles arbitrarily, but sufficiently finely, sampled inputs and outputs during both training and inference across several numerical examples.
- The learned dictionaries find low-dimensional structure; in one example, 10 basis functions reconstructed 100-dimensional data with low error.
- For some problems, the operator between the latent spaces becomes simple, such as a linear map.
