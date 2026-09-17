# AURA — STAGE 07 RE-ENTRY REQUIREMENTS v1.0

**Artifact:** `Aura Protection/EVIDENCE/STAGE_07_REENTRY_REQUIREMENTS_v1.0.md`

**Date:** 2026-09-17  
**Source corpus:** `Aura-IDToken/aura-specification`  
**Forensic repository:** `vaidt/Crystal-panel-Aura-Protection`  
**Related gate:** `STAGE_07_AUTHORITY_CLOSURE_GATE_v1.0.md`  
**Authority:** NONE  
**Normative effect:** NONE  
**Status:** EVIDENCE / RE-ENTRY CONTROL ONLY

---

## 1. Purpose

This artifact defines the minimum evidence delta required before Stage 07 may be re-entered after the current result:

`FAIL — CLOSURE BLOCKED`

It does not resolve SD-045, choose a canonical ADR-001 representation, create authority, amend the source specification repository, or authorize Stage 08.

The purpose is to prevent repetition of the completed provenance replay when the missing input is a **new competent governance act**.

---

## 2. Current Locked State

The immediately preceding Stage 07 gate establishes:

```text
Part 6R provenance replay       COMPLETE
E1–E15 evidence boundary       PASS
A01/A02/A03 genealogy          PASS
Supersession                   UNPROVEN
Revocation                     UNPROVEN
A02 acceptance                 NOT ESTABLISHED
A03 acceptance                 NOT ESTABLISHED
Identifier reassignment        NOT ESTABLISHED
Acceptance-rule reconciliation NOT ESTABLISHED

SD-045                         CONFLICTED / OPEN
Stage 07                       OPEN
Stage 07 Closure               BLOCKED
Stage 08                       NOT AUTHORIZED
```

This state is not changed by this document.

---

## 3. Re-entry Principle

A Stage 07 re-entry package must contain a **new evidence delta** relative to Part 6R / E1–E15.

Re-running E1–E15 without additional evidence is insufficient for closure because the previous replay already established provenance and genealogy while failing to locate the competent act required for authority reconciliation.

Therefore:

```text
SAME EVIDENCE
    → NO NEW AUTHORITY INPUT
    → NO BASIS FOR DIFFERENT GATE RESULT
```

---

## 4. Accepted Evidence Classes for Re-entry

The following classes are relevant to the unresolved SD-045 closure condition. They are listed as evidence requirements, not as decisions about which outcome should occur.

| ID | Evidence class | What must be evidenced | Closure relevance |
|---|---|---|---|
| RE-01 | Acceptance / approval act | Competent authority act accepting A01, A02, or A03 | Resolves lifecycle acceptance status if authority and scope are proven |
| RE-02 | Explicit supersession act | An act explicitly superseding one ADR-001 representation with another | Establishes lifecycle transition if competent authority is proven |
| RE-03 | Explicit revocation act | An act explicitly revoking an earlier ADR-001 representation/decision | Establishes loss of prior authority if competent authority is proven |
| RE-04 | Identifier reassignment | Authoritative allocation/reassignment of ADR-001 to one subject | Resolves identifier collision if competent authority and scope are proven |
| RE-05 | Acceptance-rule reconciliation | Competent act resolving the conflict between generic merge-acceptance and specific Custodian acceptance requirements | Resolves the governing acceptance path for this collision |

Multiple classes may be required if a single act does not resolve the complete collision.

---

## 5. Mandatory Provenance Fields

Any proposed re-entry evidence must be recorded with enough provenance to replay the act without inference:

1. source repository;
2. exact path or object identifier;
3. branch/ref;
4. commit SHA;
5. blob SHA where applicable;
6. author/actor identity as recorded by the source;
7. event timestamp;
8. exact act type;
9. competent authority claimed by the source;
10. scope of authority;
11. object(s) governed by the act;
12. relationship to A01/A02/A03;
13. whether the act is approval, acceptance, supersession, revocation, reassignment, or reconciliation;
14. whether the act is itself ratified/accepted under the applicable governance mechanism;
15. any contradictory evidence located in the same authoritative source path.

Missing provenance fields must remain explicitly `UNKNOWN` rather than being reconstructed by assumption.

---

## 6. Mechanical Re-entry Procedure

A future re-entry should execute in this order:

```text
NEW EVIDENCE IDENTIFIED
        ↓
PROVENANCE CAPTURE
        ↓
ACT TYPE CLASSIFICATION
        ↓
COMPETENT AUTHORITY CHECK
        ↓
SCOPE CHECK
        ↓
A01/A02/A03 RELATION CHECK
        ↓
ACCEPTANCE / SUPERSESSION / REVOCATION / REASSIGNMENT REPLAY
        ↓
CONFLICT CHECK
        ↓
SD-045 CLOSURE GATE
```

No architectural redesign is part of this procedure.

---

## 7. Negative Controls

The following must **not** be treated as sufficient new authority evidence by themselves:

- a newer timestamp;
- later commit chronology;
- branch creation;
- branch ancestry;
- authorship alone;
- file naming;
- directory location;
- `Status: ACCEPTED` without an evidenced competent act where such act is required;
- a merge considered in isolation when the applicable acceptance mechanism is unresolved;
- a PR existing without the competent approval/acceptance evidence required by the governing rule;
- a later document merely claiming that an earlier document was superseded;
- an AI-generated or forensic artifact asserting resolution;
- repetition of E1–E15 without a new competent act.

These controls preserve the evidence boundary established by Part 6R.

---

## 8. Re-entry Package Minimum

Before a future Stage 07 gate is executed, the evidence package should contain:

### Required
- a new evidence record for each claimed governance act;
- exact source identity and provenance;
- the affected A01/A02/A03 representation(s);
- explicit authority scope;
- mechanical replay of the act;
- contradiction/conflict check;
- a statement of what remains unresolved, if anything.

### Optional but useful
- linked PR/issue evidence;
- review/approval records;
- signed commits or signed governance records;
- release or ratification records;
- cross-repository corroboration.

Optional evidence does not become authoritative merely because it is present.

---

## 9. Re-entry Outcomes

The next gate may mechanically produce any result supported by the new evidence. This artifact does not preselect an outcome.

Permitted state transitions must be derived from the evidenced act and its competent authority. In particular, the re-entry process must not assume that the existence of new evidence necessarily means closure will succeed.

If the evidence remains insufficient or contradictory:

`SD-045 = CONFLICTED / OPEN`

and Stage 07 remains blocked.

---

## 10. Stage 08 Boundary

No Stage 07 re-entry artifact, evidence package, or provenance record authorizes Stage 08.

Stage 08 remains:

`NOT AUTHORIZED`

until a separate gate establishes the required authority and closure conditions under the applicable governance baseline.

---

## 11. Relationship to Existing Evidence

This artifact is derived from, and subordinate to, the forensic state recorded in:

- `Aura Protection/EVIDENCE/PART_6R_PROVENANCE_REPLAY_v1.0.md`
- `Aura Protection/EVIDENCE/STAGE_07_AUTHORITY_CLOSURE_GATE_v1.0.md`
- `Aura Protection/EVIDENCE/MANIFEST.json`
- E1–E15 identified by the manifest.

It does not modify or replace those evidence records.

---

## 12. Final Control Statement

```text
Current Stage 07 result     = FAIL — CLOSURE BLOCKED
SD-045                      = CONFLICTED / OPEN
New evidence required       = YES
Repeat Part 6R alone        = INSUFFICIENT
Authority created here      = NONE
Normative effect             = NONE
Stage 08                    = NOT AUTHORIZED
```

**This artifact is a re-entry control, not a governance act.**
