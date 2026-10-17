# Hypotheses and operational tests

## H1 — Compositional Capability Emergence

**Claim:** In a defined domain, some combinations of advances enable a capability not reachable using either constituent in isolation under matched evaluation and allowed resources.

Define a capability as a pre-registered task/behavior with performance threshold, elicitation protocol, and test distribution. "Reachable" always refers to specified budgets and optimization/measurement access; absence of observed success is not proof of impossibility.

**Tests:** Full factorial conditions (baseline, A alone, B alone, A+B), repeated independent seeds, explicit integration controls and ablations. A positive interaction on a fixed outcome scale is

`I_AB = Y_AB - Y_A - Y_B + Y_0`.

This tests superadditivity **on the chosen metric**; it is not automatically evidence of a qualitatively novel behavior. For a new-capability claim, preregister behavioral criteria and show isolated controls fail those criteria with adequate statistical power. Compare with best single-component performance, stronger isolated models given matched resources, and a generic integration baseline.

**What weakens H1:** Repeated controlled searches in a defined domain finding no prespecified synergistic interactions, after calibration with injected positive controls. A finite null does not disprove existence in all domains.

## H2 — Exploration-Strategy Advantage

**Claim:** Under equal total search budgets, retaining initially weak, unrealized, or substrate-blocked candidates with dependency metadata and reassessing them when primitives change improves discovery value and/or diversity versus matched early filtering.

**Primary outcome:** Number of independently validated *held-out* capabilities discovered by a deadline under fixed compute/evaluation budget (and confidence interval over seeds).

**Secondary outcomes:** Capability-space coverage, diversity, rediscovery delay, discovery cost, validation rate, and fraction of productive discoveries involving initially filtered candidates.

**Baselines:** (a) greedy early filter, (b) random retention, (c) quality-diversity archive, (d) archive without dependency triggers, and (e) dependency-triggered archive. Match candidate generation, evaluation access, integration budgets, and total compute including archive retrieval and scoring.

**What weakens H2:** No advantage against strong baselines at comparable cost; advantage vanishes when retrieval overhead or informative controls are included; results do not replicate across seeds/tasks.

**Critical independence:** H1 may hold while H2 fails, or H2 may hold without H1. Report each separately.

## Anti-leakage and preregistration

Fix held-out capability tests and primitive-release schedule before comparing pipelines. Do not use future-release information in early decisions. Register the utility filter, allocation rule, permitted adaptations, stopping conditions, and analysis thresholds before testing. Disclose post-hoc discoveries separately. Include security and misuse assessment for proposed experiments.
