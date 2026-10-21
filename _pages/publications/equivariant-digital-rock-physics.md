---
published: false
title: "Equivariant geometric learning for digital rock physics: estimating formation factor and effective permeability tensors from Morse graph"
layout: publication
pub_id: equivariant-digital-rock-physics
permalink: /publications/equivariant-digital-rock-physics/
figure_caption: "Rotating the Morse graph of a rock sample rotates the permeability tensor predicted by the equivariant network, shown as an ellipsoid, in the same way."
---

Formation factor and effective permeability are key hydraulic properties of porous rocks, and they can be computed from micro-CT images through direct numerical simulation. Such 3D simulations are costly, while standard convolutional neural networks used as surrogates can give predictions that depend spuriously on the orientation of the image and require large memory for 3D inputs.

This paper predicts the formation factor and effective permeability tensors directly from micro-CT images of sandstone. The pore space is represented compactly by a persistence-based Morse graph, and Fast Fourier Transform solvers generate the training data. An SE(3)-equivariant graph neural network is compared with a classical convolutional neural network and a graph neural network without the equivariance constraint.

**Key findings**

- Graph neural networks on Morse graphs consistently outperform the convolutional neural network.
- The equivariant network gives the most accurate predictions, especially when training data are limited.
- Its predictions satisfy material frame indifference, rotating consistently with the input, whereas convolutional predictions can depend on the coordinate system.
- With rotational data augmentation, non-equivariant networks remain roughly an order of magnitude less accurate.
