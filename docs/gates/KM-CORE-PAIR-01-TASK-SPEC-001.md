# KM-CORE-PAIR-01-TASK-SPEC-001

Status: FROZEN TASK SPEC / EXECUTION BLOCKED
Authority: NONE
SOT mutation: NO

## Objective
Prepare the first controlled compatibility experiment without assigning runtime identity to an artifact that has not been proven to be the named Core.

## Candidate
- Surface A: PrimeCore concrete adapter surface (`LLMAdapter` / `MockLocalAdapter`).
- Surface B: MetaCore12 FastAPI backend surface.
- Named pair under evaluation: `PrimeCore × MetaCore12-backend-surface`.
- IMPORTANT: this is not evidence for `PrimeCore × MetaCore` until MetaCore identity is independently established.

## Controlled task
Given a fixed, non-secret task payload, Surface A produces a bounded deterministic computation/verification artifact. Surface B accepts only a read-only compatibility probe or task-description payload and returns an observable response without changing authority or financial state. The composition harness must record interface success/failure, schema conformity, latency, errors, and hashes.

## Required runs
1. A-alone baseline.
2. B-alone baseline, if B is executable in the controlled environment.
3. A→B composed invocation.
4. Independent reproduction of the composed invocation.

## Required evidence
- frozen task hash
- source artifact hashes
- environment/runtime versions
- run IDs and timestamps
- raw output hashes
- schema validation
- error/deny behavior
- side-effect check
- independent reproduction record

## Forbidden
- synthetic score
- treating mock inference as real model inference
- treating MetaCore12 as MetaCore without identity evidence
- authority creation
- financial mutation
- SOT mutation
- client secret exposure
- promotion to VERIFIED without independent reproduction

## Acceptance
A compatibility datapoint can be scored only if the execution is observable, the task is frozen, the surfaces are executable, and the result is independently reproducible. Otherwise status remains BLOCKED / NEED MORE EVIDENCE.
