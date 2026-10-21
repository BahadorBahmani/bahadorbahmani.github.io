---
published: false
title: "A stochastic bulk damage model based on Mohr-Coulomb failure criterion for dynamic rock fracture"
layout: publication
pub_id: stochastic-bulk-damage-rock
permalink: /publications/stochastic-bulk-damage-rock/
figure_caption: "Damage spreading through a heterogeneous rock sample under strong compressive loading, with localized damage bands forming over time."
byline: "This page was summarized by AI (Claude by Anthropic)."
---

Bulk damage models represent microcracking through a smooth damage field, which makes complex rock fracture patterns easy to capture. However, common formulations drive damage only with the tensile part of strain or stress, so they fail to model rock failure in compression. Earlier local models also suffer from mesh sensitivity.

This paper proposes a damage force based on the Mohr-Coulomb failure criterion, together with an effective stress relation suited to compressive failure. Damage evolves by a time-delay ordinary differential equation whose relaxation time introduces an intrinsic length scale. The coupled problem is solved with the asynchronous spacetime discontinuous Galerkin method, and rock inhomogeneity is modeled by treating cohesion as a lognormal random field generated with the Karhunen-Loeve method.

**Key findings**

- The time-delay law removes mesh sensitivity and captures loading-rate effects on strength and toughness.
- Inhomogeneity strongly changes where damage initiates and which zones become most damaged, compared with a homogeneous rock.
- As the correlation length decreases, damage localizes into angled bands resembling compressive rock fractures.
