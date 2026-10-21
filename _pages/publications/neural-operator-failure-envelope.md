---
title: "Neural Operator Representation of Granular Micromechanics-based Failure Envelope"
layout: publication
pub_id: neural-operator-failure-envelope
permalink: /publications/neural-operator-failure-envelope/
caption_align: left
figure_in_body: true
section_style: numbered
---

This page was written by Jinkyo Han with the help of AI (Claude by Anthropic).

## Overview
{: style="margin-top: 0.5em"}

Granular micromechanics models predict failure in porous and particulate materials such as concrete, soils, foams and biological tissues. However, the link from microstructure parameters to a macroscopic failure envelope is implicit: each point on the envelope requires a costly nonlinear, non-smooth simulation along a loading path. This cost grows further in inverse problems, where one searches for microstructures that give a target failure response.


{% include pub-animation.html src="/images/publications/neural-operator-failure-envelope.png" width="70%" caption="Illustration of the architecture. The micromechanical configuration and the angular coordinate enter the network, and the angular parametrization is reused to trace a closed, star-shaped failure envelope with the expected periodicity." %}

This paper proposes a differentiable neural operator, based on DeepONet, that maps microstructure configurations directly to failure envelopes, enabling fast forward prediction and gradient-based inverse identification. A curvature penalty motivated by Drucker's postulate pushes the predicted envelopes to be convex. The operator learns from envelopes given as irregular point clouds at varying resolutions, and an ensemble-based active learning strategy picks new simulations where the model is most uncertain.

## Results

Motivated by Drucker's postulate, the failure envelope is kept convex for a stable material response, through a curvature-based penalty on negative signed curvature.

{% include pub-animation-pair.html left="ex1_worst_10_nocurv.png" left_width="35%" right="ex1_worst_10_curv.png" right_width="35%" caption="Worst validation cases for the model trained without (left) and with (right) the curvature-based penalty." %}

The trained neural operator serves as a differentiable surrogate with fast inference, which enables inverse identification: finding micromechanical configurations that produce a desired material behavior.

{% include pub-animation-pair.html left="loss_movie.gif" left_width="30%" left_offset="0.38%" center="inverse_movie.gif" center_width="30.84%" right="xi_movie.gif" right_width="30%" right_offset="0.38%" caption="Inverse identification over multiple trials: loss histories (left), surrogate predictions against the target failure envelope (center), and trajectories of the micromechanical parameters (right)." %}

The surrogate also serves as a backbone for uncertainty quantification. In an adaptive sequential sampling example, a smaller dataset chosen by active learning is as informative as a larger dataset from Latin hypercube sampling.

{% include pub-animation-pair.html left="ex3_benchmark_full_mean.png" left_width="40%" right="ex3_benchmark_full_q99.png" right_width="40%" caption="Informativeness of the dataset across dataset sizes, measured by the mean (left) and near-worst, 99% quantile (right) validation errors." %}

## Key findings

- The convexity regularization removes non-physical, non-convex artifacts in both forward predictions and inverse identification.
- Finite differences evaluate the curvature penalty faster than automatic differentiation at the problem sizes of interest.
- Beyond a small initial dataset, 160 adaptively chosen samples gave lower mean error than 320 Latin hypercube samples.
