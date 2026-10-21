---
published: false
title: "Physics-constrained Symbolic Model Discovery for Polyconvex Incompressible Hyperelastic Material"
layout: publication
pub_id: polyconvex-symbolic-hyperelasticity
permalink: /publications/polyconvex-symbolic-hyperelasticity/
figure_caption: "Two-step discovery: convex neural networks first fit the energy of each strain invariant, then symbolic regression turns each one into a short equation."
byline: "This page was summarized by AI (Claude by Anthropic)."
---

Hyperelastic energy functionals describe soft materials that undergo large elastic deformations. Neural network models can fit such data well, but they are hard to interpret, may violate physical requirements such as polyconvexity, and can behave poorly outside the training range. Symbolic regression gives readable equations but struggles when there are many input variables.

This paper proposes a polyconvex neural additive model (PNAM) that writes the energy as a sum of univariate functions, each built from an input-convex neural network, so polyconvexity is guaranteed by construction. Genetic programming then converts each univariate function into a compact mathematical expression, which avoids the high-dimensional search that limits standard symbolic regression.

**Key findings**

- The resulting symbolic models are interpretable and provably satisfy polyconvexity and frame indifference.
- On Treloar's rubber data, the discovered equation extrapolates well and is slightly more accurate than a reference model, while a vanilla neural network fails beyond the training range.
- The compact equations need fewer arithmetic operations than deep networks, which suits large-scale simulations with many integration points.
