# AURA AUTHORITY ACT PACKAGE — SD-045 / Q1

**Document ID:** AUTH-ACT-PKG-SD045-001  
**Version:** 1.0  
**Classification:** GOVERNANCE / EXECUTION PREPARATION  
**Status:** DRAFT — NON-BINDING / NOT EXECUTED  
**Authority exercised by this package:** NONE  
**Normative effect:** NONE  
**Execution authority:** Competent human governance authority only  
**Control repository:** `vaidt/Crystal-panel-Aura-Protection`

---

## 1. Purpose

This package defines the exact material governance act required before the next authority gate can be executed.

It is an execution surface, not an authority source. Preparation, recording, indexing, and verification by an agent do not constitute approval, delegation, ratification, supersession, revocation, reassignment, or any other competent authority act.

The immediate material act identified by the current evidence is:

> **Chief Architect → Protocol Custodian: bounded delegation for `DESIGNATION OF Q1 DECISION SURFACE`.**

The existing Scope Bridge expressly states that it is only a proposed bridge instrument and becomes binding only through the competent governance act/approval required by the existing hierarchy. fileciteturn708file0L2-L6

---

## 2. Critical distinction: Q1 delegation vs SD-045 resolution

This package deliberately separates two governance questions.

### A. Q1 jurisdictional act

The prepared instrument establishes a possible bounded delegation:

```text
CHIEF ARCHITECT
      ↓
PROTOCOL CUSTODIAN
      ↓
DESIGNATION OF Q1 DECISION SURFACE
```

Permitted downstream dispositions are exactly:

- Package #1
- Package #2
- Neither

The bridge does **not** itself select a package or resolve substantive questions.

### B. SD-045 collision resolution

The ADR-001 collision remains a separate load-bearing governance problem.

Execution of the Q1 Scope Bridge **must not be treated as sufficient to close SD-045** unless the competent authority act explicitly contains an effect that satisfies the SD-045 closure criteria.

In particular, the Q1 delegation does not automatically establish:

- which ADR-001 representation is canonical;
- that A01 supersedes A02/A03;
- that A02 supersedes A01/A03;
- that A03 supersedes A01/A02;
- revocation of any representation;
- identifier reassignment;
- reconciliation of conflicting acceptance rules.

No such effect may be inferred from the existence, merge, chronology, or selection of the Q1 bridge.

---

## 3. Primary execution instrument

**Source repository:** `Aura-IDToken/aura-specification`  
**Instrument path:**

`conformance/boundary/BC-02-Q1-CHIEF-ARCHITECT-CUSTODIAN-SCOPE-BRIDGE.md`

**Current source identity:**

- branch/ref: `main`
- blob SHA: `c2df3807a96b02befa7896fe27524d664ddf6641`
- current status in the instrument: `DRAFT — AUTHORITY INSTRUMENT PREPARATION`
- authority exercised by current instrument: `NONE`

The instrument itself defines the delegation as one decision class only: `DESIGNATION OF Q1 DECISION SURFACE`. fileciteturn708file0L2-L6

**Important:** The exact source artifact identity must be recaptured at execution time. A branch-local copy, stale SHA, filename, or historical reference is not sufficient.

---

## 4. Competent authority required

### Delegating authority

> **Chief Architect**

The act must be executed by the person/entity that is competent to exercise the Chief Architect authority under the governing hierarchy actually in force.

The agent must not fill in the person's name from inference.

### Receiving authority

> **Protocol Custodian**

The receiving authority must be identifiable as the competent Protocol Custodian at execution time.

The agent must not infer appointment, identity, or acceptance from repository activity alone.

---

## 5. Exact scope of delegation

The delegated decision class is exactly:

> **DESIGNATION OF Q1 DECISION SURFACE**

The delegation permits only the later designation of one of the closed outcomes:

1. `PACKAGE #1` — `conformance/boundary/BC-02.1-CUSTODIAN-DECISION-PACKAGE-A-B.md`
2. `PACKAGE #2` — `conformance/boundary/BC-02-CUSTODIAN-DECISION-PACKAGE-A-B-v1.md`
3. `NEITHER`

If Package #1 or Package #2 is later designated, the subsequent Selection Act must identify its exact path, commit, blob, SHA-256, Q1 identifier, delegated-authority reference, Custodian identity, date, and required approval/signature record.

---

## 6. Explicit exclusions — authority leakage firewall

The executing authority act must state, or otherwise unambiguously preserve, that the delegation does **not**:

- select Package #1 or Package #2;
- resolve Decision A;
- resolve Decision B;
- resolve C-1;
- resolve C-2;
- define or interpret ARI semantics;
- authorize implementation;
- establish or determine conformance;
- authorize fixture creation/modification or validation execution;
- amend, replace, supersede, freeze, or otherwise modify a normative protocol requirement;
- convert the selected Q1 surface into normative authority;
- create authority for artifacts referenced by the selected package;
- convert historical or engineering evidence into normative authority.

These exclusions reproduce the boundary already established by the Scope Bridge. fileciteturn708file0L2-L6

---

## 7. Required execution fields

The competent authority must provide actual values for all applicable fields.

| Field | Required value/evidence | Agent may prefill? |
|---|---|---|
| Delegating Authority | Competent Chief Architect identity + role | No — identity must be supplied/verified |
| Receiving Authority | Protocol Custodian identity + role | No — identity must be supplied/verified |
| Delegated Decision Class | `DESIGNATION OF Q1 DECISION SURFACE` | Yes, from instrument |
| Permitted Outcomes | Package #1 / Package #2 / Neither | Yes, from instrument |
| Effective Date | Actual effective date/time | No |
| Chief Architect identity/role | Actual identity and competence basis | No |
| Approval / Signature | Actual approval/signature record | No |
| Custodian acknowledgement | Actual acknowledgement, if required | No |
| Status | `APPROVED` or `NOT APPROVED` | No |
| Act identifier | Unique authority-act identifier | No, unless assigned by competent process |
| Scope reference | Exact Scope Bridge identity | Yes, subject to execution-time verification |
| Evidence location | Exact repo/path/commit/blob | Agent captures after act |

No placeholder may be interpreted as an executed value.

---

## 8. Minimum validity predicate

The Q1 delegation shall be treated as **EFFECTIVE** only if all applicable conditions are evidenced:

```text
COMPETENT_DELEGATOR
∧ IDENTIFIABLE_DELEGATE
∧ EXPLICIT_SCOPE
∧ EXPLICIT_DECISION_CLASS
∧ CLOSED_OUTCOME_SET
∧ EFFECTIVE_DATE
∧ ACTUAL_APPROVAL
∧ REQUIRED_ACKNOWLEDGEMENT
∧ PROVENANCE_CAPTURE
```

If any mandatory element is absent, the agent shall record the result as `NOT ESTABLISHED` rather than infer validity.

---

## 9. What constitutes the actual authority act

The following are **not**, by themselves, the authority act:

- creation of this package;
- creation of a branch;
- opening or merging a PR;
- a commit authored by an agent;
- repository presence of the Scope Bridge;
- a comment saying that approval is intended;
- chronology;
- a declaration by an AI assistant;
- selection of a package by an unqualified actor;
- a test result;
- a forensic conclusion.

The actual act must be attributable to the competent authority and contain the approval/delegation decision in a governance-recognizable form.

---

## 10. Material-act boundary for the agent

### Agent MAY

- prepare this package;
- prepare a clean execution copy of the Scope Bridge;
- identify exact evidence requirements;
- recover and verify provenance;
- check whether an existing authority act already exists;
- record observations and unresolved conflicts;
- capture the executed act after it exists;
- replay the authority criteria mechanically;
- prepare the subsequent SD-045 / Stage 07 gate input.

### Agent MUST NOT

- invent a signer;
- sign on behalf of the Chief Architect;
- fabricate Custodian acknowledgement;
- mark the bridge `APPROVED` without competent evidence;
- choose Package #1/#2/Neither without effective delegated authority;
- declare A01/A02/A03 canonical;
- infer supersession or revocation;
- infer identifier reassignment;
- resolve SD-045 by chronology or repository topology;
- authorize Stage 08.

---

## 11. Optional separate SD-045 resolution act

If the competent authority is asked to resolve SD-045 directly, that is a **separate material authority act** unless the existing governance instrument explicitly provides otherwise.

A direct SD-045 resolution act would need to identify, without ambiguity, the treatment of:

- A01 `adrs/ADR-001_REPOSITORY_STRUCTURE.md`;
- A02 `adrs/ADR-001_DOCUMENT_MODEL.md`;
- A03 `docs/adr/001-document-model.md`;

and explicitly state the relevant relationship, such as:

- supersession;
- revocation;
- identifier reassignment;
- acceptance/ratification;
- reconciliation of conflicting acceptance mechanisms;
- or another competent disposition already permitted by the governing model.

The package does **not** choose which disposition should be adopted. It specifies what must be explicit if such an act is executed.

---

## 12. Execution procedure

```text
PREPARED PACKAGE
      ↓
COMPETENT AUTHORITY REVIEW
      ↓
ACTUAL AUTHORITY ACT
      ↓
CAPTURE EXACT ARTIFACT
      ↓
CAPTURE COMMIT / BLOB / HASH / PR / REVIEW EVIDENCE
      ↓
PROVENANCE REPLAY
      ↓
AUTHORITY / SCOPE REPLAY
      ↓
A01 / A02 / A03 COLLISION REPLAY
      ↓
SD-045 GATE
      ↓
STAGE 07 AUTHORITY CLOSURE GATE
```

No later gate may be back-propagated to make the preceding act valid.

---

## 13. Execution-time provenance record

Immediately after an actual act, capture:

```text
ACT_ID:
ACT_TYPE:
DELEGATING_AUTHORITY:
DELEGATING_ROLE:
RECEIVING_AUTHORITY:
RECEIVING_ROLE:
DECISION_CLASS:
PERMITTED_OUTCOMES:
EFFECTIVE_DATE:
APPROVAL_RECORD:
ACKNOWLEDGEMENT_RECORD:
SOURCE_REPOSITORY:
SOURCE_REF:
SOURCE_COMMIT:
SOURCE_PATH:
SOURCE_BLOB:
SOURCE_SHA256:
PR_NUMBER:
REVIEW_RECORD:
EXECUTION_COMMIT:
EXECUTION_BLOB:
```

Unknown values remain `UNKNOWN`; they must not be replaced by inference.

---

## 14. Post-act decision matrix

| Condition after replay | Result |
|---|---|
| Valid delegation evidenced; no SD-045 effect | Q1 jurisdiction may become established; SD-045 remains open |
| Valid delegation + explicit SD-045 resolution | Re-run SD-045 closure criteria |
| Approval absent/invalid | Delegation not established |
| Scope ambiguous | Delegation not established |
| Signer competence unverified | Delegation not established |
| Evidence only shows repository merge | Repository event only; authority not established |
| Act claims supersession but does not identify object/relationship | Supersession unresolved |
| Act resolves acceptance-rule collision explicitly | Candidate evidence for SD-045 criterion G11; still requires replay |

---

## 15. Current state before execution

```text
Authority Act Package             PREPARED / NON-BINDING
Q1 Scope Bridge                   DRAFT / NON-BINDING
Q1 Delegation                    NOT ESTABLISHED
Q1 Selection                     NONE
A01/A02/A03 canonical selection  NONE
SD-045                           CONFLICTED / OPEN
Stage 07                         BLOCKED / OPEN
Stage 08                         NOT AUTHORIZED
Authority created by agent       NONE
Normative effect                 NONE
```

---

## 16. Closure condition for this package

This package itself is never the authority act.

It is complete when it provides a mechanically checkable execution surface and prevents authority leakage.

The next material state transition occurs only when an actual competent authority act is recorded.

```text
PREPARATION
   ≠
AUTHORITY ACT
   ≠
AUTHORITY REPLAY
   ≠
STAGE 07 CLOSURE
```

---

## 17. Final instruction to the execution operator

Do not modify the source Scope Bridge to insert a fictional name, signature, approval date, or acknowledgement.

Do not convert this package into an approval record.

Obtain or recover the actual competent authority act first. Then freeze the exact evidence identity and perform the replay mechanically.

**Required next sequence:**

> **Authority Act → Provenance Capture → Authority Replay → A01/A02/A03 Collision Replay → SD-045 Gate → Stage 07.**

**Package authority:** NONE.  
**Package normative effect:** NONE.  
**Package status:** READY FOR COMPETENT AUTHORITY EXECUTION.