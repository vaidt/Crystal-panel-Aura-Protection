# AURA ADR-001 SUPERSESSION / AUTHORITY PATH RECONSTRUCTION v1.0

## 1. Record Identity

- Stage: Stage 07 Authority Evidence / Re-entry
- Source repository: `Aura-IDToken/aura-specification`
- Examined ref: `main`
- Main HEAD: `71133de047c71e0bc1156d58c20396fe593ace70`
- Date: 2026-09-17
- Authority: NONE
- Normative effect: NONE
- Disposition: FORENSIC / EVIDENCE ONLY

## 2. Scope

This record is deliberately limited to the three concrete ADR-001 representations:

- A01 — `adrs/ADR-001_REPOSITORY_STRUCTURE.md`
- A02 — `adrs/ADR-001_DOCUMENT_MODEL.md`
- A03 — `docs/adr/001-document-model.md`

The reconstruction checks only genealogy, PR/merge ancestry, and evidence for approval / acceptance / supersession / revocation. It does not choose a canonical ADR-001 or modify repository semantics.

## 3. A01 — Repository Structure

- Subject: Canonical Repository Structure
- Introducing commit: `b68181e48a65ed3a96007b5f3f89bad20a1caabf`
- Commit date: 2026-07-23T21:03:00Z
- Current blob: `3df6315b5b9883753d29668870bdace611e37f23`
- Current status: ACCEPTED
- PR path: PR #5
- PR #5 base: `main` at `7a22522350a0e917fa773d724854796778623147`
- PR #5 head: `176f7abb3659ff34855d5693d89317b5dfe14290`
- PR #5 merge commit: `93f677fe34bf3f3fe0e8abffd6c8fdfd92b7958f`
- PR #5 merged: 2026-07-23T21:06:21Z
- PR body explicitly identifies `ADR-001` as `adrs/ADR-001_REPOSITORY_STRUCTURE.md`.
- No independent approval/review act beyond the repository merge record was established in this pass.

The ADR itself declares `Status: ACCEPTED` and states `Supersedes: —` and `Superseded By: —`. The content records the repository restructuring decision. fileciteturn549file0L2-L4

PR #5 is evidenced as merged, with the cited ADR path in its body and merge commit `93f677...`. fileciteturn563file0L2-L16

## 4. A02 — Document Model

- Subject: Document Model — ARC → SPEC → APS
- Introducing commit: `3c68a36bdb464b1a2f3edc81cab282b7850de02d`
- Commit date: 2026-08-02T21:10:34+02:00
- Current blob: `66083e286a2fc33e70ccab4d1df6015ec0be65fd`
- Current status: PROPOSED
- Introducing commit message: `adr: add ADR-001 Document Model: ARC -> SPEC -> APS`
- Introducing commit has no PR associated in the examined GitHub commit-to-PR lookup.
- The ADR explicitly requires Protocol Custodian approval, an `Accepted-by` line, and merge into the canonical branch.
- No such acceptance evidence is present in the current artifact.

The introducing commit creates A02 as PROPOSED and explicitly states the required acceptance mechanism. fileciteturn555file0L3-L7

The current artifact retains PROPOSED status and the Protocol Custodian acceptance requirement. fileciteturn550file0L2-L2

## 5. A03 — Document Model Duplicate

- Subject: Document Model — ARC → SPEC → APS
- Introducing commit: `c4ba21506066f873ac574edb01ddba679feb4142`
- Commit date: 2026-08-02T21:31:16+02:00
- Current blob: `340ed584082baf5353ce0496034484ab6379ac45`
- Current status: DRAFT
- Introducing commit message: `adr: add ADR-001 to docs/adr/001-document-model.md on branch docs/adr-001-document-model (#10)`
- PR: #10
- PR head: `b5a0c8c0b58e3cf738832763aca138ea7b9c4d7b`
- PR base SHA: `3c68a36bdb464b1a2f3edc81cab282b7850de02d`
- PR merge commit: `c4ba21506066f873ac574edb01ddba679feb4142`
- PR #10 merged: 2026-08-02T19:31:16Z
- Changed files: 1
- PR comments/review comments: empty in the retrieved timeline.
- The artifact explicitly requires Protocol Custodian approval and an `accepted_by` entry before ACCEPTED.

The commit establishes A03 directly as the Document Model representation and its patch contains status DRAFT. fileciteturn556file0L3-L10

PR #10 confirms the one-file merge and merge commit. fileciteturn561file0L2-L16
The retrieved PR discussion contains no comments. fileciteturn566file0L1-L6

## 6. Genealogy

```text
A01 Repository Structure
  b68181e48a65...
        │
        └── repository/main lineage

A02 Document Model
  3c68a36bdb46...
        │
        ▼
A03 Document Model duplicate
  c4ba21506066...
        │
        └── main lineage
```

A02 is introduced after A01. A03 is a later direct-child representation in the A02 lineage. The available evidence does not establish that either A02 or A03 supersedes A01.

## 7. Supersession Search

Searches were performed for ADR-001-related commit history and supersession terminology.

- ADR-001 commit search returned A01, A02 and A03 as the relevant concrete creation events, followed by later forensic/governance records.
- A commit search for `supersed` returned no matching commits.
- No explicit `Supersedes` / `Superseded By` relation was found connecting A01 to A02 or A03.
- A01 itself explicitly declares no supersession relation. fileciteturn549file0L2-L4
- A02/A03 do not contain an executed supersession act against A01; A02's scope explicitly says it does not supersede existing protocol specifications unless explicitly referenced and superseded by a subsequent ADR. fileciteturn550file0L2-L2

Disposition: **SUPERSESSION UNPROVEN**.

## 8. Approval / Acceptance / Revocation Search

### A01

Evidence establishes:
- repository artifact status = ACCEPTED;
- PR #5 merged;
- PR #5 explicitly identifies A01 as ADR-001.

This is repository-state evidence. Independent competent approval by a named authority was not established in this pass.

### A02

Evidence establishes:
- status = PROPOSED;
- Protocol Custodian is Decision Owner;
- explicit acceptance mechanism requires `Accepted-by` and merge.

No executed acceptance was found. The introducing commit has no associated PR in the examined commit-to-PR endpoint. fileciteturn564file0L1-L12

### A03

Evidence establishes:
- status = DRAFT;
- PR #10 merged;
- PR discussion retrieved no comments;
- acceptance procedure requires `accepted_by` plus merge.

Merge occurred, but the artifact remained DRAFT and no acceptance act by Protocol Custodian was evidenced. Therefore merge alone cannot be treated as executed acceptance for A03 without resolving the repository's conflicting governance mechanisms.

### Revocation

No ADR-001-specific revocation act was found in the examined commit/PR searches.

## 9. Authority Path Determination

| Subject | Repository event | Authority event | Result |
|---|---|---|---|
| A01 Repository Structure | PR #5 merged; artifact ACCEPTED | No independent named approval act established | ACCEPTED repository state; independent ratification NOT ESTABLISHED |
| A02 Document Model | Direct commit; remains PROPOSED | Required Protocol Custodian acceptance absent | NOT ACCEPTED |
| A03 Document Model duplicate | PR #10 merged; artifact remains DRAFT | Required Protocol Custodian acceptance absent | NOT ACCEPTED |

## 10. Load-Bearing Finding

The conflict is not resolved by merge chronology.

A01 predates A02 and is the repository's first concrete use of ADR-001, with PR #5 explicitly tying the identifier to Repository Structure. A02 subsequently reuses the same identifier for a different architectural subject. A03 duplicates A02's subject under the same identifier and is merged, but remains DRAFT.

No evidence currently establishes:

1. A01 superseded by A02;
2. A01 superseded by A03;
3. A02 accepted by Protocol Custodian;
4. A03 accepted by Protocol Custodian;
5. A01 revoked;
6. an authority act assigning ADR-001 to a new subject;
7. a supersession chain resolving the identifier collision.

Therefore the correct forensic disposition remains:

`SD-045 = CONFLICTED / OPEN`

## 11. Closure-Gate Input

This reconstruction may be used as evidence input to a later Stage 07 Closure Gate.

It does **not** satisfy the closure condition requiring an independently evidenced authority act resolving the conflict.

Current state:

```text
Stage 07 evidence pass       COMPLETE
ADR-001 re-entry             EXECUTED
Genealogy reconstruction     COMPLETE
Supersession proof           NOT ESTABLISHED
Authority resolution         NOT ESTABLISHED
SD-045                       CONFLICTED / OPEN
Stage 07 formal closure      BLOCKED
Stage 08                     NOT AUTHORIZED
```

## 12. Non-Resolution Boundary

This record does not:

- select A01, A02 or A03 as canonical;
- rename or edit any ADR;
- declare a supersession;
- infer an approval from authorship, timestamp, merge, or status alone;
- alter governance documents;
- authorize Stage 08.
