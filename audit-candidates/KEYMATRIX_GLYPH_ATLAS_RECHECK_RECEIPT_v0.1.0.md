# KeyMatrix Glyph Atlas — Recheck Receipt v0.1.0

**Result:** PASS_WITH_OBSERVATION  
**Mode:** READ_ONLY / EVIDENCE_FIRST  
**Authority:** NONE  
**Canonical SOT:** READ_ONLY  
**Mutation budget:** canonical SOT 0 · source artifacts 0 · automatic promotions 0

## Recheck observed

- Existing standard-library validator ran again against the same materialized source snapshots.
- Validator tests: **9/9 PASS**, 0 FAIL.
- Indexed records: **187**; incomplete identity records: **112**.
- Repeated-record candidate groups: **62**; glyph-ID payload conflict groups: **0**; Unicode NFKC collision groups: **0**.
- Confirmed version conflict: **1**; core position differences: **7**; declared controlled symbol collisions: **5**; explicit negative constraints: **4**.
- Seven generated report outputs are byte-identical to the previous audit package outputs.
- ZIP integrity check passed; all **22** file checksum entries in the package manifest verified.

## Package and source evidence

- Audit ZIP SHA-256: `a96a1ce64edb65046d41f824d77abe25677a0668342eceaa07846e46866206f6`
- Validator SHA-256: `b27db824a3910f4f7ac5293e36d3f9102d27935674ced14d05b90b14fb240a15`
- Older v1.1 registry SHA-256: `21ef4b01b735b825427504f11c72e3f18555db2050eddbfc50eb5bb61ecf4e70`
- v1.1.1-named registry SHA-256: `fbb53a21a0e509a5ea695f5907c0f0dca147c5e24b08c96a21b17634ee6e32bc`

## History reconciliation

The earlier v0.2.0 audit marked the older-registry assignment discrepancy as an unconfirmed lead because that exact source had not been retrieved in that pass. The later v0.3.0 source materialization and comparison now confirm different source bytes and seven core-position differences between the two measured registry snapshots. The earlier finding remains historically accurate for its own scope; this receipt records the later update.

**Still unresolved:** which registry is the intended release successor. The filename/embedded-version conflict remains, and no release manifest/change log proving release lineage was observed in the reviewed scope.

## Boundaries

This result establishes repeatability in the same environment only. It does not establish an independent reproduction, runtime implementation, deployment, canonical authority, or glyph-edge promotion. Runtime remains `NOT_OBSERVED`; independent verification remains `NOT_PERFORMED`; canonical promotion remains `HOLD`.

## Next permitted action

Retrieve the release/change record and the remaining provenance artifacts, validate exact project-side source bytes, and arrange a separate independent reproduction. Do not merge registries or promote candidate mappings until those gates are met.
