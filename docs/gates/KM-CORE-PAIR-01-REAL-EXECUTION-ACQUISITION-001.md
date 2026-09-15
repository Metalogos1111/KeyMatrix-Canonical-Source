# KM-CORE-PAIR-01 — REAL EXECUTION ACQUISITION v1

## STATUS
TARGET / BLOCKED — acquisition gate only.

## PURPOSE
Acquire a genuinely executable inference surface for the frozen Pair-01 task without weakening KeyMatrix authority, secret, provenance, or verification boundaries.

## HARD BOUNDARIES
- No synthetic inference.
- No mock output may be scored as real inference.
- No secret may enter HTML, browser storage, client bundle, evidence artifact, or Git history.
- service_role, provider API keys, signing keys, private trust-root material, and database secrets remain server-side.
- UI is requester/observer only.
- GitHub is persistence/provenance, not technical authority.
- No SOT mutation.
- No canonical promotion.
- No production promotion.
- Missing runtime evidence => HOLD / NEED MORE EVIDENCE.

## FROZEN TASK
Reuse the already frozen `KM-CORE-PAIR-01-TASK-SPEC-001` task without changing its semantic workload. The same input must be supplied to every candidate execution surface.

## REQUIRED EXECUTION CHAIN
DISCOVER → ADAPTER RESOLVE → CAPABILITY CONTRACT → REAL AUTH → FROZEN TASK → INDEPENDENT OUTPUTS → CANONICALIZATION → HASH → SEMANTIC COMPARISON → COMPATIBILITY MEASUREMENT → EVIDENCE → INDEPENDENT VERIFICATION.

## ACCEPTABLE SURFACES
1. Existing server-side `askMetaLogos` receiver with a real provider credential available only in server runtime.
2. Another independently executable server-side receiver implementing the frozen task and explicit capability contract.

A provider credential is not requested through source control, chat text, HTML, browser storage, or evidence artifacts.

## CURRENT BLOCKER
The observed `askMetaLogos` receiver reached real server-function logic, but its external xAI path was unavailable because `XAI_API_KEY` was absent. Therefore external inference was not executed and compatibility cannot be scored.

## RELEASE CONDITIONS
The gate may leave BLOCKED only when all are independently evidenced:
- real external or otherwise genuinely executable inference occurred;
- credential remained server-side;
- frozen task identity/hash matches;
- at least two controlled executions exist;
- outputs are captured without secret material;
- canonicalization algorithm/version is frozen;
- output hashes are reproducible;
- semantic comparison is explicit and deterministic;
- PrimeCore execution is not MOCK for the scored run;
- MetaLogos identity is established sufficiently for the claim being tested;
- authority remains NONE for the experimental compatibility layer;
- SOT remains unchanged;
- independent verifier reproduces the result;
- evidence package is sealed and provenance-complete.

## CURRENT DECISION
BLOCKED / NEED MORE EVIDENCE.
Do not promote Pair-01 compatibility until the release conditions are met.
