# AURA — STAGE 07 AUTHORITY RE-ENTRY v1.0

**Date:** 2026-09-17  
**Source repository:** `Aura-IDToken/aura-specification`  
**Forensic repository:** `vaidt/Crystal-panel-Aura-Protection`  
**Stage:** 07 — Authority Evidence / Re-entry  
**Trigger:** `AE-R-ADR001-COLLISION-001`  
**Status:** RE-ENTRY EXECUTED — CONFLICT REMAINS OPEN  
**Authority:** NONE  
**Normative effect:** NONE

---

## 1. Re-entry mandate

Stage 07 re-entry was opened because a new load-bearing governance/document-identity finding was confirmed:

```text
ADR-001
   ├── Repository Structure → ACCEPTED
   ├── Document Model → PROPOSED
   └── Document Model duplicate → DRAFT
```

The re-entry mandate is forensic only. No representation is selected, merged, renamed, deleted, superseded, or promoted.

The re-entry sequence is:

```text
EVIDENCE RECORD
      ↓
GENEALOGY
      ↓
SUPERSESSION PATH
      ↓
AUTHORITY PATH
      ↓
DISPOSITION
      ↓
NO CLOSURE GATE YET
```

The underlying finding was first preserved in `07_AUTHORITY_EVIDENCE_RECORD_ADR001_COLLISION_v1.0.md`.

---

## 2. Subject inventory

| Record | Path | Subject | Current status | Blob |
|---|---|---|---|---|
| AE-R-001 | `adrs/ADR-001_REPOSITORY_STRUCTURE.md` | Canonical Repository Structure | ACCEPTED | `3df6315b5b9883753d29668870bdace611e37f23` |
| AE-R-002 | `adrs/ADR-001_DOCUMENT_MODEL.md` | Document Model — ARC → SPEC → APS | PROPOSED | `66083e286a2fc33e70ccab4d1df6015ec0be65fd` |
| AE-R-003 | `docs/adr/001-document-model.md` | Document Model — ARC → SPEC → APS | DRAFT | `340ed584082baf5353ce0496034484ab6379ac45` |

The current source contents confirm that these are three distinct repository representations. fileciteturn510file0L2-L4 fileciteturn511file0L2-L4 fileciteturn512file0L2-L4

---

## 3. Genealogy result

### 3.1 Repository Structure ADR

`adrs/ADR-001_REPOSITORY_STRUCTURE.md` entered the repository in:

- `b68181e48a65ed3a96007b5f3f89bad20a1caabf`
- `2026-07-23T21:03:00Z`
- parent `7a22522350a0e917fa773d724854796778623147`
- valid GitHub signature
- commit message identifies the complete repository-structure bootstrap and explicitly includes `ADR-001 (repository structure decision)`.

GitHub path history establishes this as the introducing commit for that path. fileciteturn507file0L2-L5

### 3.2 Document Model ADR

`adrs/ADR-001_DOCUMENT_MODEL.md` entered the repository in:

- `3c68a36bdb464b1a2f3edc81cab282b7850de02d`
- `2026-08-02T19:10:34Z`
- parent `812598e349bd830d688f3e9e4ba728e29a645a7d`
- unsigned commit
- message `adr: add ADR-001 Document Model: ARC -> SPEC -> APS`.

GitHub path history confirms the distinct later introduction. fileciteturn508file0L2-L5

### 3.3 Document Model duplicate

`docs/adr/001-document-model.md` entered the repository in:

- `c4ba21506066f873ac574edb01ddba679feb4142`
- `2026-08-02T19:31:16Z`
- direct parent `3c68a36bdb464b1a2f3edc81cab282b7850de02d`
- valid GitHub signature
- PR #10 merge commit.

PR #10 was merged to `main`, with base SHA `3c68a36bdb464b1a2f3edc81cab282b7850de02d`, head `b5a0c8c0b58e3cf738832763aca138ea7b9c4d7b`, and merge commit `c4ba21506066f873ac574edb01ddba679feb4142`. It changed one file. fileciteturn514file0L2-L16 fileciteturn514file0L28-L35

### 3.4 Genealogy conclusion

The two Document Model representations are genealogically related:

```text
3c68a36b  (adrs/ADR-001_DOCUMENT_MODEL.md)
    │
    │ direct parent
    ▼
c4ba2150  (docs/adr/001-document-model.md)
```

This proves ancestry. It does **not** prove that the second file superseded the first.

The Repository Structure ADR is earlier and has a separate subject. Its introduction occurred as part of the repository bootstrap PR #5, merged as `93f677fe34bf3f3fe0e8abffd6c8fdfd92b7958f`. fileciteturn515file0L2-L16

---

## 4. Supersession analysis

### 4.1 Explicit markers

The Repository Structure ADR currently states:

- `Supersedes: —`
- `Superseded By: —`.

No explicit supersession relation was found between the Repository Structure ADR and either Document Model representation. fileciteturn510file0L2-L4

The Document Model representations likewise do not establish a supersession relation between the two paths. The `docs/adr` representation explicitly states that the ADR does not supersede existing protocol specifications unless explicitly referenced and superseded by a subsequent ADR. fileciteturn512file0L2-L4

### 4.2 Temporal and genealogical evidence

- Later creation date does not establish supersession.
- Direct parentage establishes ancestry only.
- Different path establishes representation distinction only.
- Different status establishes lifecycle divergence only.
- Semantic similarity establishes related subject matter only.

### 4.3 Disposition

**Supersession:** `UNPROVEN`

No forensic inference may convert ancestry or coexistence into supersession.

---

## 5. Authority-path analysis

### 5.1 Repository Structure ADR

The artifact declares `ACCEPTED`. PR #5 was merged and the repository state transition is evidenced. PR #5 itself describes the change as governance/process and initial canonical repository structure and identifies ADR-001 as the related decision. fileciteturn515file0L8-L16

However, the evidence examined here does not contain a separate competent approval act for the Repository Structure ADR beyond repository integration and the artifact's own status declaration.

**Disposition:** `CLAIMED_ONLY` as an independently ratified authority act; `EVIDENCED` as a repository-state artifact and accepted-status declaration.

### 5.2 Document Model ADR

The `adrs/` representation states `PROPOSED` and names the Protocol Custodian as Decision Owner. It requires explicit Protocol Custodian approval and an `Accepted-by` entry plus merge. No such acceptance entry is present in the current content. fileciteturn511file0L2-L4

**Disposition:** `PROPOSED / CLAIMED_ONLY`; no acceptance evidenced.

### 5.3 Document Model duplicate

The `docs/adr` representation states `DRAFT`, names the same Decision Owner, and requires `accepted_by` plus merge before acceptance. No acceptance entry is present. fileciteturn512file0L2-L4

PR #10 proves that this representation was merged, but merge alone cannot satisfy the representation's own explicit acceptance condition where the required `accepted_by` evidence is absent.

**Disposition:** `DRAFT / CLAIMED_ONLY`; no acceptance evidenced.

### 5.4 Governance-rule interaction

Current `GOVERNANCE.md` states that merging a PR equals accepting an ADR and that ADR status is set to ACCEPTED. It also states that AI assistants may not self-approve or freeze canonical documents. fileciteturn516file0L2-L4

The Document Model representations impose an additional Protocol Custodian acceptance condition. No independent governance act was found in this re-entry that reconciles these two acceptance mechanisms for this ADR-001 subject.

Therefore the correct forensic result is **not** to choose the repository-wide merge rule over the ADR-local acceptance rule, or vice versa. The relationship itself remains an evidence gap.

---

## 6. Load-bearing classification

The prior normalization audit independently identified this surface as open because one identifier is used by three documents, with three statuses and two subjects, and because citations of bare `ADR-001` can therefore become ambiguous. fileciteturn506file0L8-L18

The present re-entry confirms that the conflict is not merely textual duplication:

1. the identifier namespace is reused;
2. the subjects are not identical;
3. the lifecycle states diverge;
4. the Document Model subject itself has two representations;
5. no explicit supersession relation resolves the coexistence;
6. authority requirements are not reconciled.

**Classification:** `LOAD-BEARING GOVERNANCE / DOCUMENT-IDENTITY CONFLICT`.

---

## 7. Stage 07 disposition update

| Subject | Previous Stage 07 | Re-entry result | Current disposition |
|---|---|---|---|
| SD-001 | CLAIMED_ONLY | no direct resolution | CLAIMED_ONLY |
| SD-003 | CLAIMED_ONLY | no direct resolution | CLAIMED_ONLY |
| SD-032 | CLAIMED_ONLY | no direct resolution | CLAIMED_ONLY |
| SD-045 | CONFLICTED | genealogy confirmed; supersession unproven; authority path unreconciled | **CONFLICTED / OPEN** |

This re-entry does not resolve SD-045. It makes the conflict more precisely characterized.

---

## 8. Closure-gate consequence

The next Stage 07 Closure Gate is **not executed by this artifact**.

Reason:

```text
ADR-001 collision confirmed
        ↓
genealogy materially reconstructed
        ↓
supersession NOT proven
        ↓
authority path NOT reconciled
        ↓
load-bearing conflict remains
        ↓
Stage 07 remains OPEN
        ↓
Stage 08 remains NOT AUTHORIZED
```

A future closure gate must evaluate the resulting evidence state, including whether an independent competent act resolves the identifier/subject collision and acceptance-path conflict.

---

## 9. No-resolution rule

This re-entry explicitly does **not**:

- choose Repository Structure as the authoritative ADR-001;
- choose Document Model as the authoritative ADR-001;
- choose either Document Model path as canonical;
- infer supersession from date or ancestry;
- infer acceptance from status text alone;
- infer Protocol Custodian approval from merge alone;
- delete, rename, merge, or rewrite any source artifact;
- reopen Stage 06 semantic reconstruction;
- authorize Stage 08.

---

## 10. Final forensic result

**RE-ENTRY RESULT: PARTIAL RESOLUTION OF EVIDENCE PATH — GOVERNANCE CONFLICT REMAINS OPEN.**

The forensic record now establishes:

```text
ADR-001 / Repository Structure
  introduced 2026-07-23
  ACCEPTED declaration
  supersession relation: none found

ADR-001 / Document Model
  introduced 2026-08-02 19:10Z
  PROPOSED
  Protocol Custodian acceptance: not evidenced

ADR-001 / Document Model duplicate
  introduced 2026-08-02 19:31Z
  direct descendant of Document Model commit
  DRAFT
  Protocol Custodian acceptance: not evidenced
```

The remaining issue is therefore no longer merely “there are duplicates.” It is a formally recorded **identifier + subject + lifecycle + authority-path collision** whose resolution requires evidence or an explicit competent governance act.

**Stage 07:** OPEN  
**SD-045:** CONFLICTED / OPEN  
**Supersession:** UNPROVEN  
**Authority:** NONE independently established for Document Model acceptance  
**Normative effect:** NONE  
**Stage 08:** NOT AUTHORIZED
