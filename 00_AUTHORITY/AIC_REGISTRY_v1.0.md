# AIC REGISTRY v1.0 — AURA IMPLEMENTATION CONTROL REGISTRY

**Registry ID:** AURA-AIC-REGISTRY-001  
**Version:** 1.0  
**Created:** 2026-09-17  
**Repository:** `vaidt/Crystal-panel-Aura-Protection`  
**Control-plane role:** governance / traceability / implementation control  
**Authority created by this file:** NONE  
**Normative effect created by this file:** NONE  
**Mutation policy:** append-only records; corrections by superseding record, never silent rewrite

---

## 1. Purpose

This registry is the operational source of truth for **recording and controlling implementation state** across the AURA ecosystem.

It does not replace the authoritative governance instruments. It materializes their currently evidenced scope into explicit control records so that an implementation action can be answered with:

```text
WHAT
WHY
AUTHORITY
EVIDENCE
OWNER
REPOSITORY
REF
COMMIT
BLOB
DEPENDENCIES
CONFORMANCE
EXECUTION GATE
ALLOWED ACTION
FORBIDDEN ACTION
CURRENT STATE
NEXT AUTHORIZED ACTION
```

The registry therefore separates:

```text
PROTOCOL AUTHORITY
IMPLEMENTATION AUTHORITY
EVIDENCE AUTHORITY
CONFORMANCE AUTHORITY
IDENTITY / SIGNING AUTHORITY
EXECUTION AUTHORIZATION
```

These are not interchangeable.

---

## 2. Registry Invariant

```text
AIC REGISTRY RECORD
    ↓
MUST REFERENCE AUTHORITY OR EVIDENCE
    ↓
MUST HAVE PROVENANCE
    ↓
MUST HAVE CURRENT STATE
    ↓
MUST HAVE EXECUTION GATE
    ↓
MUST DEFINE ALLOWED / FORBIDDEN ACTIONS
```

And:

```text
EXISTS ≠ CURRENT ≠ APPROVED ≠ AUTHORIZED ≠ IMPLEMENTED ≠ CONFORMANT ≠ RELEASED
```

No implementation record may become normative merely because it is present in this registry.

---

## 3. Authority Baseline

The current governance corpus establishes the following authority domains:

| Domain | Authority | Current basis | Registry treatment |
|---|---|---|---|
| Protocol | AURA Human Governance Authority / Owner | D-8 | AUTHORITY ESTABLISHED |
| Evidence | AURA Human Governance Authority / Owner | D-9 / AG-004 | AUTHORITY ESTABLISHED |
| Conformance | AURA Human Governance Authority / Owner | D-10 / AG-005 | AUTHORITY ESTABLISHED |
| Identity | AURA Human Governance Authority / Owner | D-11 / AG-006 | AUTHORITY ESTABLISHED |
| Signing | AURA Human Governance Authority / Owner | D-11 / AG-006 | AUTHORITY ESTABLISHED |
| Implementation | `vaidt/Aura-vNEXT` current canonical implementation role | D-8-era governance baseline / AG-007 evidence | ROLE ESTABLISHED; scope must remain explicit |
| Guard | `vaidt/Aura-Guard` current demonstration role | D-3 / AG-003 | ROLE ESTABLISHED; not historical successor |
| Ecosystem control plane | `vaidt/Crystal-panel-Aura-Protection` | governance/context evidence | CONTROL-PLANE ROLE; not Protocol Authority |

### Critical authority rule

```text
Repository ≠ Authority
Implementation ≠ Protocol Definition
Evidence ≠ Governance Decision
Conformance Result ≠ Governance Decision
```

D-9 explicitly keeps Evidence Authority separate from evidence production, storage, repository ownership and independent verification. D-10 keeps Conformance Authority separate from conformance execution, tooling, repositories and independent verification. D-11 keeps Identity/Signing Authority separate from implementation, key material, KMS/HSM architecture and historical signing repositories.

---

## 4. AIC Core Records

The original AIC family is preserved as the top-level control domains:

### AIC-000 — Governance Control

**Purpose:** record the governance authority and execution boundary governing an AIC record.

**Required authority fields:**
- authority_source
- decision_id / governance_id
- decision_status
- effective_state
- scope
- non_scope
- ratification / acceptance evidence
- supersession / revocation state

**Current control state:** ACTIVE CONTROL DOMAIN.

**Hard rule:** AIC-000 records authority; it does not manufacture authority.

### AIC-001 — Repository / Artifact Identity

**Purpose:** identify the exact implementation or evidence object.

**Required identity tuple:**

```text
repository
ref
commit_sha
path
blob_sha
artifact_version
first_seen
last_verified
```

A branch name or filename alone is insufficient identity for load-bearing records.

### AIC-002 — Architecture / Responsibility Allocation

**Purpose:** map an authorized responsibility to a component and repository without allowing implementation to redefine the protocol.

**Required fields:**

```text
protocol_domain
component
responsibility
non_responsibility
canonical_repository
allocation_status
allocation_authority
allocation_evidence
```

Current AG-007 evidence establishes the authority needed to make allocation decisions but also records that complete component-to-repository allocation must be explicit rather than inferred from repository structure.

### AIC-003 — Evidence / Provenance

**Purpose:** preserve evidence identity and provenance.

**Required fields:**

```text
evidence_id
source_repository
source_ref
source_commit
source_path
source_blob
provenance_chain
evidence_class
integrity_state
retention_class
```

Evidence Authority is governed separately by D-9.

### AIC-004 — Release / Execution Control

**Purpose:** prevent implementation, merge, release or deployment from bypassing governance and conformance gates.

**Required fields:**

```text
release_id
subject
source_aic_records
required_authority
required_evidence
required_conformance
required_gate
approval_state
execution_state
release_state
rollback_reference
```

No release state may be inferred from a passing build alone.

---

## 5. Mandatory Record Schema

Every material implementation record SHALL contain:

| Field | Requirement |
|---|---|
| `record_id` | unique, immutable |
| `record_type` | AIC-000…AIC-004 or control subtype |
| `domain` | explicit |
| `subject` | explicit artifact/component |
| `status` | current state |
| `authority_status` | evidenced / claimed / absent / conflicted |
| `authority_source` | exact decision/instrument |
| `evidence_status` | current evidence state |
| `evidence_refs` | exact source refs |
| `repository` | exact repo |
| `ref` | branch/tag/commit ref |
| `commit_sha` | exact commit when applicable |
| `path` | exact path when applicable |
| `blob_sha` | exact blob when applicable |
| `semantic_status` | current/historical/target/etc. |
| `implementation_status` | implemented/not implemented/etc. |
| `conformance_status` | verified/not verified/blocked/etc. |
| `execution_gate` | M0–M8 / decision gate |
| `dependencies` | explicit IDs |
| `allowed_actions` | bounded |
| `forbidden_actions` | bounded |
| `owner` | responsible authority/role |
| `last_verified` | timestamp |
| `supersedes` | explicit only |
| `superseded_by` | explicit only |
| `revoked_by` | explicit only |
| `notes` | evidence-qualified notes |

---

## 6. Current Governance Records

### GOV-001 — Custodian Governance Model

**Source:** AURA Custodian Charter / Context Pack / governance corpus  
**State:** CONTROL MODEL  
**Authority:** none created by the registry  
**Control:** Existing Authority First  
**Forbidden:** self-authorization, inferred delegation, authority by recency, authority by implementation completeness.

### DEC-REG-v2 — Current Custodian Decision-State Register

**Source:** `CUSTODIAN-NORMATIVE-DECISION-REGISTER-v2`  
**State:** current decision-state register  
**Inherited ratified decisions:** D-2.1, D-2.2, D-2.3, D-2.4, D-2.5, D-5, D-7.1, D-7.2, D-7.3  
**D-1:** subsequently determined through the D-1 placement artifact  
**D-3:** controlled / ratified path  
**D-4:** open / no closure  
**D-6:** blocked  
**DQ-003:** open  
**DQ-004:** open / blocked.

### D-1 — APS-200 §8 Canonical Placement

**Current evidence state:** DETERMINED / ACCEPTED in the D-1 determination artifact.  
**Canonical anchor:** `Aura-IDToken/aura-specification` → APS-200 → consolidated §8.  
**Rule:** historical §8.1–§8.9 are not restored as current numbered anchors.

### D-3 / AG-003 — Guard Lineage

**Current state:** D-3 ratified/current governance path.  
**Historical:** `Aura-IDToken/aura-guard-v1.3` = reference/provenance.  
**Current:** `vaidt/Aura-Guard` = Emergent-generated demonstration implementation.  
**Not established:** successor, reimplementation, normative replacement, migration.

### D-8 — Protocol Authority

**Current authority:** AURA Human Governance Authority / Owner.  
**Boundary:** Protocol Authority is distinct from Implementation Authority.

### D-9 / AG-004 — Evidence Authority

**Current authority:** AURA Human Governance Authority / Owner.  
**Boundary:** Evidence Authority ≠ evidence production ≠ evidence storage ≠ repository ownership ≠ independent verification.

### D-10 / AG-005 — Conformance Authority

**Current authority:** AURA Human Governance Authority / Owner.  
**Boundary:** Conformance Authority ≠ conformance execution/tooling/repository/independent verification.

### D-11 / AG-006 — Identity and Signing Authority

**Current authority:** AURA Human Governance Authority / Owner.  
**Boundary:** does not designate a specific implementation, key material, certificate issuer, KMS/HSM, rotation scheme, or historical `aura-sign-mvp` successor.

---

## 7. Concrete Ecosystem Records

| Record | Subject | Repository | State | Authority | Implementation | Conformance | Execution |
|---|---|---|---|---|---|---|---|
| AIC-001-REPO-001 | Normative protocol specification | `Aura-IDToken/aura-specification` | CURRENT NORMATIVE SPECIFICATION | D-8 | N/A | governed by D-10 | M1/M2 gated |
| AIC-001-REPO-002 | Current canonical implementation | `vaidt/Aura-vNEXT` | CURRENT CANONICAL IMPLEMENTATION ROLE | D-8 separation | CURRENT | must satisfy authorized contract | M1–M8 gated |
| AIC-001-REPO-003 | Guard demonstration | `vaidt/Aura-Guard` | DEMONSTRATION / CURRENT GUARD ROLE | D-3 | CURRENT DEMONSTRATION | not automatically certified | M4/M5 gated |
| AIC-001-REPO-004 | Historical Core | `Aura-IDToken/aura-poc-a-core-v3.3` | HISTORICAL / REFERENCE | provenance only | HISTORICAL | reference only | no current deployment authority |
| AIC-001-REPO-005 | Historical Guard | `Aura-IDToken/aura-guard-v1.3` | HISTORICAL / REFERENCE | provenance only | HISTORICAL | reference only | no current deployment authority |
| AIC-001-REPO-006 | Historical signing MVP | `Kamil1230xd/aura-sign-mvp` | HISTORICAL / REFERENCE | D-11 explicitly excludes promotion | HISTORICAL | reference only | no migration authorized |
| AIC-001-REPO-007 | Conformance candidate | `AuraIDToken/Aura-Conformance-Kit` | CONFORMANCE CANDIDATE | D-10 authority, repository allocation separate | CANDIDATE | decision-gated | M3 gated |
| AIC-001-REPO-008 | Ecosystem control plane | `vaidt/Crystal-panel-Aura-Protection` | CONTROL PLANE | governance mapping role | no protocol authority | evidence/governance support | controls execution records |

---

## 8. Implementation Control State

The registry SHALL treat the implementation lifecycle as:

```text
M0 BASELINE CONTROL
  ↓
M1 KNOWLEDGE & GOVERNANCE LOCK
  ↓
M2 GOLDEN VECTOR FREEZE
  ↓
M3 CONFORMANCE CLOSURE
  ↓
M4 PROTOCOL RELEASE
  ↓
M5 PRODUCTION HARDENING
  ↓
M6 OPERATIONAL READINESS
  ↓
M7 LOAD & FAILURE VALIDATION
  ↓
M8 PRODUCTION READY
```

The registry does **not** grant any milestone. Each milestone is a gate evaluated against its own authority/evidence criteria.

Current governance baseline continues to require revalidation before treating M1–M5 as executable. Open dependencies include DQ-003, DQ-004, BC-02 A/B, Phase 3 decision-gated surfaces and any remaining allocation/authority questions.

---

## 9. Execution Gate Logic

An implementation action is **EXECUTION-ELIGIBLE** only when all applicable predicates are true:

```text
AUTHORITY EXISTS
AND
AUTHORITY SCOPE COVERS ACTION
AND
ARTIFACT IDENTITY IS EXACT
AND
DEPENDENCIES ARE CLOSED OR EXPLICITLY WAIVED BY AUTHORITY
AND
REQUIRED EVIDENCE EXISTS
AND
REQUIRED CONFORMANCE IS SATISFIED
AND
CURRENT GATE IS OPEN
AND
NO HIGHER-PRIORITY CONFLICT EXISTS
```

Otherwise:

```text
BLOCK
    ↓
RECORD REASON
    ↓
RECORD REQUIRED AUTHORITY / EVIDENCE
    ↓
DO NOT MUTATE SOURCE
```

---

## 10. Forbidden Implementation Shortcuts

The AIC registry must reject:

```text
README claim → authority
repository owner → protocol authority
CODEOWNER → governance authority
merge → ratification unless the governing instrument explicitly defines it
CI PASS → conformance authority
implementation completeness → canonicality
newer commit → supersession
branch name → canonical status
file name → identity
historical recovery → restoration authorization
successful demo → production authorization
```

---

## 11. Change / Mutation Control

For every proposed implementation mutation, create or update a control record containing:

1. target repository;
2. target ref;
3. target commit base;
4. exact files;
5. semantic reason;
6. authority source;
7. evidence source;
8. required conformance tests;
9. required review/approval;
10. rollback reference;
11. execution gate;
12. resulting commit SHA;
13. resulting tree/blob identities;
14. post-change verification.

No mutation may be justified solely by a registry entry.

---

## 12. Conflict Handling

If two records conflict:

```text
DO NOT OVERWRITE
DO NOT PICK THE NEWER ONE
DO NOT PICK THE MORE COMPLETE ONE
DO NOT PICK THE MORE CONVENIENT ONE
```

Instead:

```text
CREATE CONFLICT RECORD
    ↓
PRESERVE BOTH PROVENANCES
    ↓
IDENTIFY AUTHORITY SOURCE
    ↓
CHECK RATIFICATION / SUPERSESSION / REVOCATION
    ↓
ESCALATE IF UNRESOLVED
```

This is particularly mandatory for ADR-001 identity/subject collision and any specification-to-repository allocation conflict.

---

## 13. Minimum Control Views

The control plane should be able to render at least:

### A. Authority View

```text
Domain → Authority → Decision → Scope → Evidence → Effective State
```

### B. Implementation View

```text
Component → Repository → Ref → Commit → Artifact → Implementation State
```

### C. Conformance View

```text
Requirement → Control → Fixture/Vector → Implementation → Result → Evidence
```

### D. Execution View

```text
Action → Preconditions → Dependencies → Gate → Approval → Commit → Verification
```

### E. Provenance View

```text
Artifact → First appearance → Branch → Commit → Blob → Derivative → Current status
```

### F. Conflict View

```text
Conflict → Competing records → Authority → Evidence → Resolution status
```

---

## 14. Current Hard Blocks to Implementation Expansion

The registry must currently surface, rather than hide:

- DQ-003;
- DQ-004;
- BC-02 Decision A;
- BC-02 Decision B;
- Phase 3 P-001…P-012 decision-gated surfaces;
- any incomplete component-to-repository allocation under AG-007;
- any unresolved acceptance/supersession/revocation question;
- any conformance requirement lacking authoritative contract status.

A control registry is successful only if it makes a blocked action impossible to mistake for an authorized action.

---

## 15. Retention / Audit Rule

Load-bearing records are retained while they are needed to reconstruct:

```text
AUTHORITY
PROVENANCE
SEMANTIC STATE
IMPLEMENTATION STATE
CONFORMANCE STATE
EXECUTION HISTORY
```

Corrections are additive. Historical records are never silently deleted or rewritten to make the current state appear cleaner.

---

## 16. Registry Integrity Statement

This registry is a **control-plane artifact**.

It does not:

- establish Protocol Authority;
- establish Implementation Authority;
- ratify a decision;
- supersede a governance instrument;
- authorize M1–M8 by declaration;
- replace the Decision Register;
- replace the Governance Resolution Matrix;
- replace the Governance Closure artifact;
- define protocol semantics;
- select a repository merely because it is technically complete.

Its job is stricter:

> **Every implementation action must be traceable to an existing authority, an exact artifact identity, explicit evidence, applicable conformance, and an open execution gate.**

---

## 17. Status

```text
REGISTRY: ACTIVE CONTROL-PLANE BASELINE
AUTHORITY CREATED BY REGISTRY: NONE
NORMATIVE EFFECT CREATED BY REGISTRY: NONE
IMPLEMENTATION AUTHORIZATION CREATED BY REGISTRY: NONE
TRACEABILITY: REQUIRED
PROVENANCE: REQUIRED
EXECUTION GATING: REQUIRED
```
