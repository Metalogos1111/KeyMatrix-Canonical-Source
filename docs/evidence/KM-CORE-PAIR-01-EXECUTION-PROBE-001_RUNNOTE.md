# KM-CORE-PAIR-01-EXECUTION-PROBE-001

## OBSERVED EXECUTION NOTE

Concrete local artifacts were executed in a controlled read-only probe.

### PrimeCore surface
- Source: `Интерфейс LLM-Адаптера для PrimeCore`
- SHA-256: `e2322a9d31d75f9af240b47aea7feebc730115d3637e99248212882c85d943ef`
- Adapter: `MockLocalAdapter`
- Backend: `Mock/CPU`
- Initialization: returned `true`
- Output SHA-256: `e5b0a2454f542d65dbcc5cfd0886016a2a17f2e387ce73d2ce145442706712f6`

### MetaCore12 surface
- Source: `MetaCore12 Backend Server`
- SHA-256: `0e996e091f83849b2f8891fa30e856f448ce072b9ba181dda9b8c475f05a4efc`
- Exact FastAPI application loaded locally with the secret accessor returning no secret.
- `GET /` returned HTTP 200.
- `GET /api/status` returned HTTP 200.
- Read-only observed state: coherence_gate `0.99`, rsn_balance `15420.5`, usdc_balance `0.0`.

### Repeatability / integrity
- PrimeCore output hash matched on repeat.
- MetaCore12 read-only status matched on repeat.
- OmniState SHA-256 before and after: `045f856b2b853d04004c34b8faba34b89734c5ec2f29854623d2826463e0e2eb`.
- No state mutation observed.

### Boundary
The composition endpoint `/api/transmute` was NOT invoked because the artifact mutates state and can return simulated output when no Gemini credential exists. Therefore this execution is evidence of concrete surface execution and repeatability, NOT evidence of PrimeCore × MetaCore compatibility.

Status: `OBSERVED / COMPATIBILITY_NOT_SCORED`
Authority: `NONE`
SOT: `UNCHANGED`
