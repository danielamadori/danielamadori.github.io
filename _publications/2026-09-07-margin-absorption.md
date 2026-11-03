---
title: "Compiling the Plurality Winner of a Random Forest into OBDDs via Margin Absorption"
collection: publications
permalink: /publication/2026-margin-absorption
excerpt: >-
  A random forest classifies a tabular input by aggregating the votes of its decision trees, and a
  natural prerequisite for formal, region-based explanations is a compact symbolic representation
  of the regions of input space on which each label is the prediction of the forest. We present a
  relational encoding that compiles, one tree at a time, the regions on which a label is the
  plurality (argmax) winner of the forest into Ordered Binary Decision Diagrams (OBDDs). The
  encoding keeps, for a fixed pivot label, one signed margin counter per rival, and folds the
  trees through a transition relation over two copies of the counter state. Its distinguishing
  device is margin absorption: two latch flags, certain-win and certain-lose, fire the moment the
  contest against the relevant rivals is decided regardless of the trees still to be folded, after
  which the decided states collapse to a single absorbing state, reducing the intermediate
  diagram; a complementary drop discipline frees a counter that can no longer be the binding one.
  A prioritized one-vs-rest peeling then assembles the per-label win and tie regions and yields a
  sound and complete test for verifying a box-shaped reason. We prove the two latches fire at
  exactly the right moment, as soon as no outcome of the trees still to be folded can change the
  contest and not a step before, since a lead equal to the number of remaining trees can still be
  driven to a tie; we establish a collapse invariant, showing that once a state is decided it no
  longer depends on its counters; and we show the assembled win regions coincide with the
  prediction the forest itself makes. On tuned forests we confirm the construction (the regions
  are bit-identical with the collapse on and off) and find the reduction grows with the diagram,
  to several-fold on the densest forests. The encoding is purely relational, in the symbolic
  model-checking style, and keeps no auxiliary state beyond the counters and flags, the lone
  auxiliary of the drop phase being projected away within each tree step, and is the compilation
  core of a compile-once, read-many explainer.
date: 2026-09-07
venue: 'Italian Conference on Theoretical Computer Science (ICTCS 2026), Udine, Italy, CEUR-WS.org vol. 4269, pp. 288-300'
paperurl: 'https://ceur-ws.org/Vol-4269/paper53.pdf'
citation: 'Amadori, D., Chini, E., Sala, P., Tosato, E.M.S. (2026). &quot;Compiling the Plurality Winner of a Random Forest into OBDDs via Margin Absorption.&quot; <i>Italian Conference on Theoretical Computer Science (ICTCS 2026)</i>, CEUR-WS.org vol. 4269, pp. 288-300.'
---
[Read the paper here](https://ceur-ws.org/Vol-4269/paper53.pdf)

The central device is margin absorption: two flags, certain-win and certain-lose, fire as soon as a
contest is decided, and the decided states collapse into a single absorbing state.

The code is available online: [margin-absorption](https://github.com/PietroSala/margin-absorption)

Recommended citation: Amadori, D., Chini, E., Sala, P., Tosato, E.M.S. (2026). "Compiling the Plurality Winner of a Random Forest into OBDDs via Margin Absorption." <i>Italian Conference on Theoretical Computer Science (ICTCS 2026)</i>, CEUR Workshop Proceedings vol. 4269, pp. 288-300.
