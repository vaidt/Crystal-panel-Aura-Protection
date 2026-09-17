# AURA ADR-001 SD-045 CLOSURE GATE v1.0

## 1. Gate Identity

- Stage: Stage 07 Authority Evidence / Re-entry
- Gate scope: SD-045 only
- Subject: ADR-001 identifier / subject collision
- Source repository: `Aura-IDToken/aura-specification`
- Examined ref: `main`
- Main HEAD: `71133de047c71e0bc1156d58c20396fe593ace70`
- Date: 2026-09-17
- Authority: NONE
- Normative effect: NONE
- Gate purpose: determine whether the reconstructed evidence establishes a supersession, acceptance, revocation, or other competent authority act sufficient to resolve SD-045.

## 2. Scope Boundary

This gate does not reopen Stage 06 or the other Stage 07 subjects. It evaluates only the evidence chain reconstructed for:

- A01 — `adrs/ADR-001_REPOSITORY_STRUCTURE.md`
- A02 — `adrs/ADR-001_DOCUMENT_MODEL.md`
- A03 — `docs/adr/001-document-model.md`

The gate does not select a preferred representation and does not create authority.

## 3. Evidence Basis

### A01 — Repository Structure

A01 was introduced by commit `b68181e48a65ed3a96007b5f3f89bad20a1caabf` on 2026-07-23. The repository-structure PR was PR #5, merged as `93f677fe34bf3f3fe0e8abffd6c8fdfd92b7958f`. PR #5 explicitly identifies ADR-001 as `adrs/ADR-001_REPOSITORY_STRUCTURE.md`. fileciteturn563file0L2-L16

The A01 artifact is presently represented as ACCEPTED, but no independent competent approval act is established by the evidence examined here.

### A02 — Document Model

A02 was introduced by `3c68a36bdb464b1a2f3edc81cab282b7850de02d`. The commit creates ADR-001 for the Document Model and records status PROPOSED. Its acceptance section requires Protocol Custodian approval, an `Accepted-by` line, and merge into the canonical branch. fileciteturn555file0L3-L7

No executed Protocol Custodian acceptance was established.

### A03 — Document Model duplicate

A03 was introduced and merged through PR #10 as commit `c4ba21506066f873ac574edb01ddba679feb4142`. PR #10 merged one changed file and identifies `docs/adr/001-document-model.md` as its subject. fileciteturn561file0L2-L16

The A03 artifact is DRAFT and its acceptance procedure requires an `accepted_by` entry before ACCEPTED. The retrieved PR discussion contains no comments. fileciteturn566file0L1-L6

## 4. Gate Criteria

| ID | Criterion | Result |
|---|---|---|
| SD045-G01 | A01 genealogy reconstructed | PASS |
| SD045-G02 | A02 genealogy reconstructed | PASS |
| SD045-G03 | A03 genealogy + PR/merge ancestry reconstructed | PASS |
| SD045-G04 | Explicit supersession act A01→A02 found | FAIL |
| SD045-G05 | Explicit supersession act A01→A03 found | FAIL |
| SD045-G06 | Explicit revocation of A01 found | FAIL |
| SD045-G07 | Protocol Custodian acceptance of A02 evidenced | FAIL |
| SD045-G08 | Protocol Custodian acceptance of A03 evidenced | FAIL |
| SD045-G09 | Authority act reassigning ADR-001 identifier found | FAIL |
| SD045-G10 | Evidence sufficient to resolve collision without inference | FAIL |
| SD045-G11 | SD-045 can be closed | FAIL |

## 5. Supersession Determination

No evidence establishes a supersession relation between A01 and A02 or A03.

A01 predates A02. A03 is later and derives from the A02 subject lineage, but chronology and ancestry do not constitute supersession.

No explicit supersession declaration or competent supersession act was identified.

**Result: SUPERSESSION UNPROVEN.**

## 6. Authority Determination

The evidence distinguishes repository state from competent authority action:

```text
A01: ACCEPTED repository state
     ≠ independently evidenced authority ratification

A02: PROPOSED
     + required Protocol Custodian acceptance absent

A03: DRAFT
     + required acceptance evidence absent
```

PR #5 and PR #10 establish repository merge events. They do not, by themselves, establish the missing competent approval acts required by the respective ADR procedures. PR #10's artifact explicitly defines the required acceptance mechanism. fileciteturn567file0L27-L38

**Result: AUTHORITY RESOLUTION NOT ESTABLISHED.**

## 7. Revocation Determination

No ADR-001-specific revocation act was found in the examined commit/PR evidence.

**Result: REVOCATION UNPROVEN.**

## 8. Closure Decision

### GATE RESULT: FAIL — SD-045 REMAINS OPEN

The evidence is sufficient to establish the existence, genealogy, and merge history of A01/A02/A03. It is **not** sufficient to establish a valid supersession, revocation, or competent acceptance path resolving the ADR-001 collision.

This is a forensic closure result, not a substantive architectural decision.

## 9. Exact State Transition

```text
BEFORE GATE
SD-045 = CONFLICTED / OPEN

        │
        ▼

RECONSTRUCTED EVIDENCE
A01 genealogy       PASS
A02 genealogy       PASS
A03 genealogy       PASS
PR/merge ancestry   PASS
Supersession        NOT ESTABLISHED
Acceptance          NOT ESTABLISHED
Revocation         NOT ESTABLISHED

        │
        ▼

AFTER GATE
SD-045 = CONFLICTED / OPEN
Gate = FAIL / CLOSURE BLOCKED
Stage 07 = OPEN
Stage 08 = NOT AUTHORIZED
```

## 10. No Reopening of Other Stages

This gate does not reopen:

- Stage 06 semantic classification;
- SD-001;
- SD-003;
- SD-032;
- other Stage 07 authority records;
- previously completed genealogy work.

It only records the closure result for SD-045.

## 11. Required Evidence for Any Future Re-entry

A future re-entry may proceed only if new evidence appears showing one or more of:

1. competent approval/acceptance of A01;
2. competent approval/acceptance of A02;
3. competent approval/acceptance of A03;
4. explicit supersession of one ADR-001 representation by another;
5. explicit revocation of an earlier ADR-001 act;
6. an authoritative identifier-allocation/reassignment act resolving the collision.

Absent such evidence, reopening the gate would repeat the same unresolved authority state.

## 12. Non-Resolution Boundary

This gate does not:

- choose A01/A02/A03;
- declare a winner;
- infer authority from merge chronology;
- rename ADR identifiers;
- edit governance/specification artifacts;
- authorize Stage 08.
