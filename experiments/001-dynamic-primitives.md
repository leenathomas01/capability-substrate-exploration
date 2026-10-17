# Experiment 001 — Dynamic primitive release

**Status:** Design proposal only; not executed.

## Objective

Test H2 first: Does an archive with typed conditional dependencies and targeted reassessment outperform early filtering and quality-diversity retention when new primitives become available over time?

## Environment

Use a synthetic, deterministic compositional task generator. Generate a family of programs from typed primitives (e.g. transforms, stateful operations, composition operators). Hide a stratified subset of necessary primitives until a prespecified release step. Generate candidate specifications and their predicted dependencies at step 0; candidates may be initially nonfunctional because relevant primitives are absent. Avoid giving any arm oracle knowledge of future releases.

A separate validation generator creates held-out tasks requiring (i) already available primitives, (ii) a newly released primitive, and (iii) combinations involving initially unusable candidate specifications. Give all arms the same public observation stream, primitive-release schedule, candidate pool and evaluator.

## Conditions

- **G:** Greedy utility/feasibility pruning, with no long-term candidate archive.
- **R:** Random retention at a defined archive capacity.
- **QD:** Quality-diversity archive with behavioral descriptors and periodic evaluation.
- **P:** Preserve candidates and periodically rerun retrieval without typed triggers.
- **PD:** Preserve candidates with typed dependencies and reassess when dependency conditions change.

For fairness, compare at multiple archive capacities and compute budgets; report total token/compute-equivalent cost including metadata, retrieval, reevaluation, and integration.

## Controls

- Seeded task and primitive generators, frozen before evaluation.
- Held-out test tasks, preregistered thresholds, common evaluator.
- Dependency-label corruption ablation and random-trigger ablation.
- Positive control: inject known solvable complementary pairs.
- Negative control: independently composable pairs with only additive effects.
- Strong baseline: QD with an equally informative dependency-aware variant, to separate dependency metadata from the archive algorithm.

## Measurements

**Primary:** independently validated held-out capabilities discovered by each arm within the common budget.

**Secondary:** time from primitive release to discovery; unique capability coverage; precision/recall of dependency-triggered retrieval; cost per validated capability; robustness across seeds.

Analyze bootstrap confidence intervals over independently generated worlds, not merely over repeated evaluations of the same world. Report failed runs and preregistered stopping rules.

## H1 subexperiment

Independently sample paired candidates from validated combinations. Evaluate 2×2 factorial controls: neither, A-only, B-only, A+B. Keep evaluation, training, and integration costs matched. Predefine outcome scale and genuinely new behavioral criterion. Distinguish positive statistical interaction from novel behavior.

## Interpretation

If PD exceeds G but not QD, the evidence favors archive-based diversity, not a distinctive CSDE contribution. If PD exceeds dependency-aware QD under matched budget, investigate whether explicit missing-substrate reassessment is causal. A null result is a valid result.

## Safety and scope

Start with harmless synthetic tasks. No autonomous modification of production systems, unsafe capability-targeted search, or claims about frontier research generality.
