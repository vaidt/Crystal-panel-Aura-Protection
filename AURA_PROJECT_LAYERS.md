# AURA PROJECT — FULL LAYER MODEL

## Purpose

This document defines the repository directory topology for the AURA project. It is a **structural control plane**, not a redesign of the protocol and not a declaration of normative authority.

The directories separate evidence, specification, governance, implementation, conformance, operations, and forensic reconstruction so that artifacts cannot silently acquire authority merely by being colocated.

## Layer 0 — Authority & Constitution

`00_AUTHORITY/`

- Constitution
- authority records
- ownership / custodian records
- ratifications and approvals
- authority reconciliation
- canonicality determinations

## Layer 1 — Foundation & Terminology

`01_FOUNDATION/`

- APS-000
- terminology
- definitions
- protocol scope
- foundational concepts

## Layer 2 — Protocol Invariants

`02_INVARIANTS/`

- APS-100
- invariant registry
- invariant dependency records
- normative invariant evidence

## Layer 3 — Canonical Data Model

`03_DATA_MODEL/`

- APS-200
- entities
- schemas
- canonical object contracts
- serialization
- canonical byte rules
- hash-domain definitions
- event registry

## Layer 4 — Evidence Model

`04_EVIDENCE/`

- APS-300
- evidence objects
- evidence lifecycle
- evidence hashes
- evidence chains
- provenance
- evidence packs

## Layer 5 — Conformance

`05_CONFORMANCE/`

- APS-400
- CONF-001…
- conformance requirements
- test definitions
- certification rules
- cross-implementation conformance

## Layer 6 — Reference Fixtures

`06_FIXTURES/`

- APS-500
- golden vectors
- canonical fixtures
- negative fixtures
- immutable fixture records
- fixture provenance

## Layer 7 — Compliance & Traceability

`07_COMPLIANCE/`

- APS-900
- regulatory mapping
- traceability matrices
- Constitution → APS → INV → ENT → Evidence → CONF → FIX → RI → Release chains

## Layer 8 — Reference Implementations

`08_REFERENCE_IMPLEMENTATIONS/`

- APS-950
- RI-PY
- RI-RS
- implementation requirements
- implementation evidence
- replay evidence

## Layer 9 — Cryptography & Verification

`09_CRYPTO_VERIFICATION/`

- canonical hashing
- Merkle rules
- signatures / attestations
- verification profiles
- verification vectors
- cryptographic boundary records

## Layer 10 — Governance & Decisions

`10_GOVERNANCE/`

- ADRs
- DQ records
- decision matrices
- closure records
- custodian decisions
- governance status
- unresolved authority questions

## Layer 11 — Architecture & System Maps

`11_ARCHITECTURE/`

- architecture maps
- dependency maps
- protocol graphs
- data-flow maps
- assurance boundaries
- repository/system boundaries

## Layer 12 — Repository & Integration

`12_INTEGRATION/`

- repository relationships
- integration records
- branch integration status
- cross-repository mappings
- release integration

## Layer 13 — Operations & Release

`13_OPERATIONS/`

- release controls
- versioning
- operational procedures
- audit reports
- security procedures
- deployment/readiness records

## Layer 14 — Forensic Reconstruction

`14_FORENSICS/`

- file genealogy
- branch genealogy
- commit genealogy
- PR reconstruction
- semantic delta matrices
- evidence provenance
- historical snapshots
- supersession / conflict analysis

## Layer 15 — Historical Archive

`15_HISTORICAL/`

- historical artifacts
- superseded drafts
- reverted artifacts
- legacy specifications
- historical implementation snapshots

Historical artifacts must remain immutable records of what existed. Moving an artifact here does not by itself establish that it is superseded; that status requires evidence.

## Layer 16 — Templates & Controls

`16_TEMPLATES_CONTROLS/`

- RFC templates
- issue templates
- PR templates
- specification-gap templates
- document templates
- control checklists

## Layer 17 — External Evidence

`17_EXTERNAL_EVIDENCE/`

- externally supplied evidence
- audit evidence
- regulatory source material
- independent verification records

## Layer 18 — Reports

`18_REPORTS/`

- forensic reports
- architecture reports
- governance reports
- conformance reports
- repository state reports
- release reports

## Layer 19 — Controlled Working Area

`19_WORKSPACE/`

- temporary analysis
- generated intermediate data
- reconciliation workspaces
- non-authoritative working artifacts

Nothing in this directory is normative merely because it is present.

## Global authority rule

Directory placement is **not authority**.

Authority must be established from:

1. document status;
2. governance record;
3. explicit approval/ratification;
4. provenance;
5. versioning;
6. repository history;
7. applicable dependency/authority chain.

## Forensic rule

The repository structure must preserve the distinction between:

```text
WHAT EXISTED
    ↓
WHEN IT EXISTED
    ↓
WHERE IT EXISTED
    ↓
WHO AUTHORED / COMMITTED IT
    ↓
WHAT IT CHANGED
    ↓
WHAT AUTHORITY IT CLAIMED
    ↓
WHAT AUTHORITY IT ACTUALLY HAD
```

## Current reconstruction boundary

This structure is intended to host the complete reconstruction of:

`Aura-IDToken/aura-specification`

from PR #1 (`[WIP] Add complete documentation for APS and Constitution`) through PR #43 (`Revert "docs(dq-003): specification reconciliation control record"`), including all surviving branches and relevant historical snapshots.

No protocol semantics are changed by this directory model.
