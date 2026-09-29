# glas.sh — risk-rated proposals and confirmation

Status: analysis/reference only; not an installed skill, implementation, or approved specification.

Source: [msitarzewski/glas.sh](https://github.com/msitarzewski/glas.sh). Revision and license: [source ledger](./SOURCES.md).

## Problem and observed source pattern

Natural-language command generation needs a clear boundary before execution. [README.md](https://github.com/msitarzewski/glas.sh/blob/229a80e1b2003a233c9e21b570cc1bcf36ce7184/README.md) describes a Command Assistant with safe/moderate/destructive labels, deterministic response parsing, and mandatory user confirmation.

## What to mine

Keep proposal and execution separate. Show the exact action, target, expected effect, and risk before confirmation. Preserve a record linking the authorized proposal to its execution outcome.

## Exclusions and proposed adaptation

Do not import the full Swift terminal, Apple Foundation Models dependency, or treat a model-generated risk label as an authorization decision. For LCARS, map proposals onto registered actions with validated arguments and deterministic policy checks. The confirmation pattern is a candidate product behavior, not a new blanket approval rule for all work in this repository.

## Next analysis

Trace confirmation through the execution boundary and inspect malformed-response handling. Test edited targets after confirmation, repeated execution, cancellation, and a dangerous command incorrectly labeled safe. Define when material changes to a proposal invalidate prior confirmation.
