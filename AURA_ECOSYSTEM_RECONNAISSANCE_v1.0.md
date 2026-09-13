# AURA Ecosystem Reconnaissance v1.0

**Status:** WORKING AUDIT BASELINE  
**Date:** 2026-09-13  
**Scope:** Crystal Panel + currently verifiable AURA repositories and supplied historical evidence  
**Execution mode:** READ-ONLY  
**Mutation authorization:** NONE

## 1. Purpose

Crystal Panel is being established as the map and coordination layer for AURA.

This first document records only what can currently be verified. It does not decide the final architecture, does not transfer code, and does not authorize implementation.

> **HISTORY ≠ CURRENT ≠ TARGET**

## 2. Crystal Panel — current state

Repository: `vaidt/Crystal-panel-Aura-Protection`

Verified:
- public repository
- default branch: `main`
- current HEAD: `43d50a22c3f7aadd0e53a1d90196bb1b55e8c712`
- current tree contains exactly one file: `README.md`
- README currently contains only the repository title

Therefore Crystal Panel is currently an **empty documentation/control-plane shell**, not yet an operational AURA map.

## 3. Current AURA repositories verified

| Repository | Observed role | State |
|---|---|---|
| `vaidt/Aura-vNEXT` | New canonical implementation and product direction | CURRENT / ACTIVE |
| `vaidt/Aura-Guard` | Guard candidate under reconciliation | CURRENT / RECONCILIATION |
| `AuraIDToken/Aura-Conformance-Kit` | Conformance tooling/materials | CURRENT / EARLY STRUCTURE |
| `AuraIDToken/Aura-Conformance-Kits` | Older duplicate conformance repository | HISTORY / ARCHIVED |

This is an accessible/verifiable inventory, not proof of every repository ever existing under every AURA account.

## 4. Aura-vNEXT — verified current picture

Current default branch: `claude/aura-vnext-genesis-xerti8`.

The current README states:
- M0 canonical evidence domain is implemented and gated.
- The product loop runs end to end.
- The repository describes itself as the new canonical implementation of Aura.
- It is not a fork, mirror, migration, or Git merge of the frozen Aura-IDToken repositories.
- M0 covers canonical evidence representation, audit-chain binding, portable Evidence Package, and an independent three-state verifier.
- No compatibility claim is made with the frozen corpus because that corpus is not reachable from the environment.
- Genesis established repository boundary, provenance policy, transfer register, module acceptance criteria, ADRs and a CI baseline.
- No implementation modules have been transferred from the frozen corpus.
- The intended non-authorizing direction is Evidence-First Runtime Governance for AI Agents.

Visible repository domains include:
`architecture/`, `governance/`, `provenance/`, `conformance/`, `core/`, `runtime/`, `policy/`, `audit/`, `evidence/`, `integrations/`, `packs/`, `cli/`, `tests/`, `tools/`, `docs/`.

## 5. Aura-vNEXT — declared governed chain

```text
CONTEXT
   ↓
DECISION
   ↓
ACTION
   ↓
OUTPUT
   ↓
AUDIT
   ↓
EVIDENCE
   ↓
VERIFICATION
```

The declared objective is to establish not merely whether an action was allowed, but whether the resulting execution can be reconstructed, verified and supported by evidence for a third party.

## 6. Aura-Guard — verified current picture

Repository: `vaidt/Aura-Guard`

Verified current HEAD:
`7d2f5746ae61a66edcd11d75bff0787bed854363`

Current repository visibly contains:
- backend Python service and tests
- CLI material
- signing configuration
- extensive `docs/`
- `.emergent/` operational material
- current GitHub workflow material

The current README is only a placeholder title. Therefore the repository itself does not currently provide a reliable high-level product description.

**Conclusion:** do not infer the final Guard role from directory layout alone.

## 7. Historical Aura-Guard reference

The supplied historical `aura-guard-v1.3` corpus documents deterministic audit middleware covering:
- deterministic decision processing
- append-only hash-chained audit records
- Merkle batching
- optional RFC 3161 timestamping
- signed policies
- replay
- fail-closed behavior
- API authentication and operational controls

Assessment:

**LEGACY / REFERENCE IMPLEMENTATION — HIGH VALUE**

Historical code is provenance/evidence. It is not automatically the current canonical implementation and is not approved for transfer by this audit.

## 8. Historical architecture evidence

Supplied System Restore material records an earlier target model:

```text
Mathematical Core
      ↓
Evidence Model
      ↓
Decision Engine
      ↓
Attestation Engine
      ↓
Cryptographic Core
      ↓
Operational Core
```

It also records:
- Aura as a protocol rather than a single application.
- determinism as fundamental.
- Mathematical Core measures rather than makes business decisions.
- signed policies.
- implementation conformance to the protocol.
- specification before implementation.

These statements are treated as **HISTORY** until reconciled against current canonical direction.

## 9. Conformance

`AuraIDToken/Aura-Conformance-Kit` is public and non-archived.

Its README describes a set of tools/materials for verifying implementation conformity with Aura requirements and says the current stage focuses on project structure and documentation before implementation.

This establishes a visible conformance responsibility, but not yet a final repository contract.

## 10. First reconciliation observations

### Confirmed
1. Aura is still treated as a system/protocol/ecosystem rather than one application.
2. Determinism remains central.
3. Evidence, provenance, auditability and verification remain central.
4. AURA has an explicit canonical/current direction in `Aura-vNEXT`.
5. Historical repositories remain valuable provenance sources.
6. Conformance remains a distinct concern.

### Unverified / unresolved
1. Exact canonical responsibility of `vaidt/Aura-Guard`.
2. Final boundary between Aura-vNEXT, Guard, Sign, Conformance and future Runtime.
3. Which historical protocol artifacts remain normative.
4. Final specification-to-repository allocation.
5. Whether all previously discussed repositories are currently accessible.
6. Final component/module graph.

## 11. Crystal Panel operating model

```text
                AURA CRYSTAL PANEL
                       │
        ┌──────────────┼──────────────┐
        ↓              ↓              ↓
     HISTORY        CURRENT         TARGET
        │              │              │
        └──────────────┼──────────────┘
                       ↓
                 RECONCILIATION
                       ↓
                VERIFIED SYSTEM MAP
```

For important claims:

```text
CLAIM
  ↓
SOURCE
  ↓
REPOSITORY / DOCUMENT
  ↓
COMMIT / VERSION
  ↓
IMPLEMENTATION
  ↓
TEST
  ↓
EVIDENCE
```

## 12. Next controlled step

1. Complete repository-level reconnaissance.
2. Perform the Vision Preservation Check.
3. Reconcile historical versus current repositories.
4. Identify unresolved conflicts and gaps.
5. Construct the Current System Map only after that.
6. Construct the Target System Map afterwards.

**No implementation changes are authorized by this document.**
