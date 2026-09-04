# Reson8 — LogOS Cognitive Lattice

LogOS is an experimental cognitive-lattice and distributed-systems research project combining Rust services, formal-methods experiments, topological abstractions, multi-agent coordination concepts, and visualization/runtime tooling.

## Evidence status

This repository should **not** be described as a fully formally verified distributed operating system, a proven security system, or a machine-checked realization of its entire topological narrative.

The repository contains implementation artifacts, formalization-related material, and build/test logs. Those are claim-specific evidence surfaces. A formal model can establish properties of the model that was actually checked; it does not automatically prove the Rust runtime, network interfaces, deployment configuration, authentication system, or broader conceptual interpretation.

Likewise, a mathematical invariant used as an experimental gate does not become a cryptographic authentication primitive merely because it is mathematically interesting. Security properties require a threat model and security analysis appropriate to the mechanism.

See `EVIDENCE_STATUS.md` for the promotion boundary.

## Research architecture

The project explores a lattice in which heterogeneous reasoning strands exchange state through shared interfaces while local and global invariants are represented explicitly. Major conceptual surfaces include:

- Rust crates/services for orchestration and runtime behavior;
- a Styx/9P-style shared-state interface;
- WAVE/coherence metrics;
- topological and homotopy-inspired representations;
- SPHINX/Jones-polynomial experiments;
- Lean/Agda or related formal-methods artifacts where present;
- interactive dashboards and application integrations.

Terms such as `TriWeavon`, `Homotopic Unitarity`, `Viviani Peak`, and `WAVE coherence` are project-specific constructs unless a document explicitly maps them to a standard mathematical object and proves the claimed relationship. Project-defined thresholds such as `0.85`, `0.9998`, or equations such as `α + ω = 15` are configuration/design constraints unless separately justified as empirical or mathematical laws.

## Multi-agent strand model

Historical project material describes multiple AI/model strands with weighted roles and shared state. These weights are orchestration choices, not evidence that one model has intrinsically greater reasoning authority. Model identity, platform, and assigned weight must not be treated as a proof of competence, truth, or authorization.

## Formal-methods boundary

Formal verification claims must identify:

1. the exact theorem/property;
2. the exact formal source file and commit;
3. the prover and version;
4. all axioms, assumptions, admitted lemmas, trusted code and external dependencies;
5. a clean machine-check transcript;
6. the mapping from the formal model to the executable implementation, if implementation behavior is being claimed.

Without that chain, use terms such as `formal model`, `formalization experiment`, or `proof-oriented artifact`, not `formally verified system`.

## Security boundary

The SPHINX/Jones-polynomial work is treated here as an experimental authorization/gating design. It is not a substitute for established authentication or cryptographic authorization mechanisms unless a concrete construction, threat model, security proof/analysis, key-management design, implementation audit, and independent review establish the required properties.

For real deployments, standard authentication, authorization, transport security, secret management, and audit controls remain required.

## Runtime and build status

The repository contains Rust workspace material and captured build/check output. A historical build log records at least one environment failure caused by a missing local `sccache.exe`; therefore the presence of source and build scripts must not be summarized as a clean universal build result.

Use a fresh environment and preserve exact commands, toolchain versions, dependency lock state, raw stdout/stderr, and commit identity for any new build claim.

Typical development flow, subject to the actual workspace state:

```bash
cargo build --workspace
cargo test --workspace
```

Do not report those commands as passing until they have been executed successfully on the exact commit being cited.

## Suggested evidence ladder

- **E0** — concept or untested claim
- **E1** — architecture/specification/formal statement exists
- **E2** — exact implementation or formal artifact checked locally with a retained result
- **E3** — fresh-environment same-team reproduction with artifact and identity binding
- **E4-A** — independent reproduction
- **E4-B** — governance/constitutional review where applicable
- **E4-C** — adversarial assessment
- **E5+** — operational/external validation appropriate to the claim

Evidence does not transfer automatically between formal proofs, runtime code, security mechanisms, dashboards, simulations, or conceptual interpretations.

## Core rule

```text
interesting mathematics != verified runtime
formal model != whole-system proof
invariant gate != cryptographic authentication
coherence score != truth
architecture != authority
```

## Provenance and license

This repository contains material attributed in the historical project documentation to Matthew Ruhnau. Preserve original authorship, license notices, and third-party provenance. A writable mirror or downstream branch does not alter original authorship or automatically grant broader rights.
