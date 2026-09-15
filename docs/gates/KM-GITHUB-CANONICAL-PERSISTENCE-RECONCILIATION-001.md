# KM-GITHUB-CANONICAL-PERSISTENCE-RECONCILIATION-001

## Purpose
Controlled GitHub persistence and evidence-reconciliation boundary for KeyMatrix.

GitHub is a persistence/provenance plane. It is not technical authority, SOT, runtime verifier, or deployment controller.

## Hard boundaries
- DOCUMENTED != IMPLEMENTED != DEPLOYED != VERIFIED != PROVEN
- No synthetic PASS.
- No hidden authority.
- No implicit ALLOW.
- BRANCH PERSISTENCE != CANONICAL PROMOTION
- `main` must remain unchanged by this gate.
- Canonical promotion is forbidden by this gate.
- Evidence status must be derived from observable evidence.

## Controlled branch
- Repository: `Metalogos1111/KeyMatrix-Canonical-Source`
- Base: `main`
- Base SHA: `8c37863402d92dc65829a1d27036b32c80ea4029`
- Branch: `km-github-evidence-reconciliation-001`

## Pair-01 provenance reconciliation
Authoritative observed `MetaCore12 Backend Server` SHA-256:
`0e996e091f83849b2f8891fa30e856f448ce072b9ba181dda9b8c475f05a4efc`

Persisted no-mutation state hash:
`045f856b2b853d04004c34b8faba34b89734c5ec2f29854623d2826463e0e2eb`

The persisted Pair-01 evidence JSON must contain the authoritative backend hash and equal before/after state hashes when declaring `state_mutation_observed=false`.

## Verification requirements
1. Exact branch-vs-main diff contains only controlled expected scope.
2. `CANONICAL_SOURCE_ROOT.md` is unchanged.
3. Registry parses and preserves authority/SOT/status boundaries.
4. Pair-01 evidence remains `OBSERVED / COMPATIBILITY_NOT_SCORED`.
5. Persisted MetaCore12 source SHA equals the correction SHA.
6. State before/after hashes are equal when evidence declares no mutation.
7. Secret-pattern scan rejects introduced prohibited credential material.
8. CI success is not compatibility proof or merge authorization.

## Promotion boundary
No Core identity promotion, compatibility promotion, production claim, or canonical promotion is authorized by this gate.