---
published: false
title: "A Review on Data-Driven Constitutive Laws for Solids"
layout: publication
pub_id: review-data-driven-constitutive-laws
permalink: /publications/review-data-driven-constitutive-laws/
figure_caption: "The review's taxonomy of constitutive modeling, separating phenomenological, model-free and machine-learning approaches by interpretability and learning type."
byline: "This page was summarized by AI (Claude by Anthropic)."
---

Constitutive laws describe how materials respond to loading, and they have traditionally been built by hand from limited experiments. Full-field imaging and multiscale simulation now provide far more data, and a fast-growing body of data-driven methods aims to use it, which calls for an organized view of what works and what remains open.

This review surveys data-driven techniques that discover, encode, surrogate or emulate the path-independent and path-dependent behavior of solids. It separates machine-learning-based methods from model-free methods and further groups them by interpretability and by the type of data and learning they require. It also covers data sampling, design of experiments, verification and validation, with applications spanning elasticity, hyperelasticity, plasticity, damage, fracture, fatigue and multiphysics problems.

**Key findings**

- Enforcing physics constraints is a recurring route to robustness, interpretability, generalization and trust across all classes of data-driven models.
- Open challenges include integrating learned laws with experimental and finite element workflows, discovering internal variables for path-dependent behavior, and working with little data.
- Uncertainty quantification and optimal test design are expected to play a major role in future work.
