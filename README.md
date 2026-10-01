# JARVI3 / EcoKure — public tools and evidence

Inspect a check. Run it yourself. Keep the receipt.

JARVI3 and the EcoKure E-stack connect supported verification tools, evidence
records and replay. Start with the [E-stack overview and public quickstart](E-STACK.md),
try [JARVI3](https://jarvi3.com), or discuss a bounded evaluation through
[EcoKure](https://ecokure.com).

This is the public evidence board for the Deterministic Taxonomy Lanes (DTL)
method. It is not the official ProgramBench leaderboard and it does not turn
local or public-seed results into official rankings.

## Current board

| Entry | Track | Result | Eligibility | Evidence |
| --- | --- | ---: | --- | --- |
| Jarvi3: Themis-G / ProgramBench cleanroom | official benchmark submission | 2/200 resolved; 1,037/1,037 recorded tests passed | Official registry PR pending | [public package](https://github.com/kyal102/jarvi3-themis-g-programbench-2solve), [PR #27](https://github.com/ProgramBench/submissions/pull/27) |
| DTL/SuperMath / AIME-style public cases | problem-specific arithmetic replay | 14 correct, 0 incorrect, 16 abstain; 14/30 overall | Development evidence using case-specific code; not an unseen-problem reasoning score or an official MathArena ranking | [included report](evidence/aime-2026-supermath-dtl-full30.md) |

Coverage, correctness and refusals are reported separately. The AIME wrapper
routes by known case identifiers to problem-specific calculations; its 100%
precision on answered examples does not measure generalization to unseen math
problems. A certificate records the declared computation, not benchmark eligibility.

Last registry status check: 1 October 2026. ProgramBench PR #27 remains open.

## Eligibility

- `official`: an external benchmark registry has accepted the entry.
- `pending_registry`: the public package and registry PR exist, but a
  maintainer has not merged the entry yet.
- `public_seed_evidence`: reproducible local evidence on a public or development
  seed; useful for method inspection, not an official ranking.
- `holdout_eligible`: reserved for a fresh post-implementation holdout whose
  expected answers were withheld from the system.

The machine-readable source is [`leaderboard.json`](leaderboard.json). Every
entry includes its scope, result counts, source commit or report, and claim
boundary. The board must never report a self-awarded rank as an official rank.

## DTL promotion rule

```text
proposal -> deterministic lane -> certificate -> promote, abstain, or reject
```

The model can propose. The lane decides what compounds. A future commercial
board can add independent submissions, fresh holdouts, replay hashes, and
reviewer signatures without changing this evidence format.
