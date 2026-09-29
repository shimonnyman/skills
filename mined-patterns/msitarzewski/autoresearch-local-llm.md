# autoresearch-local-llm — change, benchmark, keep or revert

Status: analysis/reference only; not an installed skill, implementation, or approved specification.

Source: [msitarzewski/autoresearch-local-llm](https://github.com/msitarzewski/autoresearch-local-llm). Revision and license: [source ledger](./SOURCES.md).

## Problem and observed source pattern

Autonomous optimization needs an objective result and a way to discard regressions. [README.md](https://github.com/msitarzewski/autoresearch-local-llm/blob/ce9aa72c872e873b4b9ea054039b4f9f2463a8ea/README.md) describes a local Ollama/Qwen researcher modifying training code, checking syntax, committing, running a fixed-duration experiment, and keeping or resetting according to validation bits per byte.

This repository is a fork of [SohniSwatantra/autoresearch-local-llm](https://github.com/SohniSwatantra/autoresearch-local-llm), which credits [karpathy/autoresearch](https://github.com/karpathy/autoresearch).

## What to mine

Keep one bounded change, a fixed benchmark, baseline and candidate evidence, a decision rule, and a recoverable experiment history.

## Exclusions and proposed adaptation

Do not import the GPU training setup, infinite loop, cloud deployment, or reset behavior. Propose isolated experiments for startup time, memory use, or model configurations with correctness checks, explicit resource budgets, and a stop condition. Reversion must affect only the experiment's changes.

## Next analysis

Inspect [agent.py](https://github.com/msitarzewski/autoresearch-local-llm/blob/ce9aa72c872e873b4b9ea054039b4f9f2463a8ea/agent.py) and [program.md](https://github.com/msitarzewski/autoresearch-local-llm/blob/ce9aa72c872e873b4b9ea054039b4f9f2463a8ea/program.md) as reference data. Test noise, failed benchmarks, timeouts, and metric improvements that break correctness. Decide improvement thresholds before running experiments.

No license file or explicit license declaration was found in the inspected repository tree/README. Do not infer permission from a public fork or a different ancestor's license; resolve provenance before copying any code or prompt text.
