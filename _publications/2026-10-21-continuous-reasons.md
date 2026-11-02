---
title: "Continuous Reasons for Random Forests via Budgeted Ordered Binary Decision Diagrams Compilation"
collection: publications
permalink: /publication/2026-continuous-reasons
excerpt: >-
  Random forests are accurate but opaque, and explaining their decisions with formal guarantees is
  computationally demanding. We study continuous reasons for random-forest classifiers, that is,
  robust boxes of input imprecision within which every point receives the same hard-majority
  label, and we compute coordinate-wise maximal such boxes that certify how far the inputs may
  jointly vary before the verdict changes. The central idea is to amortize the cost of formal
  reasoning across an entire dataset: we compile the classification relation of a trained forest
  into Ordered Binary Decision Diagrams (OBDDs) once, encoding each feature axis into cells cut by
  the forest thresholds and tallying hard-majority votes through a symbolic accumulator, then read
  a per-sample reason off the shared diagram by a counterexample-driven squeeze and a
  coordinate-wise maximize. To keep compilation within memory, a node budget triggers a
  tableau-style case split on a single cell bit, so the monolithic diagram is replaced by a tree
  of disjoint cubes, each carrying a small final OBDD. We compare this compile-once, read-many
  approach with existing sample-wise optimization methods in a preliminary experimental study.
date: 2026-10-21
venue: '17th International Conference on Scalable Uncertainty Management (SUM 2026), Athens, Greece — Springer LNAI, in press'
citation: 'Amadori, D., Chini, E., Sala, P. (2026). &quot;Continuous Reasons for Random Forests via Budgeted Ordered Binary Decision Diagrams Compilation.&quot; <i>17th International Conference on Scalable Uncertainty Management (SUM 2026)</i>, Springer LNAI. In press.'
---
Presented at SUM 2026 (NTUA, Athens, 21-23 October 2026). **The Springer LNAI proceedings are not
out yet**, so there is no DOI to link to for now.

The classification relation of the forest is compiled into Ordered Binary Decision Diagrams once;
the continuous reason of a single sample is then obtained from the shared diagram by a
counterexample-guided squeeze. A node budget triggers a case split on a cell bit, so the monolithic
diagram becomes a tree of disjoint cubes.

The code is available online: [RandomForest-Symbolic-Compiler](https://github.com/danielamadori/RandomForest-Symbolic-Compiler)

Recommended citation: Amadori, D., Chini, E., Sala, P. (2026). "Continuous Reasons for Random Forests via Budgeted Ordered Binary Decision Diagrams Compilation." <i>17th International Conference on Scalable Uncertainty Management (SUM 2026)</i>, Springer LNAI. In press.
