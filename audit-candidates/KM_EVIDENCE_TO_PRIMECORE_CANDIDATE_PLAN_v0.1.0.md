# Evidence → PrimeCore Candidate Plan v0.1.0

**Status:** CANDIDATE PLAN ONLY / PACKAGE ASSEMBLY BLOCKED.

This is a non-canonical audit artifact, not an updated plugin package. The source package `evidence` v1.0.0 remains untouched and available.

## Candidate rules

1. Preserve all five source evidence record paths, source package identity, current source release reference, embedded run IDs, hashes, and original timestamps.
2. Keep `PACKAGE_MANIFEST.json`, `PACKAGE_SHA256.txt`, `manifest.json`, `README.md`, `.codex-plugin/plugin.json`, and `docs/UNIFIED_CONTRACT.md` as separate source provenance records. Never overwrite the target files with these source snapshots.
3. Existing exact-text-shared contracts, skills, source and tests should be referenced from the current target rather than copied blindly. Retain the source release lineage.
4. Exclude seven generated cache/bytecode paths from the clean candidate build only. No source deletion.
5. Keep PrimeCore-only verification boundary, EPM-04–07 historical records, MindState source, migration tests, and target metadata intact.
6. Do not recalculate manifests until both exact release archives are available and their raw bytes and extracted file bytes can be hashed.

## Gate status

- Lineage map: PASS_WITH_OBSERVATION.
- Reconstructed-text regression: PASS_WITH_OBSERVATION, 9/9 tests.
- Negative-authority controls: PASS_WITH_OBSERVATION for five injected fields on reconstructed source text.
- Exact archive bytes: NOT_OBSERVED.
- Fresh manifest verification: NOT_RUN.
- Packaged candidate build: BLOCKED.
- Independent reproduction of assembled candidate: NOT_PERFORMED.
- Retirement: NOT_AUTHORIZED; human approval required.

See [lineage map](KM_EVIDENCE_LINEAGE_MAP_v0.2.0.md) and [test receipt](KM_EVIDENCE_CANDIDATE_TEST_RECEIPT_v0.1.0.json).
