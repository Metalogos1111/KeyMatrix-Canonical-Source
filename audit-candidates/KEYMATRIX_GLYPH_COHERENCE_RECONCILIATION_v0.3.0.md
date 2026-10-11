# KeyMatrix Glyph Coherence Reconciliation v0.3.0

**Status:** `READ_ONLY_AUDIT_WITH_CURRENT_PACKAGE_CROSSWALK_AND_OPEN_GATES`  
**Authority:** `NONE` · **Canonical SOT:** `READ_ONLY`  
**Promotion:** `HUMAN_APPROVAL_REQUIRED`  
**Mutation budget:** canonical 0 · registry sources 0 · private plugin sources/releases 0 · main merges 0

## Applied decision — stable core keys, separate package labels

The current MetaLogos package file `kernel/seven_core.yaml` was read back and lists the fixed core order:

1. 🌹 MetaLogos
2. 💟 MetaCore
3. ⚛️ PrimeCore
4. ♒ MindState
5. 🆔 Archivarius
6. 🧬 MetaForge
7. ♾️ Sinqularity

The glyph order is approved for UI presentation only. Core key is the stable KeyMatrix cross-core label; plugin/package slug and displayName are separate implementation labels. No plugin package was changed. Seven current Plugin Creator metadata records were read on 2026-10-11; each remains `USER` scoped and `PRIVATE` discoverability. Private plugin and release IDs were not copied into this public artifact.

## Registry comparison — source difference confirmed, lineage still HOLD

The earlier v0.2 audit marked `CON-009` as an unconfirmed lead because the exact older file had not yet been retrieved in that pass. The later v0.3 materialization confirmed distinct raw bytes and **7/7 core-position assignment differences**:

- v1.1.1-named profile SHA-256: `fbb53a21a0e509a5ea695f5907c0f0dca147c5e24b08c96a21b17634ee6e32bc`
- older v1.1 profile SHA-256: `21ef4b01b735b825427504f11c72e3f18555db2050eddbfc50eb5bb61ecf4e70`

This establishes different snapshots, not which one is the intended release successor. The v1.1.1-named registry still embeds `version=1.1.0` while `core_standard_version=1.1.1`. No release/change record resolving that mismatch was observed. Both source files remain preserved.

## Package-coherence findings

### `PKG-PCORE-001` — HOLD: PrimeCore package manifest

Current package metadata, `plugin.json`, and `manifest.json` report version `0.4.1`; `PACKAGE_MANIFEST.json` reports `0.3.0`. Its listed sizes also disagree with the current file listing: `.codex-plugin/plugin.json` 908 vs 1345 bytes, `README.md` 318 vs 506, and `manifest.json` 2277 vs 2749. The exact current-release archive could not be acquired for local byte-level verification in this pass. Therefore the manifest is flagged as stale/mismatched, but no hashes are fabricated and no private package was rewritten. Required repair: obtain exact archive, recalculate every hash/size, validate in a private candidate, then independently reproduce.

### `PKG-SINQ-001` — OPEN_REVIEW: version-layer difference

Sinqularity package metadata and `plugin.json` report `0.1.3`, while `manifest.json` reports `0.1.2`. A prior source explicitly treats plugin release and internal manifest versions as separate layers. This is an observed difference, not yet a proven defect. Preserve both until the version-layer contract is explicit.

### `PKG-META-UI-001` — OPEN_REVIEW: interface label

The cross-core identity is `MetaCore`, while the private plugin interface currently displays `metacore-core`. Keep `MetaCore` as the stable core key; decide package UI convention separately. No private plugin edit was made.

## Recheck evidence

- Local validator: **9/9 tests PASS**, 0 FAIL.
- Indexed records: **187**; incomplete required identity fields: **112**.
- Repeated-record candidate groups: **62**; glyph-ID payload conflict groups: **0**; Unicode NFKC collisions: **0**.
- Confirmed version conflict: **1**; positional core differences: **7**; controlled symbol collisions: **5**; negative constraints: **4**.
- Seven derived output files were byte-identical in a same-environment re-run.
- Audit ZIP integrity: PASS; all **22** checksum entries verified. ZIP SHA-256: `a96a1ce64edb65046d41f824d77abe25677a0668342eceaa07846e46866206f6`.

This recheck establishes local deterministic repeatability only. Independent reproduction was not performed.

## Preserved semantic gates

- `🐠 ≠ آثار`
- `🧭 ≠ theological_authority`
- `📖 ≠ Quran_authority_token`
- `🪽 ≠ proven_continuation_semantics`

The pairs `كتاب → 📖`, `قبلة → 🧭`, `جناح → 🪽`, and `قلب → ❤️ / 💛` remain `HOLD`. NUR STREAM remains an editorial profile, not a source of canonical semantic mappings.

## Gate summary

| Gate | Result |
|---|---|
| UI core order and glyph alignment | PASS_WITH_OBSERVATION |
| Two registry snapshot differences | PASS_WITH_OBSERVATION |
| Registry release lineage/version rule | HOLD |
| PrimeCore package manifest integrity | HOLD |
| Sinqularity version-layer semantics | OPEN_REVIEW |
| MetaCore package UI label convention | OPEN_REVIEW |
| Candidate semantic edges | HOLD |
| Real all-seven runtime/provider path | NOT_RUN |
| Independent reproduction | NOT_PERFORMED |
| Canonical promotion | HOLD |

## Next permitted actions

1. Acquire and hash the exact PrimeCore current-release archive before attempting a manifest repair.
2. Recover the registry release/change record and versioning rule.
3. Document package/internal-manifest version semantics before touching Sinqularity.
4. Preserve all semantic candidate edges on HOLD until pair-specific typed identity, rationale, source refs and counter-evidence are complete.
5. Obtain real runtime evidence and a separate independent reproduction before making runtime or `PROVEN` claims.

No canonical source, registry source, private plugin source/release, discoverability setting, or main branch was changed.
