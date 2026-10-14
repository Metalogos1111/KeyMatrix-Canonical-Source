# Evidence → PrimeCore Migration Map v0.1.0

**Status:** `MIGRATION_MAP_OBSERVED / RETIREMENT_HOLD`  
**Observed:** 2026-10-14 · **Authority:** NONE · **Canonical SOT:** READ_ONLY  
**Promotion:** HUMAN_APPROVAL_REQUIRED

## Inventory and comparison

- Standalone `evidence` package: **32 files**, version `1.0.0`, USER / PRIVATE.
- Target `primecore-quantum-hybrid`: **45 files**, version `0.4.1`, USER / PRIVATE.
- Shared paths from file inventories: **25**.
- Shared paths whose text was compared: **25**.
- Exact returned-text matches: **19**.
- Different returned-text payloads: **6**.

This is direct source-text comparison through Plugin Creator, not raw archive hashing. No archive was acquired, and no independent reproduction was performed.

## Six shared paths that differ

| Path | Evidence package | PrimeCore | Decision |
|---|---|---|---|
| `README.md` | candidate v0.2.0 description | current v0.4.1 description | Preserve evidence README as history; do not overwrite current README. |
| `.codex-plugin/plugin.json` | evidence package interface | PrimeCore interface | Keep package identity/interface separate. |
| `docs/UNIFIED_CONTRACT.md` | modular arithmetic only is bound; NFS/ECM/AI/Quantum deferred | adds MindState result/transition boundary | Preserve both; clause-by-clause review before consolidation. |
| `manifest.json` | v0.2.0 package manifest | v0.4.1 package manifest | Keep as separate historical records. |
| `PACKAGE_MANIFEST.json` | 0.2.0 sandbox candidate inventory | 0.3.0 manifest in current 0.4.1 package; Library says it may be a historical integrity snapshot | HOLD until intended scope and exact archive bytes are established. |
| `PACKAGE_SHA256.txt` | per-file SHA-256 listing | manifest-level digest line only | Preserve historical evidence; recompute only from exact candidate bytes. |

## Shared paths that matched exactly (19/25)

- Five schemas: `adapter_contract`, `evidence`, `mindstate_result_packet`, `primecore_request`, `primecore_result`.
- `docs/P1_P2_GATE_REPORT.md`.
- Five evidence records: `P1_P2_GATE_EVIDENCE.json`, `baseline_input.json`, `baseline_verification_p1p2.json`, `first_run.json`, `verification.json`.
- Five skills: `evidence`, `metaforge`, `mindstate`, `primecore`, `verification`.
- `src/primecore_qh/__init__.py`, `src/primecore_qh/core.py`, `tests/test_core.py`.

The same source and test payloads in both packages indicate that no unique core algorithm was observed in the standalone evidence package in this comparison. That does not mean its provenance/evidence records can be discarded.

## Evidence-only paths: generated cache, not migration value

The seven evidence-only paths in the current inventory are `.pytest_cache` entries and `__pycache__` bytecode files. Proposed candidate migration should exclude these generated artifacts. This is a candidate hygiene decision only; no files were deleted.

## PrimeCore-only material to preserve

PrimeCore has additional migration evidence (`EPM-04` through `EPM-07`), verification-boundary schema, MindState runtime code/evidence, independent reproduction test source, migration tests, shared sync contract, and UI assets. These remain separate package records; the migration must not collapse verification into execution authority.

## Recommended sequence

1. Build a source-to-target lineage map for each evidence JSON/report and record its current path, content digest basis, run/trace identifiers, and verification state where available.
2. Define the intended `PACKAGE_MANIFEST.json` scope and acquire exact current release archive bytes before regenerating any package hashes.
3. Create a private candidate migration that preserves original evidence records and their provenance; exclude generated caches.
4. Run PrimeCore core tests, migration tests, MindState boundary tests, regression tests, and negative-authority controls against the candidate.
5. Obtain independent reproduction with a separate executor/run ID.
6. Only after all gates pass and explicit human approval, consider retirement of standalone `evidence`.

## Gate state

| Gate | Result |
|---|---|
| Current file inventory | PASS_WITH_OBSERVATION |
| 25 shared paths text-compared | PASS_WITH_OBSERVATION |
| Provenance-complete migration map | HOLD |
| Candidate migration package | NOT_STARTED |
| Candidate regression | NOT_RUN |
| Independent reproduction | NOT_PERFORMED |
| Retire standalone evidence | HUMAN_APPROVAL_REQUIRED |

**No package files, releases, discoverability settings, or canonical sources were changed.**
