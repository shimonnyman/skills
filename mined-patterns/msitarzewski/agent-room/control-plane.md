# Agent Room — evidence-backed completion

Status: analysis/reference only; not an installed skill, implementation, or approved specification.

Source: [msitarzewski/agent-room](https://github.com/msitarzewski/agent-room). Revision and license: [source ledger](../SOURCES.md).

## Problem and observed source pattern

A worker's completion claim needs inspectable support. [README.md](https://github.com/msitarzewski/agent-room/blob/c48e8036159c2bf0a03473a3352457a2ef2c3e7e/README.md) separates normalized coordination state from authoritative source systems. It describes immutable events, transactional projections, artifact integrity, explicit approvals, and audit records.

The documented foundation does not yet ship an isolated production worker service; production in-process Codex/Claude execution is disabled.

## What to mine

Represent a completion claim separately from artifact references, verification results, source identity, and the revision being verified. Preserve who requested and approved consequential actions and what actually happened. Keep Git and CI authoritative for their own facts.

## Exclusions and proposed adaptation

Do not import Go, React, OIDC, PostgreSQL, or the whole control plane solely to add a completion record. Propose a small evidence contract for the harness; LCARS could present the same record as a review surface. Database operations are a separate [mining target](postgresql-production-patterns.md).

## Next analysis

Inspect [boot.md](https://github.com/msitarzewski/agent-room/blob/c48e8036159c2bf0a03473a3352457a2ef2c3e7e/boot.md) and [api/openapi/agent-room.v1.yaml](https://github.com/msitarzewski/agent-room/blob/c48e8036159c2bf0a03473a3352457a2ef2c3e7e/api/openapi/agent-room.v1.yaml). Trace one claim through artifact verification, rejection, and human intervention. Test missing evidence, changed revisions, duplicate events, and stale approval. A model assertion or successful process exit alone should not satisfy the proposed completion contract.
