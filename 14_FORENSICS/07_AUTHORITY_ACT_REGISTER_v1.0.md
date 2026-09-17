# AURA — STAGE 07 AUTHORITY ACT REGISTER v1.0

**Artifact:** `14_FORENSICS/07_AUTHORITY_ACT_REGISTER_v1.0.md`
**Source repository:** `Aura-IDToken/aura-specification`
**Forensic repository:** `vaidt/Crystal-panel-Aura-Protection`
**Stage:** 07 — Authority Evidence
**Status:** OPEN — MECHANICAL ACT REGISTER
**Authority:** NONE
**Normative effect:** NONE

## 1. Purpose

This register records **actual authority acts evidenced in repository history or explicitly evidenced external approval records**. It does not infer authority from document wording, branch names, filenames, commit messages, merge status, or role attribution.

The register is deliberately narrower than the Stage 07 Authority Evidence Register:

```text
SEMANTIC DELTA
      ↓
CLAIMED AUTHORITY
      ↓
AUTHORITY SOURCE
      ↓
ACTOR
      ↓
ACT / APPROVAL
      ↓
EVIDENCE
      ↓
SCOPE
      ↓
EFFECTIVE DATE
      ↓
VERIFICATION
      ↓
STATUS
```

A repository event is not automatically an authority act.

## 2. Act classification

| Code | Meaning |
|---|---|
| `APPROVAL` | Explicit competent approval of a defined subject |
| `RATIFICATION` | Explicit confirmation of an already recorded decision |
| `DELEGATION` | Explicit transfer/designation of authority for a defined scope |
| `ACCEPTANCE` | Explicit acceptance under the applicable lifecycle |
| `RELEASE` | Explicit publication/release act by the designated release authority |
| `REVOCATION` | Explicit withdrawal of a prior authority act |
| `SUPERSESSION` | Explicit act replacing a prior authority-bearing artifact/decision |
| `REVERT` | Repository-state reversal; not semantic adjudication |
| `MERGE` | Repository integration event; not automatically approval |
| `DECLARATION` | Status/authority statement without independently evidenced act |
| `AUDIT` | Examination/evidence production without decision authority |
| `PREPARATION` | Instrument prepared for a future authority act |

## 3. Authority-status vocabulary

| Status | Definition |
|---|---|
| `EVIDENCED` | Competent act and evidence are both established |
| `CLAIMED_ONLY` | Authority is asserted but the act is not independently established |
| `PROPOSED` | Instrument proposes an act that has not been executed |
| `NON_AUTHORITY` | Record explicitly does not exercise authority |
| `CONFLICTED` | Competing authority claims or acts require reconciliation |
| `REVERSED` | Repository act was explicitly reverted |
| `SUPERSESSION_UNPROVEN` | Supersession is claimed or suspected but the superseding act is not established |
| `UNRESOLVED` | Evidence is insufficient to classify the act |

## 4. Mechanical records

### AA-001 — Initial repository bootstrap

**Subject:** Initial Aura specification repository structure and embedded canonical/authoritative/frozen declarations.

**Primary repository event:** `93f677fe34bf3f3fe0e8abffd6c8fdfd92b7958f`

**Act type:** `MERGE` + `DECLARATION`

**Actor evidence:** repository history records the bootstrap merge and its associated PR path.

**Authority source claimed:** repository governance / Constitution declarations embedded in the imported corpus.

**Actual authority act located:** **NO independent approval act located in the forensic pass.**

**Evidence:** the commit establishes that the repository structure and declarations entered Git history. It does not independently establish the competent approval of each embedded canonical/authoritative/frozen claim.

**Scope:** initial repository structure, governance scaffolding and historical specification import.

**Reachability:** historical repository lineage established; individual artifact reachability remains artifact-specific.

**Verification:** Git provenance available.

**Status:** `CLAIMED_ONLY` for the embedded authority declarations; `EVIDENCED` only for the repository bootstrap event.

**Disposition:** retain as historical evidence; do not promote embedded status declarations to independent authority.

---

### AA-002 — ARC/SPEC governance correction attributed to Chief Architect

**Subject:** ARC/SPEC lifecycle and mapping structure.

**Primary commit:** `102423256e33ad3dea54461f692819aeebaa0700`

**Act type:** `DECLARATION` / repository documentation change.

**Commit attribution:** `docs(spec): apply Chief Architect corrections to ARC/SPEC templates and mapping structure`.

**Actor evidence:** Aura-IDToken author/committer recorded in Git.

**Authority source claimed:** Chief Architect correction.

**Actual authority act located:** **NO independent approval/signature record located.**

**Evidence:** commit proves the attributed correction was recorded; it does not prove an independently evidenced Chief Architect approval act or complete authority scope.

**Scope:** ARC/SPEC documentation workflow, mapping lifecycle and templates.

**Status:** `CLAIMED_ONLY` for the Chief Architect authority claim; `EVIDENCED` as a repository documentation change.

**Disposition:** do not use the commit message alone as approval evidence.

---

### AA-003 — DQ-006 canonical serialization decision record

**Subject:** RFC 8785 JCS canonical serialization, UTF-8 canonical bytes and associated hash-domain contract.

**Primary authority-bearing records:** ADR-CK003-DQ006 and PR #26 line.

**Act type:** `ACCEPTANCE` / `DECISION-RECORDED` claimed by the ADR/merge lineage.

**Actual authority act located:** repository decision record exists; **independent Chief Architect ratification of the DQ-006 closure was not located.**

**Evidence:** current repository records distinguish the normative protocol contract from implementation detail and state that the canonical serialization decision is bound into APS-200 §8 and APS-300 §5. fileciteturn336file0L2-L14

**Scope:** canonical serialization and related evidence/hash domains.

**Important distinction:** recorded decision ≠ final ratification of closure.

**Status:** `CLAIMED_ONLY` for independent final Chief Architect ratification; `DECISION-RECORDED` as repository evidence.

**Disposition:** preserve decision and ratification as separate authority subjects.

---

### AA-004 — P0-1 acceptance declaration

**Subject:** P0-1 Canonical Representation Contract.

**Primary commit:** `4154cc0d89b5cb3490d1d60b2efe43687c9e1ff5`

**Act type:** `DECLARATION` / claimed `ACCEPTANCE`.

**Claimed actor:** Chief Architect.

**Claimed act:** artifact states `ACCEPTED BY CHIEF ARCHITECT — 2026-08-22`.

**External approval evidence:** PR #31 has no formal review records returned by GitHub and no independent approval act was located in the forensic pass. fileciteturn407file0L2-L7

**Scope:** canonical representation contract.

**Status:** `CLAIMED_ONLY`.

**Disposition:** retain the acceptance statement as historical evidence of a claim; do not treat it as independently evidenced authority.

---

### AA-005 — P0-2 acceptance declaration

**Subject:** P0-2 Evidence / Hash Domain Contract.

**Primary commit:** `cb0494524da740399416020151db305c48aa316b`

**Act type:** `DECLARATION` / claimed `ACCEPTANCE`.

**Claimed actor:** Chief Architect.

**Claimed act:** artifact states `ACCEPTED BY CHIEF ARCHITECT — 2026-08-22`.

**External approval evidence:** PR #32 has no formal review records returned by GitHub and no independent approval act was located in the forensic pass. fileciteturn408file0L2-L7

**Scope:** evidence/hash-domain contract, including the unresolved mapping of `previous_record_hash`.

**Status:** `CLAIMED_ONLY`.

**Disposition:** retain as claim; authority not independently established.

---

### AA-006 — DQ-002 closure assertion

**Subject:** DQ-002 final closure / PASS assertion.

**Primary branch lineage:** `b6bc7992fd15cf18f2e44e0f17b35ad97ed50e10`.

**Act type:** `DECLARATION` / claimed `CLOSURE`.

**Actual authority act located:** no independent authority act establishing the closure was located. Later forensic execution evidence explicitly preserved a `BLOCKED` verdict because normative Merkle profile/tree-shape/odd-node questions and conflicting leaf domains remained unresolved. fileciteturn310file0L3-L7

**Scope:** DQ-002 closure assertion and CANONICAL-001 evidence boundary.

**Status:** `CONFLICTED` at closure-assertion level.

**Disposition:** preserve both the historical closure assertion and later blocking evidence; do not collapse them into a single status.

---

### AA-007 — DQ-006 controlled final-closure gate

**Subject:** DQ-006 final closure execution order.

**Primary commit:** `ad7548cc6ff830ac8af68a1ec09bffd201f27e58`.

**Act type:** `AUDIT` / `CONTROL GATE`.

**Actual authority act located:** **NONE.**

**Evidence:** the execution-order record explicitly preserves DQ-006 as OPEN and identifies residual requirements including a JCS-discriminating fixture, authoritative RI-RS boundary, evidence reachability and Chief Architect ratification.

**Scope:** closure sequencing and gate definition.

**Status:** `NON_AUTHORITY`.

**Disposition:** use as evidence that the closure process itself required further authority/evidence; not as the closure act.

---

### AA-008 — Q1 Chief Architect approval/delegation preparation

**Subject:** Q1 Decision Surface jurisdiction.

**Primary commit:** `6002c4910c1eefd056aff77229707904cffb3d30`.

**Act type:** `PREPARATION`.

**Claimed competent authority:** Chief Architect.

**Actual act:** **UNEXECUTED.**

**Evidence:** approval status is PENDING; Q1 jurisdiction is NOT ESTABLISHED; approval fields remain placeholders.

**Scope:** proposed delegation/designation of Q1 Decision Surface.

**Status:** `PROPOSED` / `NON_AUTHORITY`.

**Disposition:** cannot be used as evidence that Q1 jurisdiction exists.

---

### AA-009 — Q1 Scope Bridge

**Subject:** Chief Architect → Protocol Custodian Q1 scope bridge.

**Primary commit:** `eb263ce3f325fd14213c49fff1ab2da3453c426f`.

**Act type:** `PREPARATION`.

**Actual authority act:** **NONE.**

**Evidence:** artifact is explicitly `DRAFT — NON-BINDING PREPARATION`, states `Authority exercised by this document: NONE` and `Delegation effective: NO — pending competent approval`.

**Scope:** Q1 decision-surface designation only.

**Status:** `NON_AUTHORITY`.

**Disposition:** no Q1 jurisdiction established.

---

### AA-010 — BC-02 / BC-02.1 Custodian Decision Package A/B

**Subject:** BC-02 and BC-02.1 unresolved governance decisions.

**Primary commit:** `dd11311bff7c19ace8cddc002402ce2e04a3c3c4`.

**Act type:** `PREPARATION`.

**Actual authority act:** **NONE.**

**Evidence:** package explicitly records `Authority: NONE`, `Conformance authority: NONE`, `Execution authority: NONE`, and leaves Decisions A/B unresolved.

**Actor boundary:** the package states that its authoring role is not Protocol Custodian or Independent Reviewer.

**Scope:** decision preparation/routing.

**Status:** `NON_AUTHORITY`.

**Disposition:** candidate dispositions are evidence of questions considered, not decisions taken.

---

### AA-011 — DQ-003 reconciliation and subsequent revert

**Subject:** DQ-003 specification reconciliation.

**Primary act:** merge of PR #34 at `74220d27f6af01f335fb1423886a51eb063f90f7`.

**Subsequent act:** PR #43 revert, merge/current main `71133de047c71e0bc1156d58c20396fe593ace70`.

**Act type:** `MERGE` followed by `REVERT`.

**Evidence:** PR #34 itself records a read-only reference audit and states C4 remains NOT AUTHORIZED; no formal review was located. fileciteturn353file0L4-L23 PR #43 subsequently reverted the repository change.

**Important distinction:** the revert establishes repository-state reversal. It does not adjudicate the truth/falsity of the underlying DQ-003 proposition.

**Status:** `REVERSED` for repository state; underlying semantic propositions remain subject to separate authority determination.

---

## 5. External approval evidence search result

The mechanical GitHub review pass checked the principal PRs associated with authority-bearing claims, including PRs #5, #9, #17, #25, #26, #27, #31, #32, #34 and #43.

For the inspected authority-critical PRs, GitHub returned no formal review submissions. For example, PR #31 and PR #32 have empty review/comment surfaces in the connector results. fileciteturn407file0L2-L7 fileciteturn408file0L2-L7

PR #34 contains a top-level issue comment from the repository account, but its metadata has `pull_request_review_id: null` and `review: null`; therefore it is recorded as an issue comment/audit statement, not a formal review approval. fileciteturn353file0L4-L23

This register does **not** claim that no approval can exist outside the inspected GitHub evidence. It records only that such an approval was not located in the evidence currently available to this forensic pass.

## 6. Current authority-act matrix

| ID | Subject | Act located | Independent approval | Status |
|---|---|---|---|---|
| AA-001 | Initial canonical/bootstrap claims | Repository merge/declarations | No | `CLAIMED_ONLY` |
| AA-002 | ARC/SPEC Chief Architect correction | Repository change | No | `CLAIMED_ONLY` |
| AA-003 | DQ-006 canonical serialization decision | Decision record | Ratification not located | `CLAIMED_ONLY` |
| AA-004 | P0-1 | Acceptance declaration | No | `CLAIMED_ONLY` |
| AA-005 | P0-2 | Acceptance declaration | No | `CLAIMED_ONLY` |
| AA-006 | DQ-002 closure | Closure assertion | Conflicting evidence | `CONFLICTED` |
| AA-007 | DQ-006 final closure gate | Control/audit | No | `NON_AUTHORITY` |
| AA-008 | Q1 delegation | Preparation only | No | `PROPOSED` |
| AA-009 | Q1 Scope Bridge | Preparation only | No | `NON_AUTHORITY` |
| AA-010 | BC-02 A/B | Preparation only | No | `NON_AUTHORITY` |
| AA-011 | DQ-003 reconciliation | Merge + revert | No | `REVERSED` |

## 7. Closure condition for this register

`07_AUTHORITY_ACT_REGISTER` is **OPEN** until all authority-bearing claims identified by Stage 07 have one of the following mechanically defensible dispositions:

1. `EVIDENCED` — competent act independently evidenced;
2. `CLAIMED_ONLY` — explicit claim retained because no act was found;
3. `PROPOSED` — pending act explicitly recorded;
4. `NON_AUTHORITY` — record explicitly has no authority;
5. `CONFLICTED` — competing evidence retained without forced reconciliation;
6. `REVERSED` — repository-state reversal evidenced;
7. `SUPERSESSION_UNPROVEN` — supersession claim retained without proof;
8. `UNRESOLVED` — evidence insufficient for a more precise classification.

No record is promoted merely because a document says `APPROVED`, `ACCEPTED`, `FROZEN`, `CANONICAL`, or names the Chief Architect.

## 8. Next mechanical gate

Before Stage 07 Closure Gate:

```text
AUTHORITY CLAIM SET
        ↓
PRIMARY ACT REGISTER
        ↓
EXTERNAL APPROVAL / RATIFICATION SEARCH
        ↓
CONFLICT + REVERT + SUPERSESSION CHECK
        ↓
CURRENT-MAIN REACHABILITY CHECK
        ↓
FINAL AUTHORITY STATUS
```

Only after this chain is exhausted may `07_STAGE_CLOSURE_GATE` be evaluated.

**Stage 08 remains blocked.**
