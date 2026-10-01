# JARVI3 and the EcoKure E-stack

JARVI3 combines an AI workspace with tools for checking supported claims.
The EcoKure E-stack organizes the work behind those checks: select an applicable
capability, verify its result, retain the evidence, and control a proposed action.

## Explore the public tools

| Start with | What you can inspect |
| --- | --- |
| [ClaimStack demo](https://github.com/kyal102/claimstack-demo) | Route a written claim, check dimensions, seal a receipt and demonstrate receipt replay. |
| [DTL MathGate](https://github.com/kyal102/dtl-mathgate) | Evaluate supported arithmetic with exact values and explicit refusal states. |
| [EvidencePack](https://github.com/kyal102/evidencepack) | Record the input, checker, version and verdict in a hash-stamped receipt. |
| [ReplayGate](https://github.com/kyal102/replaygate) | Replay supported evidence packs and inspect result drift. |
| [DTL taxonomy](https://github.com/kyal102/dtl-taxonomy) | Inspect the public claim taxonomy and verdict schema. |

These are public lite tools with their own licenses and documented limits.
They expose useful parts of the approach; they are not the complete private
JARVI3 application or an independently validated implementation of every E-stack layer.

## Architecture at a glance

| Responsibility | E-stack roles |
| --- | --- |
| Discover and verify reusable behavior | E-OSA models declared state transformations; E-VSC validates scoped semantic capabilities. |
| Choose an applicable capability | E-DTL performs structural matching and routing within declared boundaries. |
| Check a change and its evidence | E-DCLA tracks dependencies and change impact; E-DELA tracks evidence lineage and freshness; E-DEGA performs independent checks. |
| Control an action | E-ACC binds an exact proposed action to bounded authority; E-RA rechecks state and authority at execution. |
| Continue through a defined outage | E-SR retains eligible capabilities for bounded local continuity. |

This is a map of responsibilities, not a claim that all nine roles run in every
request. Implementations have different maturity and supported domains.

## Try a small demonstration

The public ClaimStack quickstart uses Python's standard library:

```sh
git clone https://github.com/kyal102/claimstack-demo
cd claimstack-demo
python run_demo.py
```

The bundled examples include a dimensionally inconsistent equation, a
dimensionally consistent equation, a claim needing measurements, and an
unsupported claim. Inspect the JSON report and receipts alongside the displayed
verdict. Dimensional consistency alone does not establish physical truth.
The bundled replay target echoes the stored verdict to demonstrate the receipt
format; it does not independently rerun the original dimensional check.

## Evaluate it in your workflow

A useful evaluation starts with one workflow and explicit acceptance criteria:
supported inputs, expected refusals, false accepts, false rejects, repeatability,
latency, and what changes when evidence or policy changes. Keep hidden test cases
separate from development examples. The [evidence board](README.md) distinguishes
public demonstrations from accepted external benchmark entries.

Explore [JARVI3](https://jarvi3.com) or [a bounded pilot](https://kyal102.github.io/jarvi3-dtl-evidence-board/pilot.html) for product
access and enterprise evaluation enquiries. Technical reproduction questions
belong in the relevant public tool's issue tracker.
