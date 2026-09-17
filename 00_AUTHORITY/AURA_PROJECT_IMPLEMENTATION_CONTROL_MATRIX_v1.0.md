# AURA PROJECT IMPLEMENTATION CONTROL MATRIX v1.0

**Purpose:** concrete project-level execution control derived from the AIC Registry.  
**Role:** operational control / traceability  
**Authority created here:** NONE  
**Protocol semantics created here:** NONE  
**Source of truth for governance:** authoritative governance records, not this matrix.

## 1. Project Inventory

| Project / repository | Function recorded | Current status | Authority boundary | Execution boundary |
|---|---|---|---|---|
| `Aura-IDToken/aura-specification` | normative protocol specification | CURRENT NORMATIVE SPECIFICATION | D-8 Protocol Authority | semantic changes require authorized governance |
| `vaidt/Aura-vNEXT` | current canonical implementation role | CURRENT IMPLEMENTATION | implementation ≠ protocol authority | M1–M8 gated |
| `vaidt/Aura-Guard` | Guard demonstration/current role | DEMONSTRATION | D-3; not successor to historical Guard | M4/M5 gated |
| `Aura-IDToken/aura-poc-a-core-v3.3` | historical PoCA/Core | HISTORICAL REFERENCE | provenance only | no current deployment authority |
| `Aura-IDToken/aura-guard-v1.3` | historical Guard | HISTORICAL REFERENCE | provenance only | no migration without authority |
| `Kamil1230xd/aura-sign-mvp` | historical signing MVP | HISTORICAL REFERENCE | D-11 does not promote | no migration/succession by inference |
| `AuraIDToken/Aura-Conformance-Kit` | conformance candidate | CANDIDATE | D-10 governs authority; repo allocation separate | M3 gated |
| `vaidt/Crystal-panel-Aura-Protection` | ecosystem control plane / forensic governance | ACTIVE CONTROL PLANE | not Protocol Authority | governs records and gates |

## 2. Required Project Record

Every implementation work item SHALL be represented as:

```text
PROJECT_RECORD
  ├─ record_id
  ├─ project/repository
  ├─ component
  ├─ responsibility
  ├─ non_responsibility
  ├─ target_ref
  ├─ base_commit
  ├─ target_artifact
  ├─ semantic_delta
  ├─ authority_source
  ├─ evidence_refs
  ├─ dependency_records
  ├─ conformance_requirements
  ├─ execution_gate
  ├─ approval_state
  ├─ mutation_state
  ├─ result_commit
  ├─ post_change_verification
  └─ rollback_reference
```

Missing load-bearing fields = `EXECUTION BLOCKED`.

## 3. Milestone Control

| Milestone | Control objective | Required evidence | Current registry treatment |
|---|---|---|---|
| M0 | baseline control | exact refs/tree/artifact inventory | controlled baseline |
| M1 | knowledge & governance lock | governance + canonicality + decision state | gate required |
| M2 | golden vector freeze | authoritative contract + vector provenance | gate required |
| M3 | conformance closure | authorized conformance contract + complete results | gate required |
| M4 | protocol release | authority + allocation + conformance + release evidence | gate required |
| M5 | production hardening | implementation/evidence/conformance/security evidence | gate required |
| M6 | operational readiness | operational controls and recovery evidence | gate required |
| M7 | load/failure validation | preserved failure/load evidence | gate required |
| M8 | production ready | all applicable prior gates closed | gate required |

The matrix does not mark a milestone PASS merely because implementation exists.

## 4. Action Classification

### READ

May proceed when repository/ref is known.

### FORENSIC RECONSTRUCTION

May proceed with evidence preservation and provenance tracking.

### TEST / VERIFICATION

Requires an applicable authorized contract and explicit test scope.

### PREPARE MUTATION

May prepare a proposed change record without executing the mutation.

### MUTATE

Requires all execution predicates in the AIC Registry to pass.

### MERGE

Requires explicit repository/branch authorization plus all applicable governance and conformance gates.

### RELEASE / DEPLOY

Requires M4–M8 applicable gates and explicit release authority.

## 5. Mandatory Pre-Mutation Gate

Before any code/specification mutation:

```text
1. Identify repository.
2. Identify exact ref.
3. Record base commit SHA.
4. Identify exact target files.
5. State semantic purpose.
6. Identify authority decision.
7. Identify evidence.
8. Identify required conformance.
9. Check dependencies.
10. Check conflicts.
11. Check milestone gate.
12. Record approval.
13. Execute mutation.
14. Record resulting commit/tree/blob.
15. Re-run verification.
16. Record rollback point.
```

## 6. Current Blocking Conditions

The control plane SHALL block implementation expansion whenever any applicable condition remains unresolved, including:

- DQ-003;
- DQ-004;
- BC-02 A;
- BC-02 B;
- Phase 3 P-001…P-012 decision-gated surfaces;
- incomplete specification-to-repository allocation under AG-007;
- unresolved authority collision;
- unresolved supersession/revocation/acceptance;
- missing authoritative conformance contract;
- missing provenance for a load-bearing artifact.

## 7. ADR-001 Collision Control Record

The AIC system must preserve the three distinct ADR-001 representations as separate records until competent authority resolves their relationship:

| Identity | Path | Recorded status | Control treatment |
|---|---|---|---|
| A01 | `adrs/ADR-001_REPOSITORY_STRUCTURE.md` | ACCEPTED declaration | preserve; acceptance authority not independently established |
| A02 | `adrs/ADR-001_DOCUMENT_MODEL.md` | PROPOSED | preserve; explicit acceptance required |
| A03 | `docs/adr/001-document-model.md` | DRAFT | preserve; acceptance mechanism conflicts with A02/A01 governance interpretation |

The forensic closure state remains:

```text
SD-045 = CONFLICTED / OPEN
```

No AIC record may convert this into canonical selection without a competent resolving act.

## 8. Evidence / Implementation Separation

```text
IMPLEMENTED
    ≠
EVIDENCED
    ≠
CONFORMANT
    ≠
AUTHORIZED
    ≠
RELEASED
```

The control plane must expose all five states independently.

## 9. Retention

For every executed or rejected implementation action retain:

- request record;
- authority reference;
- evidence references;
- exact base SHA;
- changed paths;
- semantic delta;
- test/conformance results;
- approval/authorization record;
- resulting SHA;
- rollback SHA;
- post-change verification;
- rejection/block reason where execution did not occur.

No failed attempt or anomaly is deleted merely because the action was not ultimately executed.

## 10. Operational Rule

The AIC Registry and this matrix provide **full traceability and execution gating**, not autonomous governance.

The system is considered under control only when an auditor can answer, for every mutation:

> **Who/what authorized it, what exact artifact changed, why it changed, what evidence supported it, what conformance was required, which gate was open, what commit resulted, and how the change can be rolled back.**
