# KeyMatrix Glyph Coherence Reconciliation v0.1.0

**Status:** CANDIDATE_RECONCILIATION_CREATED / HOLD_FOR_HUMAN_APPROVAL  
**Mode:** READ_ONLY / EVIDENCE_FIRST / DERIVED_CONTROL_LAYER  
**Authority:** NONE  
**Canonical SOT:** READ_ONLY  
**Canonical mutations:** 0  
**Source rewrites:** 0  
**Automatic promotions:** 0

## Purpose

This branch contains a derived reconciliation overlay only. It does not modify, merge, replace, or promote either registry. The two source profiles remain separate because their exact content differs.

## Confirmed conflict

The filename `KeyMatrix_Glyph_Coherence_Registry_v1.1.1_20261005.json` contains embedded `version=1.1.0` while `core_standard_version=1.1.1`. It shares an `artifact_id` with the older file, but the exact source bytes differ. Seven of seven core positions have different assignments and/or identities.

## Coherence improvement applied

1. Introduced a side-by-side, source-addressable conflict ledger for all seven core positions.
2. Defined the qualified identity tuple `visible_symbol + namespace + role + position`; epistemic status and provenance stay separate.
3. Preserved five grammar-declared symbol collisions as context-qualified roles, not merge instructions.
4. Preserved all four negative constraints and four held candidate pairs.
5. Separated NUR STREAM publication rules from canonical semantic mapping.
6. Added an explicit human-review gate before selecting a display profile.
7. Specified a safe fallback: render core names and roles as text while the glyph profile is unresolved.

## Candidate profile

The v1.1.1-named registry is nominated **for human review only** because it declares `core_standard_version=1.1.1` and an explicit fixed seven-core order. This is not a claim of canonical authority. Its embedded-version conflict remains open; activation is disabled until human approval.

## Required decision

A human reviewer must confirm the intended seven-core profile and provide the relevant release/change record. Until then, both source registries remain intact, canonical SOT remains read-only, and candidate concept→glyph edges remain HOLD.

## Verification boundary

This artifact is a derived control layer. It does not establish runtime, deployment, canonical promotion, or independent verification.
