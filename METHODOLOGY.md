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
