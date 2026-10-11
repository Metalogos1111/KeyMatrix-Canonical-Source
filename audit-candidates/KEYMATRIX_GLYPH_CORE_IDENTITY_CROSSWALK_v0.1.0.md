# KeyMatrix Glyph/Core Identity Crosswalk v0.1.0

**Status:** OBSERVED_METADATA_CROSSWALK / PACKAGE_DRIFT_HOLD  
**Authority:** NONE · **Canonical SOT:** READ_ONLY  
**Scope:** read-only Plugin Creator metadata and current-release file inspection, 2026-10-11.  
**Private identifiers:** not copied into this public candidate artifact.

## Fixed core order and display-layer rule

The current MetaLogos package file `kernel/seven_core.yaml` read back this exact order: `MetaLogos → MetaCore → PrimeCore → MindState → Archivarius → MetaForge → Sinqularity`. The approved glyph display profile maps the same order to `🌹 💟 ⚛️ ♒ 🆔 🧬 ♾️`.

**Coherence rule:** `core_key` is the KeyMatrix identity. The plugin/package display name is a secondary implementation label. Do not rename a core based solely on a plugin slug or interface `displayName`.

| # | Glyph | Core key | Package display name | Observed package version |
|---:|---|---|---|---|
| 1 | 🌹 | MetaLogos | MetaLogos 7Core Kernel | 100.0.88 |
| 2 | 💟 | MetaCore | `metacore-core` (interface currently uses lowercase label) | 1.0.4 |
| 3 | ⚛️ | PrimeCore | PrimeCore Quantum Hybrid | 0.4.1 |
| 4 | ♒ | MindState | MindState — KeyMatrix Cognitive State | 0.1.6 |
| 5 | 🆔 | Archivarius | Archivarius — Evidence-Bound Memory Core | 0.1.4 |
| 6 | 🧬 | MetaForge | MetaForge Turbo Max | 1.3.3 |
| 7 | ♾️ | Sinqularity | Sinqularity | 0.1.3 |

All seven package metadata lookups returned `scope=USER` and `discoverability=PRIVATE`. This is package metadata, not host/runtime proof.

## New coherence findings

### `PKG-PCORE-001` — HOLD: PACKAGE_MANIFEST drift

PrimeCore's current package metadata, `plugin.json`, and `manifest.json` report version `0.4.1`, but `PACKAGE_MANIFEST.json` reports `0.3.0`. Its stored file sizes also conflict with the current file list: `.codex-plugin/plugin.json` 908 declared vs 1345 observed, `README.md` 318 vs 506, and `manifest.json` 2277 vs 2749. Treat this package manifest as stale or mismatched until exact current-release bytes are hashed and the manifest is regenerated in a separate candidate release.

### `PKG-SINQ-001` — HOLD: version-layer drift

Sinqularity's package metadata and `plugin.json` report `0.1.3`; `manifest.json` reports `0.1.2`. Preserve both observed values until the version-layer contract establishes whether these fields should match.

### `PKG-META-UI-001` — candidate UI label drift

KeyMatrix core identity is `MetaCore`, while the private package's current interface `displayName` is `metacore-core`. The crosswalk retains `MetaCore` as the core key; no private plugin edit was made.

## Registry release lineage still on HOLD

The glyph registry filename says `v1.1.1`, embedded `version` says `1.1.0`, and `core_standard_version` says `1.1.1`. The package identity crosswalk supports the fixed order and candidate glyph labels, but **does not establish registry release lineage**. No registry source was edited.

## Gate summary

| Gate | Result |
|---|---|
| Frozen core order read from current package | PASS_WITH_OBSERVATION |
| Seven private package metadata records observed | PASS_WITH_OBSERVATION |
| Package manifests internally consistent | HOLD |
| All-seven runtime observed | NOT_RUN |
| Independent verification | NOT_PERFORMED |
| Registry release lineage resolved | HOLD |
| Private plugin mutation/release | HOLD |

## Next action

Create a private, non-published candidate repair for the stale PrimeCore package manifest and the Sinqularity version mismatch, then compute exact archive/file hashes, run package validators and independent reproduction. Do not publish plugin releases or change the registry until the version-layer rules and human release gate are explicit.
