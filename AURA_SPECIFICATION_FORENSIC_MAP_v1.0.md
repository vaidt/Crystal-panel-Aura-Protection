# AURA SPECIFICATION FORENSIC MAP v1.0

**Repository:** `Aura-IDToken/aura-specification`  
**Inspected branch:** `main`  
**Main tree SHA:** `71133de047c71e0bc1156d58c20396fe593ace70`  
**Target map repository:** `vaidt/Crystal-panel-Aura-Protection`  
**Date:** 2026-09-16  
**Status:** FORENSIC INVENTORY / NON-NORMATIVE MAP

---

## 1. Purpose

This document records the structural and normative map of the `Aura-IDToken/aura-specification` repository as observed from GitHub.

It is deliberately separated from protocol authority. The repository contains normative specifications, drafts, evidence, conformance material, reference implementations, governance artifacts, templates, historical material and working closure material.

**Repository contents are not automatically a single normative authority.**

---

## 2. Repository Identity

Verified repository:

`Aura-IDToken/aura-specification`

Default branch:

`main`

Observed default branch tree SHA:

`71133de047c71e0bc1156d58c20396fe593ace70`

The repository is public and currently exposes `main` as the default branch.

---

## 3. Primary Normative Graph

```text
AURA Constitution
        │
        ▼
APS-000 Foundation & Terminology
        │
        ▼
APS-001 Protocol Specification
        │
        ├──────────────┐
        ▼              ▼
APS-100            APS-200
Invariants         Canonical Data Model
        │              │
        └──────┬───────┘
               ▼
            APS-300
         Evidence Model
               │
               ▼
            APS-400
       Conformance Matrix
               │
               ▼
            APS-500
      Reference Fixtures
               │
               ▼
            APS-900
       Compliance Mapping
               │
               ▼
            APS-950
 Reference Implementation
        Requirements
```

This graph is the explicit hierarchy represented by the current specification corpus. APS-001 itself states the normative authority chain from Constitution through APS-950.

---

## 4. Specification Layer

### 4.1 Root / terminology

- `AURA Constitution_260723_190157.txt`
- `AURA Constitution_260723_190157.pdf`
- `AURA Protocol Specification APS-000 — Foundation &_260723_191759.txt`
- `AURA Protocol Specification APS-000 — Foundation &_260723_191759.pdf`
- `aps/APS-000_FOUNDATION_AND_TERMINOLOGY.md`
- `specification/APS-001_PROTOCOL_SPECIFICATION.md`

### 4.2 Normative APS modules

- `aps/APS-100_PROTOCOL_INVARIANTS.md`
- `aps/APS-200_CANONICAL_DATA_MODEL.md`
- `aps/APS-300_EVIDENCE_MODEL.md`
- `aps/APS-400_CONFORMANCE_TEST_MATRIX.md`
- `aps/APS-500_REFERENCE_FIXTURES.md`
- `aps/APS-900_COMPLIANCE_MAPPING.md`
- `aps/APS-950_REFERENCE_IMPLEMENTATION_REQUIREMENTS.md`
- `aps/EVENT_TYPE_REGISTRY.md`

### 4.3 Invariant registry

- `invariants/INVARIANT_REGISTRY.md`

This registry is the detailed definition source for the 15 invariant identifiers listed by APS-100.

---

## 5. Protocol Execution Graph

The current APS-001 draft defines the execution flow as:

```text
Evaluation Request
        ↓
Identity / Version Resolution
        ↓
Structural + Type Validation
        ↓
Policy Resolution
        ↓
Deterministic Evaluation
        ↓
Canonical Result
        ↓
Evidence Construction
        ↓
Canonical Serialization
        ↓
Integrity / Hash Domains
        ↓
Audit Record + Evidence Pack
```

Mandatory failures are intended to terminate in a fail-closed state.

---

## 6. Canonical Data Model Graph

APS-200 defines these entities:

```text
ENT-001 Protocol Header
        │
        ▼
ENT-002 Evaluation Request
        │
        ▼
ENT-003 Evaluation Result
        │
        ├──────────────► ENT-004 Policy Reference
        │
        ▼
ENT-005 Evidence
        │
        ▼
ENT-006 Attestation
        │
        ▼
ENT-007 Audit Record
        │
        ▼
ENT-008 Implementation Metadata
```

APS-200 currently binds the JSON interoperability profile to RFC 8785 JCS and defines the canonical UTF-8 byte boundary for the current profile.

---

## 7. Cryptographic Boundary

Current APS-001 / APS-200 material specifies the following current profile:

```text
canonical object
      ↓
RFC 8785 JCS
      ↓
canonical UTF-8 bytes
      │
      ├── SHA-256(bytes)
      │
      └── RFC 6962-style Merkle leaf
             SHA-256(0x00 || bytes)

Merkle interior node:
SHA-256(0x01 || left_digest || right_digest)
```

The repository also contains CK-003 decision/evidence material concerning hash domains and canonical serialization.

Important boundary:

> hexadecimal digest text is a representation, not the raw digest input.

---

## 8. Evidence Graph

```text
Protocol Requirement
        ↓
Invariant
        ↓
Execution
        ↓
Evidence Object
        ↓
Evidence Pack
        ↓
Conformance Test
        ↓
Release Evidence
```

APS-300 defines Core, Audit, Conformance, Release and Chain evidence classes.

APS-300 also defines `evidence_hash` separately from a Merkle leaf hash; the two domains must not be conflated.

---

## 9. Conformance Graph

```text
APS Requirement
      ↓
INV-xxx
      ↓
CONF-xxx
      ↓
FIX-xxx
      ↓
Evidence
      ↓
Reference Implementation
      ↓
Release
```

Current conformance catalogue:

- CONF-001 Deterministic Evaluation
- CONF-002 Replay Verification
- CONF-003 Canonical Serialization
- CONF-004 Evidence Integrity
- CONF-005 Traceability
- CONF-006 Platform Independence
- CONF-007 Fail Closed
- CONF-008 Version Compatibility
- CONF-009 Evidence Completeness
- CONF-010 Cryptographic Verification
- CONF-011 Zero Float Runtime
- CONF-012 Auditability
- CONF-013 Policy Determinism
- CONF-014 Reference Compatibility
- CONF-015 Canonical Identity

Assignment of an identifier is not itself a PASS result.

---

## 10. Fixture Layer

APS-500 defines reference fixtures as a mandatory basis of conformance validation.

Current repository fixture areas include:

```text
fixtures/
├── ck003/
├── core/
├── corpus/
└── schemas/
```

Observed concrete fixtures include:

- `fixtures/core/FIX-001_BASIC_EVALUATION.json`
- `fixtures/ck003/expected_digests.json`
- `fixtures/ck003/manifest.json`
- `fixtures/corpus/CANONICAL-001_jcs_evidence.json`
- `fixtures/corpus/FIX-INV-007_zero_float.json`
- `fixtures/corpus/FIX-INV-012_event_type.json`
- `fixtures/corpus/FIX-INV-013_policy_determinism.json`
- `fixtures/corpus/FIX-INV-014_aps500_compatibility.json`
- `fixtures/corpus/FIX-INV-015_canonical_identity.json`
- `fixtures/schemas/common-object-contract.schema.json`
- `fixtures/schemas/event_types.json`

APS-500 itself still contains TODO language concerning complete fixture finalization. Therefore presence of fixtures does not by itself establish that the entire normative fixture corpus is closed.

---

## 11. CK-003 Closure / Evidence Branch

`ck003/` is a substantial working evidence and closure area.

Major observed domains:

```text
ck003/
├── APS001_INV_MATRIX/
├── audit/
├── cross-language-002/
├── decisions/
├── dq-002-hash-domain/
├── dq-006-canonical-serialization/
├── dq-006-closure/
├── dq-006-final-closure-execution/
├── evidence/
├── gates/
├── handover-assessment/
└── legacy/
```

This is not simply documentation. It contains ADRs, defect records, cross-language vectors, fixtures, scripts, closure records, evidence packages, conformance gap matrices and handover assessments.

It should therefore be represented in Crystal Panel as an **Evidence / Closure Workstream**, not merged blindly into the normative specification layer.

---

## 12. Conformance Boundary Work

The repository contains a separate `conformance/boundary/` tree covering controlled boundary validation.

Observed material includes:

- boundary validation records;
- custodian closure records;
- chief architect approval/delegation records;
- common receipt schema;
- RI-RS receiver material;
- controlled P01 handoff records;
- Python and Rust execution evidence;
- receipts, manifests and logs;
- a small Rust receiver implementation.

This area is an **assurance/conformance execution layer**, not merely prose documentation.

---

## 13. Reference Implementation Layer

`reference/` contains:

- `reference/RI-PY_AURA_POC_A_CORE.md`
- `reference/RI-RS_AURA_GUARD.md`
- `reference/README.md`

APS-950 historically identifies:

```text
RI-PY → aura-poc-a-core → Python → deterministic measurement
RI-RS → aura-guard-v1.3 → Rust → audit middleware
```

However, the repository reconciliation work elsewhere in the AURA corpus explicitly treats the current lineage and canonicality of these implementations as a governance matter. The Crystal map therefore records these as **reference lineage**, not automatic current canonical implementation authority.

---

## 14. Governance Layer

Observed governance material includes:

- `GOVERNANCE.md`
- `constitution/AURA_CONSTITUTION.md`
- `constitution/README.md`
- `adrs/`
- `docs/adr/`
- `compliance/`
- `releases/`
- `VERSIONING.md`
- `CHANGELOG.md`
- GitHub issue / PR templates

The Constitution states:

```text
Constitution
   ↓
Protocol Specification
   ↓
Protocol Invariants
   ↓
ADR / ARR / RFC
   ↓
Development Playbook
   ↓
Repository Documentation
   ↓
Implementation
```

It also states that AI may analyze, propose, implement and support tests/documentation, but does not have authority to approve canonical changes.

---

## 15. Documentation / Process Layer

Observed process and control documents include:

- `README.md`
- `ROADMAP.md`
- `CONTRIBUTING.md`
- `CODE_OF_CONDUCT.md`
- `SECURITY.md`
- `STYLE_GUIDE.md`
- `AURA-DOCUMENTATION-NORMALIZATION-AUDIT-v1.md`
- `AURA-DOCUMENTATION-NORMALIZATION-CONTROL-REVIEW-v1.md`
- `docs/completion/00_MASTER_COMPLETION_PLAN.md`
- `docs/completion/01_CURRENT_STATE_MATRIX.md`

These documents explain process and status. They do not automatically define protocol semantics.

---

## 16. Templates / Extensibility Layer

Observed templates:

```text
templates/
├── ADR_TEMPLATE.md
├── APS_DOCUMENT_TEMPLATE.md
├── CONFORMANCE_REPORT_TEMPLATE.md
├── CONFORMANCE_TEST_TEMPLATE.md
├── FIXTURE_TEMPLATE.json
├── README.md
├── RFC_TEMPLATE.md
└── SPEC_TEMPLATE.md
```

Templates are process tooling, not protocol requirements.

---

## 17. Duplicate / Parallel Artifact Problem

The repository contains several parallel representations of core documents:

- PDF;
- TXT;
- normalized Markdown;
- older/newer specification directories;
- `constitution/` plus root Constitution artifacts;
- `adrs/` plus `docs/adr/`;
- evidence/closure copies.

This is not necessarily an error. It does create a **canonicality-resolution requirement**.

Crystal Panel MUST therefore map:

```text
artifact
→ role
→ authority status
→ source version
→ relationship
→ supersedes / derived-from
```

rather than simply listing filenames.

---

## 18. Critical Specification Findings From the Current Main Branch

### F-001 — APS-001 is still a draft

`APS-001_PROTOCOL_SPECIFICATION.md` declares `0.2-DRAFT` and `ARCHITECTURE REVIEW REQUIRED`.

Therefore the repository currently contains a root normative draft, not proof of an approved APS-001 v1.0.

### F-002 — APS-100 through APS-950 are also marked DRAFT

The principal APS modules carry draft status.

Therefore:

```text
document exists ≠ document approved
```

### F-003 — APS-200 has explicit TODOs

Examples include exact `execution_id` format, request field schema, decision vocabulary and attestation lifecycle/authority.

Therefore the canonical data model is materially developed but not fully closed.

### F-004 — APS-300 has an Evidence Pack TODO

The container format remains explicitly marked TODO.

Therefore Evidence Object semantics are further developed than the complete Evidence Pack container contract.

### F-005 — APS-500 still describes fixture finalization as TODO

The repository has fixtures, but APS-500 itself states that the canonical corpus depends on completion of the relevant schemas and Evidence Pack format.

### F-006 — APS-100 catalogue vs executable coverage requires verification

APS-100 lists 15 invariants, while the catalogue marks some rows without direct CONF identifiers in the table. APS-400 separately defines CONF-011 through CONF-015.

The final closure must verify one-to-one or explicitly justified many-to-one coverage rather than assuming it from naming.

### F-007 — SPEC-002 is explicitly non-normative while DRAFT

It defines a future contract surface for Constitution Artifact / Vector construction and explicitly forbids treating its candidate choices as approved decisions.

This is important: candidate numbers, byte order, rounding, embedding method and hash formulas in SPEC-002 cannot be promoted by implication.

### F-008 — CK-003 contains closure evidence, but evidence is not automatically approval

Closure records, cross-language evidence and fixtures materially strengthen reproducibility claims, but their normative authority still follows the governance status of the associated decisions/specification.

---

## 19. System Boundary for Crystal Panel

Crystal Panel SHOULD represent the specification repository using the following six domains:

```text
                    AURA SPECIFICATION
                           │
        ┌──────────────────┼──────────────────┐
        │                  │                  │
     NORMATIVE          ASSURANCE          GOVERNANCE
        │                  │                  │
   APS / INV          CONF / FIX /        Constitution /
   data model         EVID / CK003       ADR / RFC / status
        │                  │                  │
        └──────────────────┼──────────────────┘
                           │
                 REFERENCE IMPLEMENTATION
                           │
                    RI-PY / RI-RS
                           │
                     HISTORICAL
                           │
                superseded / legacy
```

---

## 20. Branch Handling Rule

The repository has numerous working branches. Branch names include closure, DQ, CK-003, cross-language, Claude and handover workstreams.

A branch MUST be treated as a separate versioned state, not as a new protocol authority.

For each branch the forensic process is:

```text
BRANCH NAME
    ↓
HEAD SHA
    ↓
TREE INVENTORY
    ↓
FILE-BY-FILE CONTENT
    ↓
DIFF FROM MAIN
    ↓
NORMATIVE IMPACT
    ↓
EVIDENCE IMPACT
    ↓
GOVERNANCE STATUS
```

No branch should be merged into the current canonical map merely because its name contains `closure`, `final`, `canonical`, `approval`, or similar terminology.

---

## 21. Forensic Reading Rule

For the requested deep audit, each file is classified by content rather than filename:

```text
NORMATIVE
GOVERNANCE
ARCHITECTURE
CONFORMANCE
EVIDENCE
IMPLEMENTATION
FIXTURE
PROCESS
TEMPLATE
HISTORICAL
EXPERIMENTAL
DUPLICATE / DERIVED
```

The classification must be supported by the actual file contents.

---

## 22. Current Conclusion

The `aura-specification` repository is not a single flat specification. It is a **specification ecosystem** containing a normative spine plus a large closure/evidence/conformance apparatus.

The most important current distinction is:

```text
                 WHAT MUST BE TRUE
                         │
                       APS
                         │
                         ▼
                 WHAT PROVES IT
                         │
                 CONF / FIX / EVID
                         │
                         ▼
                 WHO AUTHORIZES IT
                         │
                    GOVERNANCE
                         │
                         ▼
                 WHO IMPLEMENTS IT
                         │
                  RI / PRODUCT CODE
```

This is the structure Crystal Panel must preserve.

---

## 23. Mutation Policy

This map does not authorize modifications to `Aura-IDToken/aura-specification`.

Its purpose is to provide the Crystal Panel with a verified map and a controlled basis for subsequent branch-by-branch forensic analysis.
