---
published: false
title: "Neural Chaos: A Spectral Stochastic Neural Operator"
layout: publication
pub_id: neural-chaos
permalink: /publications/neural-chaos/
figure_caption: "Neural Chaos builds a spectral expansion one term at a time, with each term the product of a learned deterministic basis function and a learned stochastic basis function."
byline: "This page was summarized by AI (Claude by Anthropic)."
---

Surrogate models with uncertainty quantification are needed whenever material properties, boundary conditions or initial conditions are random. Polynomial chaos expansion is the standard tool, but complex or high-dimensional problems need high-order polynomials, which raises cost and the risk of overfitting, and dependent random variables need special, problem-specific treatment.

This paper keeps the spectral expansion form of polynomial chaos but replaces the polynomial basis with neural network basis functions. An algorithm learns these basis functions one at a time from data, each term the product of a deterministic and a stochastic network, and keeps them orthogonal with respect to the data distribution. The stochastic basis is built directly on the joint random variables, with no assumptions about their joint or marginal distributions and no tensor-product structure.

**Key findings**

- In the examples studied, fewer than 20 neural basis functions outperformed more than 5000 polynomial chaos basis functions.
- The method applies unchanged to dependent random variables, and mean and variance fields follow directly from the expansion.
- A discrete-continuous training algorithm was more robust and converged faster than a fully continuous one.
