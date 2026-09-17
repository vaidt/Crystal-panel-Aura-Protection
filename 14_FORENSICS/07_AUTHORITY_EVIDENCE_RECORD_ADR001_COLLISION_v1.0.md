# AURA — STAGE 07 AUTHORITY EVIDENCE RECORD v1.0

**Record ID:** AE-R-ADR001-COLLISION-001  
**Date:** 2026-09-17  
**Source repository:** `Aura-IDToken/aura-specification`  
**Forensic repository:** `vaidt/Crystal-panel-Aura-Protection`  
**Stage:** 07 — Authority Evidence / Re-entry  
**Authority:** NONE  
**Normative effect:** NONE  
**Disposition:** OBSERVED — LOAD-BEARING GOVERNANCE CONFLICT OPEN

---

## 1. Purpose

This record formally captures a newly confirmed governance finding discovered during Stage 07 Re-entry:

```text
ADR-001
   │
   ├── Repository Structure
   │      ACCEPTED
   │
   ├── Document Model
   │      PROPOSED
   │
   └── Document Model duplicate
          DRAFT
```

The record does **not** select one representation, declare a winner, infer supersession, or resolve authority.

The immediate forensic requirement is to preserve the finding as evidence and then reconstruct its genealogy, reachability, supersession path, and applicable authority path before any further Stage 07 Closure Gate is attempted.

---

## 2. Confirmed current-main representations

### AE-R-001 — Repository Structure

**Path:** `adrs/ADR-001_REPOSITORY_STRUCTURE.md`  
**Current blob:** `3df6315b5b9883753d29668870bdace611e37f23`  
**Status:** `ACCEPTED`  
**Date:** `2026-07-23`  
**Author:** Documentation Architect

The document identifies itself as `ADR-001 — Canonical Repository Structure`, defines the repository hierarchy, and states `Supersedes: —` and `Superseded By: —`. fileciteturn510file0L2-L4

### AE-R-002 — Document Model

**Path:** `adrs/ADR-001_DOCUMENT_MODEL.md`  
**Current blob:** `66083e286a2fc33e70ccab4d1df6015ec0be65fd`  
**Status:** `PROPOSED`  
**Date:** `2026-08-02`  
**Decision Owner:** Protocol Custodian

The document defines ARC → SPEC → APS as the proposed canonical document model and explicitly requires Protocol Custodian approval. It states that approval is recorded by an `Accepted-by` entry and merging the ADR into the canonical branch. fileciteturn511file0L2-L4

### AE-R-003 — Document Model duplicate representation

**Path:** `docs/adr/001-document-model.md`  
**Current blob:** `340ed584082baf5353ce0496034484ab6379ac45`  
**Status:** `DRAFT`  
**Version:** `1.0`  
**Date:** `2026-08-02`  
**Decision Owner:** Protocol Custodian

The document carries the same ADR identifier and Document Model subject, but has a separate path and blob. It requires `accepted_by` plus merge for acceptance and remains DRAFT. It also states that the ADR does not supersede existing protocol specifications unless explicitly referenced and superseded by a subsequent ADR. fileciteturn512file0L2-L4

---

## 3. Genealogy evidence

### 3.1 Repository Structure lineage

GitHub path history shows `adrs/ADR-001_REPOSITORY_STRUCTURE.md` entering the repository in commit:

- **Commit:** `b68181e48a65ed3a96007b5f3f89bad20a1caabf`
- **Date:** `2026-07-23T21:03:00Z`
- **Message:** `feat: build complete canonical repository structure for aura-specification`
- **Parent:** `7a22522350a0e917fa773d724854796778623147`
- **Verification:** valid GitHub signature
- **Commit effect:** repository structure bootstrap, including `/adrs` and `ADR-001 (repository structure decision)`.

The path history returned by GitHub identifies this commit as the path's commit. fileciteturn507file0L2-L5

### 3.2 Document Model lineage

GitHub path history shows `adrs/ADR-001_DOCUMENT_MODEL.md` entering the repository in commit:

- **Commit:** `3c68a36bdb464b1a2f3edc81cab282b7850de02d`
- **Date:** `2026-08-02T19:10:34Z`
- **Message:** `adr: add ADR-001 Document Model: ARC -> SPEC -> APS`
- **Parent:** `812598e349bd830d688f3e9e4ba728e29a645a7d`
- **Verification:** unsigned
- **Commit author/committer:** `Aura-IDToken`

The path history confirms this is a distinct later artifact from the July repository-structure ADR. fileciteturn508file0L2-L5

### 3.3 Document Model duplicate lineage

GitHub path history shows `docs/adr/001-document-model.md` entering the repository in commit:

- **Commit:** `c4ba21506066f873ac574edb01ddba679feb4142`
- **Date:** `2026-08-02T19:31:16Z`
- **Message:** `adr: add ADR-001 to docs/adr/001-document-model.md on branch docs/adr-001-document-model (#10)`
- **Parent:** `3c68a36bdb464b1a2f3edc81cab282b7850de02d`
- **Verification:** valid GitHub signature

Critically, the duplicate was committed **21 minutes after** the `adrs/ADR-001_DOCUMENT_MODEL.md` commit and has the latter as its direct parent. fileciteturn509file0L2-L5

This establishes genealogy as:

```text
2026-07-23
b68181e4
ADR-001 — Repository Structure
        │
        │ later repository history
        ▼
2026-08-02 19:10Z
3c68a36b
ADR-001 — Document Model
        │
        │ direct parent
        ▼
2026-08-02 19:31Z
c4ba2150
ADR-001 — Document Model duplicate path
```

This is a genealogy fact. It is **not** a supersession fact.

---

## 4. Supersession analysis

### Observed

- `ADR-001_REPOSITORY_STRUCTURE.md` explicitly contains no `Supersedes` or `Superseded By` relation. fileciteturn510file0L2-L4
- Neither current Document Model representation establishes a relation that supersedes the Repository Structure ADR.
- The Document Model duplicate is genealogically downstream of the first Document Model commit, but no explicit supersession marker has been located.
- Current repository evidence therefore establishes coexistence, not replacement.

### Forensic disposition

**Supersession:** `UNPROVEN`

No inference is permitted from:

- later date;
- later path;
- different directory;
- different status;
- direct parentage;
- title similarity;
- semantic relationship between subjects.

---

## 5. Authority-path analysis

### Repository Structure ADR

Current artifact says `Status: ACCEPTED`, but the present evidence establishes repository integration and the artifact's own status declaration. It does not, by itself, establish a separately evidenced competent approval act for that ADR.

### Document Model ADR

Current `adrs/` representation says `PROPOSED` and requires Protocol Custodian approval. No `Accepted-by` entry is present in the current representation. fileciteturn511file0L2-L4

### Duplicate Document Model representation

Current `docs/adr/` representation says `DRAFT` and likewise requires explicit acceptance conditions. No executed acceptance is present. fileciteturn512file0L2-L4

### Authority disposition

```text
Repository Structure ADR
  declared ACCEPTED
  ↓
  independent approval act NOT established by this record

Document Model ADR
  PROPOSED
  ↓
  Protocol Custodian acceptance NOT evidenced

Document Model duplicate
  DRAFT
  ↓
  Protocol Custodian acceptance NOT evidenced
```

**Authority status:** `CONFLICTED` for the identifier/subject namespace; no Document Model acceptance established.

---

## 6. Load-bearing impact

The conflict is load-bearing because `ADR-001` is used as an architectural decision identifier while the three reachable representations do not identify the same lifecycle state or subject.

The repository's own normalization audit independently records this as a load-bearing open surface: one identifier, three documents, three statuses, and two subjects, with dependency on citations of `ADR-001` including the SPEC-approval-authority claim. fileciteturn506file0L8-L18

The conflict therefore affects the evidentiary interpretation of any statement that relies on `ADR-001` without a path/blob-qualified referent.

---

## 7. Required next forensic actions

1. Preserve all three representations as distinct evidence objects.
2. Complete genealogy for each representation through all reachable refs relevant to Stage 07.
3. Search for explicit `Supersedes`, `Superseded By`, acceptance, revocation, replacement, or retirement acts.
4. Search PR/review/merge evidence for the Document Model subject and for the Repository Structure ADR.
5. Determine whether any competent authority act identifies which ADR-001 subject/representation was intended to be authoritative.
6. Cross-reference all current and historical citations of bare `ADR-001` and classify whether the referent is path-qualified, subject-qualified, or ambiguous.
7. Do not select, merge, rename, delete, or otherwise reconcile the representations during forensic reconstruction.
8. Execute the next Stage 07 Closure Gate only after the above evidence path is recorded.

---

## 8. State transition

```text
PREVIOUS STAGE 07 STATE
SD-045 = CONFLICTED
        │
        ▼
NEW EVIDENCE
ADR-001 identifier collision confirmed as three reachable representations
        │
        ▼
RE-ENTRY
        │
        ├── genealogy = partially resolved / confirmed distinct lineage
        ├── supersession = UNPROVEN
        ├── Document Model authority = not evidenced
        └── identifier/subject collision = OPEN
        │
        ▼
NEXT STEP
Complete genealogy + supersession + authority-path cross-reference
        │
        ▼
NO CLOSURE GATE YET
```

---

## 9. Forensic conclusion

The finding is confirmed as a **load-bearing governance/document-identity conflict**.

The evidence currently supports the following facts:

- three current-main reachable ADR-001 representations exist;
- one concerns Repository Structure and declares `ACCEPTED`;
- two concern Document Model and declare `PROPOSED` / `DRAFT`;
- the two Document Model representations have distinct blobs and distinct paths;
- the duplicate Document Model representation is directly descended from the first Document Model commit;
- no explicit supersession relation has been established;
- no independent Protocol Custodian acceptance of the Document Model ADR has been established;
- no forensic basis exists to choose one representation as the authoritative ADR-001 merely from these facts.

**Disposition:** `OPEN — RE-ENTRY REQUIRED`  
**Authority:** NONE  
**Normative effect:** NONE  
**Stage 07:** OPEN  
**Stage 08:** NOT AUTHORIZED
