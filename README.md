# Capability–Substrate Decoupled Exploration (CSDE)

**Status:** Open proposal · **Experimental results:** None claimed · **Established:** 2026-10-17

This repository explores whether preserving unrealized, weakly performing, or dependency-blocked advances—and revisiting them when new primitives, substrates, or integration mechanisms arrive—improves capability discovery over early-filtering research pipelines.

This is **not** a claim to have discovered a new form of emergence or invented combinatorial search, quality-diversity methods, open-ended learning, model merging, or task arithmetic. The proposed synthesis must be evaluated against these precedents.

## Core distinctions

- **Idea:** A specification or conjecture, which may have no viable realization.
- **Capability:** A measurable behavior defined relative to a task, elicitation method, and evaluation protocol.
- **Substrate:** The physical/computational machinery needed to implement or test an idea.
- **Dependency:** A necessary, enabling, or hypothesized complementary condition. Record whether it is available and what evidence supports the relationship.
- **Hidden capability:** A behavior supported by an existing model but not ordinarily elicited; this is different from an idea lacking an implementation.

## Two independent hypotheses

**H1 — Compositional Capability Emergence.** Some combinations enable operationally defined capabilities unavailable to constituents evaluated separately under controlled conditions.

**H2 — Exploration-Strategy Advantage.** Preserving and conditionally reassessing initially unattractive advances yields more or more diverse valuable discoveries than matched early-filtering strategies under the same total budget.

H1 does not imply H2, and H2 does not imply H1. Both may fail. See [HYPOTHESES.md](HYPOTHESES.md).

## Research commitments

1. Preserve candidates with clear epistemic labels rather than treating archived hypotheses as verified.
2. Separate falsified hypotheses, inadequate substrates, poor integration, and inadequate evaluations.
3. Represent typed dependencies and conditional reassessment triggers.
4. Treat **economic constraints as a total research budget**, while experimentally delaying *candidate-level* utility filtering. This does not imply unlimited exploration.
5. Evaluate higher-order combinations and compare against strong diversity-preserving baselines.
6. Preregister isolation protocols, null models, metrics, ablations, and stopping rules.
7. Report unsuccessful searches, archive overhead, and operational/safety constraints.

## Repository

- [HYPOTHESES.md](HYPOTHESES.md) — definitions, predictions, controls
- [LIMITATIONS.md](LIMITATIONS.md) — failure modes
- [literature/README.md](literature/README.md) — related work and boundary conditions
- [experiments/001-dynamic-primitives.md](experiments/001-dynamic-primitives.md) — controlled initial experiment
- [ideas/SCHEMA.md](ideas/SCHEMA.md) — archive format
- [ideas/idea-2026-001.md](ideas/idea-2026-001.md) — hypothetical sample, not a result
- [CONTRIBUTING.md](CONTRIBUTING.md) — standards for contributions

## What constitutes evidence?

Reproducible, preregistered experiments measuring an H1 interaction or an H2 advantage relative to budget-matched baselines; distinguish effect sizes, uncertainty, costs, and the domain of validity. An interesting story or analogy is not experimental evidence.

## Attribution

This proposal was developed through human–AI exploratory discussion; AI assistance was used in literature discovery and drafting. Citations are a curated starting point, not a systematic literature review. Verify primary sources before formal scholarly citation.
