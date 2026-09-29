# AGENT-ZERO — persistent state and compaction recovery

Status: analysis/reference only; not an installed skill, implementation, or approved specification.

Source: [msitarzewski/AGENT-ZERO](https://github.com/msitarzewski/AGENT-ZERO). Revision and license: [source ledger](./SOURCES.md).

## Problem and observed source pattern

Long runs can lose decisions and repeat work after context compaction. [README.md](https://github.com/msitarzewski/AGENT-ZERO/blob/cdbceb1b79121af5b9552cd9143cc0caa9031e54/README.md) describes an explicit development state machine. The Compaction Protocol in [AGENTS.md](https://github.com/msitarzewski/AGENT-ZERO/blob/cdbceb1b79121af5b9552cd9143cc0caa9031e54/AGENTS.md) persists state at transitions and reloads the Memory Bank after compaction.

## What to mine

Keep a small active-context record, current phase, completed milestones, decisions, test evidence, blockers, and the next concrete action. Separate durable decisions from transient progress so a restart can recover without rereading a whole conversation.

## Exclusions and proposed adaptation

Do not adopt the entire Memory Bank or every workflow gate. Avoid exhaustive reuse analysis on trivial changes and redundant logs. For the harness, propose a compact checkpoint at meaningful transitions, with references to artifacts and checks rather than copied output.

These are candidate requirements, not changes to the running harness or authoritative agent instructions.

## Next analysis

Simulate interruption during implementation and after verification. Check that recovery preserves user constraints, detects stale file state, and resumes without repeating completed work or treating an old test result as proof for a new revision.
