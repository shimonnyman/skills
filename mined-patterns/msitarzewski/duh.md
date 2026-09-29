# duh — repeatable multi-model evaluation

Status: analysis/reference only; not an installed skill, implementation, or approved specification.

Source: [msitarzewski/duh](https://github.com/msitarzewski/duh). Revision and license: [source ledger](./SOURCES.md).

## Problem and observed source pattern

Comparing model answers needs more than a persuasive majority. [README.md](https://github.com/msitarzewski/duh/blob/036029611a683ec85d0fa8f9c553bc6e03329253/README.md) describes propose/challenge/revise/commit, preserved dissent and attribution, outcome feedback, and confidence calibration. It also links a benchmark comparing multiple answering methods.

## What to mine

Keep stable evaluation questions, model/configuration records, attributed critiques, minority positions, external outcomes, and cost/latency. Separate agreement, confidence, and correctness in reports.

## Exclusions and proposed adaptation

Do not adopt the hosted service, whole consensus platform, or assume debate proves truth. Propose a small repeatable comparison suite for harness/model choices, using task-specific acceptance criteria and independent checks where available.

## Next analysis

Inspect [docs/reference/benchmarks.md](https://github.com/msitarzewski/duh/blob/036029611a683ec85d0fa8f9c553bc6e03329253/docs/reference/benchmarks.md) and [docs/concepts/how-consensus-works.md](https://github.com/msitarzewski/duh/blob/036029611a683ec85d0fa8f9c553bc6e03329253/docs/concepts/how-consensus-works.md). Review benchmark selection, judge bias, repeated trials, and how outcomes update calibration. Include correlated wrong answers and persistent dissent. Compare improvement against extra cost and latency.

The source is AGPL-3.0 as reported by its README/license metadata; this note copies no implementation. Any future extraction needs a separate review of the exact files and applicable terms.
