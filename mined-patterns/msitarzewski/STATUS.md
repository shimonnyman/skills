# Mining progress — msitarzewski

Reference-only progress tracker for the mining targets in this folder. Status describes our analysis and adaptation work, not upstream implementation maturity. These notes are not installed skills, deployment instructions, or approved architecture.

## Status vocabulary

- **Seeded** — Target, rationale, source entry points, and intended use are recorded; full analysis remains.
- **Analysis in progress** — Focused source inspection or validation has started but is incomplete.
- **Analyzed** — Relevant source behavior has been examined and findings validated, with evidence and limitations recorded.
- **Adaptation spec written** — Findings have been translated into a destination-specific design/specification with acceptance checks; this does not itself authorize implementation.
- **Implemented** — The adaptation has been built or integrated and verified in its destination, with evidence linked.
- **Deferred/Reference** — Retained for later or reference use; no active analysis or implementation is planned.

## Target progress

Initialized from the existing notes on 2026-09-29. All targets remain Seeded except Phase, whose note explicitly defers it to later reference use. Suggested timing alone does not indicate that analysis has begun.

| Target | Status | Next analysis target | Destination/use | Notes |
|---|---|---|---|---|
| [agency-agents](agency-agents.md) | Seeded | Compare shortlisted role contracts with existing skills; evaluate representative tasks and handoff boundaries. | Focused roles for the planner/scout/implementer workflow and skill review. | Extract small contracts; avoid duplicate skills or the full roster. |
| [AGENT-ZERO](agent-zero.md) | Seeded | Simulate interruption and compaction recovery; check stale file state, constraints, and revision-specific test evidence. | Persistent checkpoints for long-running harness tasks. | Keep durable decisions separate from transient progress; avoid adopting the entire Memory Bank. |
| [Agent Room control plane](agent-room/control-plane.md) | Seeded | Inspect `boot.md` and the OpenAPI contract; trace claims through artifact verification, rejection, and human intervention. | Harness completion-evidence contract; possible LCARS review surface. | Test missing evidence, changed revisions, duplicate events, and stale approval; no whole control-plane adoption. |
| [Agent Room PostgreSQL](agent-room/postgresql-production-patterns.md) | Seeded | Inspect the foundation migration, backup/restore scripts, and deployment docs; validate Debian operations and data/artifact restoration. | AI-optional Debian/Linux book service lab. | Ubuntu deployment is reference only; validate least privilege, migrations, systemd, health/readiness, and recovery separately. |
| [OpenStudio](openstudio.md) | Seeded | Trace capability producer and UI consumer; check readiness refresh and missing dependency/provider failure cases. | LCARS transcription, LLM interfaces, and capability gating. | Keep setup explanations explicit; local processing depends on the configured endpoint. |
| [glas.sh](glas-sh.md) | Seeded | Trace confirmation to execution; test malformed responses, changed targets, retries, cancellation, and incorrect risk labels. | LCARS registered actions and risk-rated proposals. | Model risk labels are not authorization; determine when proposal changes invalidate confirmation. |
| [Brew Browser](brew-browser.md) | Seeded | Inspect `src-tauri/` action boundaries and `bundles.json`; verify allowlisting, argument validation, cancellation, and partial failures. | LCARS system actions, capability checks, and hardware-aware recommendations. | Backend enforces availability and permission; hardware suitability remains an estimate until measured. |
| [duh](duh.md) | Seeded | Inspect benchmark methodology and consensus mechanics; assess judge bias, repeated trials, calibration, and persistent dissent. | Repeatable harness/model comparison suite. | Separate agreement, confidence, and correctness; measure cost/latency and review exact-file licensing before extraction. |
| [VectorForge](vectorforge.md) | Seeded | Inspect `docs/QUALITY.md` and `examples/manifest.json`; assess fidelity, editability, text, resource limits, and print suitability. | Print/design assessment workflow. | Automatic classification/recommendation is planned upstream; pixel metrics alone do not establish print quality. |
| [autoresearch-local-llm](autoresearch-local-llm.md) | Seeded | Inspect `agent.py` and `program.md`; assess benchmark noise, failures, timeouts, correctness, and improvement thresholds. | Bounded startup-time, memory, or model-configuration experiments after a baseline exists. | Require budgets, stop conditions, and isolated reversion; licensing/provenance remains unresolved. |
| [Phase](phase.md) | Deferred/Reference | When a need beyond one machine exists, inspect LUCID API coverage, streaming, cancellation, privacy, and failover. | Later provider-neutral inference boundary and routing reference. | Explicitly deferred by its note; do not assume full Ollama parity. Substrate and LUCID have different licenses. |

Update a row when work actually changes, linking supporting analysis, specifications, or verification evidence in Notes. The linked target notes retain detailed scope and exclusions; [SOURCES.md](SOURCES.md) retains upstream revisions and license observations. This tracker does not authorize implementation or alter the installed skill catalog.
