# Phase — Ollama-compatible routing (later reference)

Status: analysis/reference only; not an installed skill, implementation, or approved specification.

Source: [msitarzewski/phase](https://github.com/msitarzewski/phase). Revision and license: [source ledger](./SOURCES.md).

## Problem and observed source pattern

Clients can benefit from a stable inference interface while execution location changes. [README.md](https://github.com/msitarzewski/phase/blob/6ee7eb6ee2a232d2ad17f57374953e63b359d441/README.md) describes LUCID's Ollama-compatible API, local-or-peer routing, failover, and signed receipts. It also identifies limitations: peer relay is batch-shaped, model pulling is not a full network download, and serving peers can see routed prompts.

## What to mine later

Keep a provider-neutral client boundary, endpoint configuration, explicit local-only policy, execution-location metadata, and normalized failures. Signed receipts provide provenance/integrity evidence, not proof that an answer is correct.

## Exclusions and proposed adaptation

Keep this as a later-phase reference. Do not deploy a peer network, adopt sharded inference, or imply full Ollama parity. First establish a need beyond one machine and verify the exact API subset required by local clients.

## Next analysis

Inspect [crates/lucidd/README.md](https://github.com/msitarzewski/phase/blob/6ee7eb6ee2a232d2ad17f57374953e63b359d441/crates/lucidd/README.md). Check streaming, cancellation, model identifiers, privacy boundaries, and failover behavior before any integration proposal.

The license boundary matters: the Phase substrate is Apache-2.0, while LUCID is AGPL-3.0-or-later per [crates/lucidd/Cargo.toml](https://github.com/msitarzewski/phase/blob/6ee7eb6ee2a232d2ad17f57374953e63b359d441/crates/lucidd/Cargo.toml). The repository-level Apache license does not describe every component.
