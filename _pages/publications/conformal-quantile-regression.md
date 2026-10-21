---
title: "Conformal Quantile Regression for Neural Probabilistic Constitutive Modeling"
layout: publication
pub_id: conformal-quantile-regression
permalink: /publications/conformal-quantile-regression/
figure_caption: "Strain invariants from the deformation and fiber directions feed monotone neural networks that give upper and lower stress quantiles, which conformal prediction then calibrates."
byline: "This page was summarized by AI (Claude by Anthropic)."
---

Biological soft tissues are highly nonlinear, anisotropic and vary a lot from one specimen to another, yet most data-driven constitutive models are deterministic and give no measure of predictive uncertainty. Bayesian neural networks can supply uncertainty, but they are costly to train, need repeated sampling at inference, and make it harder to keep physical constraints.

This paper builds a probabilistic constitutive model for anisotropic soft materials based on quantile regression. Monotone neural networks learn upper and lower quantiles of the strain-energy derivatives within a polyconvex, invariant-based formulation, so every predicted quantile stays thermodynamically consistent. A tensor-valued extension of conformalized quantile regression then calibrates the stress intervals without assuming any particular data distribution.

**Key findings**

- The approach is plug-and-play: it turns existing deterministic models into probabilistic ones, avoids Monte Carlo sampling, and costs about the same as a deterministic model at inference.
- On synthetic arterial-wall data, the model extrapolates well beyond the training strains, though uncertainty becomes too narrow at very large strains.
- On experimental heart valve leaflet data, the uncertainty bands cover most measurements for an unseen biaxial loading ratio.
