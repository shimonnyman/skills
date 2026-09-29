# Mined patterns from msitarzewski repositories

Analysis/reference material for the existing skills catalog. These are seed notes for further inspection, not installed skills, copied implementations, deployment instructions, or approved architecture.

Reviewed: 2026-09-29. Each note separates observed source behavior from desired extraction and proposed adaptation. No upstream source code or role-prompt bodies are copied. Source links, reviewed revisions, and license observations are in [SOURCES.md](SOURCES.md).

## Mining index

| Source | Pattern / note | Intended use | Suggested timing |
|---|---|---|---|
| agency-agents | [Selected role contracts](agency-agents.md) | Focused agent roles and skill review | First pass |
| AGENT-ZERO | [Persistent state and compaction recovery](agent-zero.md) | Long-running harness tasks | First pass |
| Agent Room | [Evidence-backed completion](agent-room/control-plane.md) | Claims, artifacts, verification, approvals, audit | First pass |
| Agent Room | [PostgreSQL production patterns](agent-room/postgresql-production-patterns.md) | Debian/Linux book service lab | Book planning |
| OpenStudio | [Capabilities and local AI abstraction](openstudio.md) | LCARS transcription and LLM integration | First pass |
| glas.sh | [Risk-rated proposals and confirmation](glas-sh.md) | LCARS registered actions | First pass |
| Brew Browser | [Enumerated actions and system capabilities](brew-browser.md) | LCARS system integration | First pass |
| duh | [Multi-model evaluation](duh.md) | Repeatable model/harness comparisons | Evaluation planning |
| VectorForge | [Classify, trace, render, measure, recommend](vectorforge.md) | Print/design assessment | Design workflow study |
| autoresearch-local-llm | [Change, benchmark, keep or revert](autoresearch-local-llm.md) | Bounded optimization experiments | After a baseline exists |
| Phase | [Ollama-compatible routing](phase.md) | Provider-neutral inference boundary | Later reference |

Timing is a proposed analysis order, not implementation authorization.

## How to use these notes

1. Pick a concrete local problem and read only its note and linked source sections.
2. Confirm the source behavior at the recorded revision; distinguish documentation claims from tested behavior.
3. Extract the smallest useful concept or interface and record exclusions.
4. Write a destination-specific specification and acceptance checks before implementation.
5. Review exact-file licenses and attribution before copying any code or prompt text.

The existing skill catalog and its counts remain separate: this directory deliberately contains no `SKILL.md`, installer, runtime code, or automatic integration.

## Important boundaries

- Agent Room's Ubuntu deployment is reference material for a separately validated Debian adaptation.
- VectorForge's automatic classification/recommendation layer is planned; its deterministic trace/validate/render/measure path is documented as implemented.
- Phase remains a later reference and has different licenses for its substrate and LUCID.
- autoresearch-local-llm has unresolved licensing in the inspected fork.
