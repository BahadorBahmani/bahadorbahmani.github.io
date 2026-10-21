---
title: "A Multi-Fidelity Bayesian Neural Operator for Mechanics of Spinodal Metamaterial"
layout: publication
pub_id: multifidelity-bayesian-neural-operator
permalink: /publications/multifidelity-bayesian-neural-operator/
figure_caption: "A low-fidelity operator trained on actively selected simulations feeds a high-fidelity Bayesian model that learns the remaining gap to experiments from the 3D microstructure geometry."
byline: "This page was summarized by AI (Claude by Anthropic)."
---

Spinodal metamaterials offer a large design space for tailoring nonlinear mechanical behavior, but exploiting it for inverse design requires predicting full stress-strain curves, not just a few bulk properties. Data-driven models for this task are limited by the high cost of experiments, while cheaper simulations do not capture all real effects such as fabrication defects.

This paper proposes a multi-fidelity Bayesian neural operator based on DeepONet. A low-fidelity operator is first trained on finite element simulations chosen by a hybrid active learning strategy that balances model uncertainty and microstructural diversity. A high-fidelity Bayesian model, which reads the 3D microstructure as a signed distance field, then learns the residual between simulations and in-situ nanomechanical experiments.

**Key findings**

- The hybrid active learning strategy reaches nearly saturated accuracy with only 22 simulations selected from a pool of 3000 designs.
- With 20 experimental samples, the multi-fidelity model reduces mean squared error by 86.0% and 84.1% compared with the low- and high-fidelity models alone.
- It gives better predictions of stiffness, ultimate stress and energy absorption, with tighter uncertainty bands than a model trained only on sparse experiments.
