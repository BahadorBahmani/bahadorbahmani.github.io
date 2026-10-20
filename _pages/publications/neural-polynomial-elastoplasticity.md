---
title: "Discovering Interpretable Elastoplasticity Models via the Neural Polynomial Method enabled Symbolic Regression"
layout: publication
pub_id: neural-polynomial-elastoplasticity
permalink: /publications/neural-polynomial-elastoplasticity/
figure_caption: "Divide-and-conquer symbolic regression: each learned one-dimensional neural feature is replaced by an equation, and the yield function becomes a polynomial of these features."
---

Neural network elastoplasticity models can be accurate, but they are often seen as black boxes, which limits their use in high-consequence engineering. Symbolic regression can produce readable equations, yet it scales poorly when a yield surface depends on several stress variables.

This paper introduces a two-step approach. First, a Quadratic Neural Model expresses the yield surface as a polynomial of single-variable features, each learned by a small neural network, with products of features added for expressivity and a sparsity penalty to keep the model simple. Second, symbolic regression replaces each one-dimensional neural feature with a mathematical expression, turning one hard multivariate search into several easy one-dimensional ones.

**Key findings**

- The method yields analytical yield functions that are accurate enough for engineering use and easy to implement in solvers written in different languages.
- On synthetic data with a known non-convex yield function and on porous metal data with no known analytical form, it is more accurate than the neural additive model.
- The closed-form models allow automated reasoning about properties such as convexity and symmetry, and the code is open source.
