# KM Evidence Lineage Map v0.2.0

**State:** READ_ONLY / EVIDENCE_FIRST — `PASS_WITH_OBSERVATION` for text-level mapping; archive integrity remains **HOLD**.

## Scope

- Source: `evidence` v1.0.0, current release ID recorded in the private audit receipt only.
- Target: `primecore-quantum-hybrid` v0.4.1.
- Inventory: 32 source files, 45 target files, 25 shared paths, 19 exact text matches and 6 differing shared text payloads.
- Raw archives were not acquired; no archive SHA-256 or fresh per-file hashes were computed. Existing manifest hashes are treated as declarations, not current independent measurements.

## Record-by-record lineage

| ID | Source → target | Observed relation | Disposition |
|---|---|---|---|
| EL-001 | `evidence/P1_P2_GATE_EVIDENCE.json` → same path | Exact text payload; declared SHA-256 `48cc…6040` | Preserve original source release and all field pointers; historical assertions are not freshly verified. |
| EL-002 | `evidence/baseline_input.json` → same path | Exact text payload; declared SHA-256 `4110…71ee` | Preserve path and input values; input is not execution proof. |
| EL-003 | `evidence/baseline_verification_p1p2.json` → same path | Exact text payload; declared SHA-256 `938f…59b7` | Preserve both run IDs, result hashes, and scope; do not reuse IDs. |
| EL-004 | `evidence/first_run.json` → same path | Exact text payload; declared SHA-256 `99a3…e947` | Preserve as a distinct historical first-run record. |
| EL-005 | `evidence/verification.json` → same path | Exact text payload; same declared SHA-256 as EL-003 | Preserve filename/path identity even though payload matches the baseline verification record. |
| EL-006 | `PACKAGE_MANIFEST.json` → target manifest | Different inventories and snapshot semantics | Keep source manifest as historical provenance; do not overwrite or recalculate. |
| EL-007 | `PACKAGE_SHA256.txt` → target digest file | Per-file digest list vs one manifest-level digest | Preserve both formats and source list; do not copy hashes across versions. |
| EL-008 | `manifest.json` → target manifest | Source v0.2.0 snapshot vs target v0.4.1 | Preserve both. Source declares deterministic math and deferred NFS/ECM/AI/Quantum; target includes later bounded MindState/provenance surfaces. |
| EL-009 | `README.md` → target README | Different package descriptions | Keep target README; retain source README only as provenance. |
| EL-010 | `.codex-plugin/plugin.json` → target interface | Different interface metadata | Do not copy source interface over target interface. |
| EL-011 | `docs/UNIFIED_CONTRACT.md` → target contract | Contract snapshots differ | Preserve both; compare clauses before consolidation. |
| EL-012 | `docs/P1_P2_GATE_REPORT.md` → same path | Exact text payload; declared SHA-256 `282c…75d5` | Historical report only; rerun tests on the eventual assembled candidate. |
| EL-013 | 19 shared paths | Exact text payload equality on readback | Reference the target copy while retaining source release provenance. This is not raw archive hash equality. |
| EL-014 | 7 cache/bytecode-only paths | Generated pytest cache / Python bytecode | Exclude only from a clean candidate build; do not delete source files. |

The JSON companion contains field-level JSON pointers for EL-001–EL-012 and all gate limitations.

## Historical release boundary

The existing EPM-04 record names the earlier PrimeCore target v0.3.5 and its release ID. The current target package metadata is v0.4.1. EPM-04 must remain a historical record; its target identity cannot be silently rewritten.

## Test receipt

The reconstructed-text local suite produced 9/9 passing tests and a separate-process golden-vector result of `259106859`. This is `PASS_WITH_OBSERVATION`, not a packaged-candidate test or independent reproduction of the full candidate. See [test receipt](KM_EVIDENCE_CANDIDATE_TEST_RECEIPT_v0.1.0.json).

## Gates

- **PASS_WITH_OBSERVATION:** source/target metadata, inventories, selected payload equality, line-level pointers and non-destructive dispositions.
- **HOLD:** acquire exact current source and target archive bytes and compute archive hashes.
- **HOLD:** verify every manifest size/hash against extracted exact bytes.
- **BLOCKED:** assemble the separate candidate package until exact archives are available.
- **NOT_PERFORMED:** independent reproduction of the assembled candidate package.
- **REQUIRES_HUMAN_APPROVAL:** any retirement of standalone `evidence`.

No provider call, private plugin mutation, deletion, release, deployment, canonical write or merge was performed.
