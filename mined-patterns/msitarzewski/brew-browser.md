# Brew Browser — enumerated actions and capability-aware integration

Status: analysis/reference only; not an installed skill, implementation, or approved specification.

Source: [msitarzewski/brew-browser](https://github.com/msitarzewski/brew-browser). Revision and license: [source ledger](./SOURCES.md).

## Problem and observed source pattern

A desktop interface needs predictable system actions across differing host capabilities. [README.md](https://github.com/msitarzewski/brew-browser/blob/e2e222f4e87f56b679504036b7e6137b1fc7e51e/README.md) documents specific package/service operations, streaming output, and capability-aware integrations. It states that Rust builds Homebrew invocations from enumerated inputs, with no arbitrary shell execution exposed to the frontend. Optional GitHub integration on Linux depends on Secret Service/keyring availability while core operations remain usable.

## What to mine

Study the native action boundary in `src-tauri/` and bundle metadata in `bundles.json`. Extract an explicit operation registry, validated arguments, capability checks, progress events, and structured failure results. Study hardware-aware bundle suitability as a reference for model/resource recommendations.

## Exclusions and proposed adaptation

Do not import the Homebrew product, macOS assumptions, or expose an arbitrary shell operation. Propose LCARS actions with stable identifiers and typed parameters; let the backend enforce availability and permission independently of the UI.

## Next analysis

Trace representative install, uninstall, and service actions to the process-launch boundary. Confirm allowlisting and argument validation in code rather than relying on the operation list alone. Test missing package manager, missing keyring, unsupported host, cancellation, and partial failure. Treat hardware suitability estimates as estimates until measured.
