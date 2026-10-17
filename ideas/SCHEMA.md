# Idea entry schema (version 0.1)

Use one Markdown file per conjecture or advance with YAML front matter. Entries are **hypotheses, not instructions to implement or assertions of feasibility**.

## Required fields

- `id`: Stable unique identifier.
- `title`: Descriptive title.
- `status`: `unrealized-theoretical` | `inadequate-substrate` | `partially-realized` | `hidden-capability-candidate` | `tested-negative` | `tested-positive` | `superseded` | `archived-dormant`.
- `summary`: What is proposed, without overstating evidence.
- `capability-claim`: Operational target or `null`.
- `dependencies`: Typed records: `ref`, `type` (necessary-substrate / complementary-idea / algorithm / integration / evaluation), `availability` (available / absent / unknown), and `evidence-level` (conjecture / theoretical / partial / validated).
- `isolation-notes`: How an independent test would isolate this component; explicitly `not-yet-testable` if appropriate.
- `created`, `last-reassessed`: ISO dates.

## Recommended fields

- `predicted-interaction`, `evidence` (with sources and counterexamples), `utility-at-creation`, `reassessment-triggers`, `tags`, `author-notes`.
- `reassessment-history`: append-only dates, trigger, findings, outcome.
- `safety-notes`: any significant foreseeable misuse.

## Validation principles

Do not silently relabel missing substrate as `tested-negative`. A negative result must identify the implemented test, task and adequate controls. Preserve superseded ideas with pointer to replacement. State uncertainty explicitly. Do not include secrets or private datasets.
