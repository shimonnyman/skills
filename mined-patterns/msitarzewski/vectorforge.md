# VectorForge — classify, trace, render, measure, recommend

Status: analysis/reference only; not an installed skill, implementation, or approved specification.

Source: [msitarzewski/vectorforge](https://github.com/msitarzewski/vectorforge). Revision and license: [source ledger](./SOURCES.md).

## Problem and observed source pattern

An SVG can be valid yet unsuitable for editing or print. [README.md](https://github.com/msitarzewski/vectorforge/blob/db329621f2d66102a4f05cf06eeeb6b992c06f60/README.md) documents explicit VTracer/Potrace selection, SVG safety validation, bounded rendering, image diffs, fidelity metrics, and structural complexity measurements.

Automatic source classification, multi-engine comparison, and recommendation are a planned orchestration layer, not the current automatic request path.

## What to mine

Use the target sequence: classify source → attempt suitable tracing/reconstruction → validate → render → measure → recommend. Keep artifacts and evidence for accept, review, reconstruct, or preserve-raster decisions. Measure command complexity as well as path count.

## Exclusions and proposed adaptation

Do not promise every raster should become a vector or import unfinished neural engines. Propose a print/design assessment workflow that distinguishes line art, flat logos, typography, gradients, and photography. A packaged tool or controlled service would need separate evaluation for a workplace that cannot run Python.

## Next analysis

Inspect [docs/QUALITY.md](https://github.com/msitarzewski/vectorforge/blob/db329621f2d66102a4f05cf06eeeb6b992c06f60/docs/QUALITY.md) and [examples/manifest.json](https://github.com/msitarzewski/vectorforge/blob/db329621f2d66102a4f05cf06eeeb6b992c06f60/examples/manifest.json). Evaluate visual fidelity, editability, text reconstruction, resource limits, and print suitability on redistributable samples. Pixel metrics alone do not establish production quality. Engine dependencies, model weights, and artwork retain their own licensing.
