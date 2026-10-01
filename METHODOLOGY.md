# DTL Board Methodology

DTL results are reported as a tuple, not as one blended score:

- precision on answered cases;
- coverage;
- abstention count;
- replay and certificate status;
- contamination and holdout status.

For software tasks, a solve requires a clean sealed archive and a complete
passing eval record. For exact-answer tasks, an answer is promoted only when a
deterministic lane emits a certificate; otherwise the system abstains.

Public-seed and development runs are evidence of behavior, not leaderboard
placements. A future holdout track must generate cases after implementation,
withhold expected answers, replay the result independently, and record the
certificate hash before assigning a rank.

The historical AIME result uses known case identifiers and case-specific
calculations. Treat it as arithmetic replay of public development examples.
It does not establish prompt understanding or performance on unseen problems.
For a competitive reasoning evaluation, freeze a solver that processes the
actual problem input before an independent evaluator supplies unseen cases.

Public package tests measure the specific cases exercised by that package.
Passing a suite does not certify the full E-stack, exclude other defects, or
establish superiority to a language model. External ranking requires acceptance
under the external benchmark's current rules.
