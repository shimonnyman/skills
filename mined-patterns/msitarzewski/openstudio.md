# OpenStudio — capability gating and local AI abstraction

Status: analysis/reference only; not an installed skill, implementation, or approved specification.

Source: [msitarzewski/openstudio](https://github.com/msitarzewski/openstudio). Revision and license: [source ledger](./SOURCES.md).

## Problem and observed source pattern

Optional dependencies should not produce controls that appear usable but fail without explanation. [README.md](https://github.com/msitarzewski/openstudio/blob/dce7d09395ff99bf851b9c3dceda9f6c83d67ba8/README.md) describes a backend capability snapshot at `/api/capabilities`, frontend gating with setup explanations, and an optional AI path using ffmpeg, whisper.cpp, and OpenAI-compatible LLM endpoints.

## What to mine

Detect actual runtime readiness, publish structured availability with an unavailable reason, and let the interface explain prerequisites. Separate transcription and language-model interfaces from a particular local runtime or provider.

## Exclusions and proposed adaptation

Do not import the WebRTC studio, recording workflow, or automated model downloads. For LCARS, propose distinct capabilities for audio capture, transcription, and LLM processing, each with explicit dependencies and failure states. Endpoint compatibility does not itself guarantee local processing; the configured endpoint determines where data goes.

## Next analysis

Follow the capability producer and UI consumer in the source. Inspect setup behavior as data, without running it. Compare missing binary, missing model, unreachable provider, and provider failure after startup. Check how readiness is refreshed and how local-only configuration would be represented.
