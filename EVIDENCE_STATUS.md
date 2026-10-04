# LogOS Evidence Status

**Status date:** 2026-10-04  
**Classification:** experimental research architecture with Rust and Agda/Cubical formal-method surfaces; no whole-system formal-verification or production-security claim.

## Property separation

| Property | Required evidence | Current default interpretation |
| --- | --- | --- |
| Rust component builds | clean build transcript bound to commit and toolchain | not inferred from source presence |
| Rust behavior | tests/reproduction for exact component | claim-specific only |
| Agda theorem/type-check result | successful prover/type-check transcript, assumptions, dependency identity, and source identity | theorem/module-specific only |
| Runtime conformance to formal source | explicit refinement/model-to-code argument plus tests or proof | not established by formal source alone |
| Jones-polynomial/SPHINX behavior | implementation tests | algorithm behavior only |
| Authentication/security | threat model, construction review, cryptanalysis/security analysis, and implementation review | not established |
| WAVE/coherence metrics | defined metric plus validation against a target construct | project metric, not truth/physics/consciousness measure |
| Distributed reliability | fault model plus reproducible distributed tests | not established by architecture |
| Runtime proof metadata | verified producer, binding to source/proof artifact, and tamper/replay controls | design target unless demonstrated |

## Formal-method source actually present

The repository contains an Agda/Cubical layer under `agda/`. The aggregate entry point is `agda/src/Everything.agda`, and TriWeavon modules live under `agda/src/TriWeavon/`.

This status file does not claim that the current commit has been independently type-checked. A successful, commit-bound Agda transcript is still required before promoting a theorem/property from source presence to checked evidence.

## Known negative evidence

Checked-in build logs must be retained as evidence rather than overwritten by generalized success language. Observed failures include:

- a Cargo/NEAR SDK target-mode error directing contract builds to `cargo near build` or `wasm32-unknown-unknown`;
- an `audiopus_sys` CMake compatibility failure in one Windows build environment;
- a configured local `sccache.exe` executable that could not be found in another captured build attempt.

These failures do not prove that every component is broken. They do prove that a whole-repository successful-build claim is not currently supported by the checked-in logs alone.

## Promotion invariant

No conceptual, mathematical, formal, implementation, simulation, or runtime layer inherits another layer's evidence automatically. Every promoted statement must name the exact property and artifact that earned it.

```text
FORMAL_SOURCE != CHECKED_PROOF
CHECKED_PROOF != RUNTIME_CONFORMANCE
ARCHITECTURE != SECURITY
METRIC != TRUTH
LOCAL_BUILD != INDEPENDENT_REPRODUCTION
CAPABILITY != AUTHORITY
```
