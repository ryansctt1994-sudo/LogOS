# LogOS Evidence Status

Status date: 2026-09-04

Classification: experimental research architecture with code and formal-methods surfaces; no whole-system formal-verification or production-security claim.

## Property separation

| Property | Required evidence | Current default interpretation |
|---|---|---|
| Rust component builds | clean build transcript bound to commit/toolchain | not inferred from source presence |
| Rust behavior | tests/reproduction for exact component | claim-specific only |
| Formal theorem | checked prover transcript, assumptions and source identity | theorem-specific only |
| Runtime conformance to proof | explicit refinement/model-to-code argument plus tests/proof | not established by theorem alone |
| Jones-polynomial/SPHINX behavior | implementation tests | algorithm behavior only |
| Authentication/security | threat model, construction, cryptanalysis/security analysis, implementation review | not established |
| WAVE/coherence metrics | defined metric + validation against a target construct | project metric, not truth measure |
| Distributed reliability | fault model + reproducible distributed tests | not established by architecture |

## Known negative evidence

The repository contains a captured build failure in which Cargo could not execute a configured local `sccache.exe`. This is environment-specific negative evidence and must be retained rather than overwritten by a generalized “builds successfully” statement.

## Promotion invariant

No conceptual, mathematical, formal, implementation, simulation, or runtime layer inherits another layer's evidence automatically. Every promoted statement must name the exact property and artifact that earned it.
