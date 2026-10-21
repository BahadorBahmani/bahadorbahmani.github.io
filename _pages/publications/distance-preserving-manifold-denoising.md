---
published: false
title: "Distance-preserving manifold de-noising for data-driven mechanics"
layout: publication
pub_id: distance-preserving-manifold-denoising
permalink: /publications/distance-preserving-manifold-denoising/
figure_caption: "The three-step local projection: an encoder flattens noisy data onto a hyperplane, points are projected onto it, and an isometric decoder maps them back as de-noised data."
byline: "This page was summarized by AI (Claude by Anthropic)."
---

Model-free, data-driven simulations replace constitutive models by searching directly in a database of material data. In practice such data are often limited and noisy, and noise can degrade the closest-point projection onto the data that these methods rely on.

This paper introduces a manifold embedding data-driven paradigm that works with noisy data. It alternates between a global step that enforces the balance principle and a local step that projects onto the constitutive manifold. A geometric autoencoder first maps the noisy data onto an approximately flat latent space, where noise is removed by projecting onto a hyperplane. Isometry constraints during training make the decoder distance-preserving, so that noise is not reintroduced when mapping back.

**Key findings**

- Enforcing isometry flattens the latent space while preserving distances, without hindering the dimensionality reduction.
- In a one-dimensional bar problem, the isometric autoencoder gives more accurate strain and stress fields that are free of spurious oscillations.
- On real biaxial data from mitral valve tissue, the de-noising schemes avoid erroneous, step-wise responses that the classical nearest-neighbor approach can produce with limited data.
