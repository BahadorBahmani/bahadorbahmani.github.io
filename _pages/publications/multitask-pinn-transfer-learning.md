---
published: false
title: "Training multi-objective/multi-task collocation physics-informed neural network with student-teachers transfer learnings"
layout: publication
pub_id: multitask-pinn-transfer-learning
permalink: /publications/multitask-pinn-transfer-learning/
figure_caption: "Temperature field for a 2D Poisson problem: exact solution, a PINN guided by a coarse finite element solution, and a plain PINN."
---

Physics-informed neural networks (PINNs) solve boundary value problems by training a network to satisfy governing equations and boundary conditions, but their training is fragile. Results depend heavily on weight initialization and hyperparameters, and the multiple physics constraints in the loss can conflict, so that reducing one error term increases another.

This paper proposes a training framework for collocation PINNs that combines three ingredients. A pre-training step uses auxiliary data, such as a cheap coarse finite element solution, to guide early training. A Net2Net teacher-student transfer selects the best of many small teacher networks and widens it into a larger student network. Finally, a gradient surgery method treats the loss as a vector of objectives and resolves conflicting gradients without extra weighting hyperparameters.

**Key findings**

- Coarse or even noisy finite element guidance made PINN training more robust to random initialization.
- On a 2D Poisson problem, the guided PINN recovered the solution where the plain, equally weighted PINN failed.
- Knowledge from a small teacher transferred stably to a student with about two orders of magnitude more parameters, including in an inverse conductivity problem.
