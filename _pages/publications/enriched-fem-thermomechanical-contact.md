---
title: "Application of an enriched FEM technique in thermo-mechanical contact problems"
layout: publication
pub_id: enriched-fem-thermomechanical-contact
permalink: /publications/enriched-fem-thermomechanical-contact/
figure_caption: "A cracked body under thermal and mechanical loads, with contact tractions and heat flux transferred across the closed crack faces."
---

Cracks in heated components can open, close, and slide, and the heat flowing across a closed crack depends on how hard its faces press together. Analytical solutions to such thermo-mechanical contact problems exist only for special cases, so numerical tools are needed. This paper notes that no explicit enriched finite element algorithm for this coupled problem existed before.

This paper presents a fully coupled thermo-mechanical contact formulation within the extended finite element method (X-FEM). Heaviside enrichment captures jumps in displacement and temperature across the crack, Coulomb friction governs sliding, and a pressure-dependent thermal contact law describes heat flux across the contact zone. The equations are discretized in time with a Newmark scheme and solved by a staggered Newton-Raphson algorithm.

**Key findings**

- Results for several benchmark problems agree with published results or analytical solutions.
- Assuming a constant thermal contact conductivity is only acceptable over a limited range of contact pressure.
- The method identifies a priori unknown contact zones and handles plates with multiple cracks.
