# KM-CORE-EXECUTION-SURFACE-DISCOVERY-001

Status: READY / BLOCKED FOR REAL MULTI-CORE EXECUTION
Authority: NONE
SOT mutation: NO

## Purpose
Resolve the first concrete executable surface for the compatibility benchmark using existing KeyMatrix artifacts. No synthetic runtime results are permitted.

## Evidence observed
- PrimeCore has a concrete `LLMAdapter` interface and `MockLocalAdapter` implementation. This is an executable adapter artifact, but the recorded surface is mock/local and does not establish real model inference.
- MetaCore12 backend artifacts contain a concrete FastAPI service surface with `/`, `/api/status`, `/api/transmute`, and `/api/burn_rsn` endpoints. The artifact also contains a Gemini integration seam, but successful external inference is not established; the code explicitly falls back to simulation when the API key is absent.
- The historical/provenance ledger identifies MetaCore as an architectural role but explicitly records runtime as UNVERIFIED and warns that MetaCore12 must not automatically be treated as MetaCore.
- The preflight benchmark records all 21 pair relationships as NOT_EXECUTED and states that the correct action is to establish bounded executable adapters/runtimes before running matched baselines and compositions.

## Candidate Pair-01
Proposed investigation target: `PrimeCore × MetaCore12-backend-surface`.

Classification: CANDIDATE EXECUTION SURFACE ONLY.
It is NOT classified as `PrimeCore × MetaCore` because the available evidence does not establish that MetaCore12 is the MetaCore core implementation.

## Required controlled execution
1. Freeze source hashes for both surfaces.
2. Define a bounded task that exercises an explicit interface between the two surfaces.
3. Run PrimeCore alone, the second surface alone where independently executable, and the composed path under matched conditions.
4. Capture raw outputs, timestamps, run identifiers, environment metadata, and artifact hashes.
5. Reproduce the result independently.
6. Only then derive compatibility/synergy metrics.

## Hard blockers
- PrimeCore non-mock runtime is not established by the current adapter artifact.
- MetaCore12 identity as MetaCore is not established.
- Successful external Gemini inference is not established.
- Therefore no genuine `PrimeCore × MetaCore` compatibility score may be emitted from this corpus alone.

## Decision
Do not fabricate Pair-01. Preserve the benchmark surface as BLOCKED and continue executable-surface acquisition. A concrete non-mock second surface or an explicitly bounded local execution adapter is required before the first compatibility datapoint can be VERIFIED.

## Status boundaries
LIVE: NOT ESTABLISHED
DEPLOYED: NOT ESTABLISHED
VERIFIED: NOT ESTABLISHED for multi-core compatibility
PROVEN: NOT ESTABLISHED
