# AURA — STAGE 07 AUTHORITY EVIDENCE REGISTER v1.0

**Artifact:** `14_FORENSICS/07_AUTHORITY_EVIDENCE_REGISTER_v1.0.md`  
**Source repository:** `Aura-IDToken/aura-specification`  
**Forensic repository:** `vaidt/Crystal-panel-Aura-Protection`  
**Stage:** 07 — Authority Evidence Register  
**Status:** OPEN — CONTROLLED AUTHORITY RECONSTRUCTION  
**Authority:** NONE  
**Normative effect:** NONE  

## 1. Purpose

Stage 07 does not determine what a semantic delta says. Stage 06 already records the content-level semantic change. Stage 07 determines whether an observed semantic delta has an evidenced authority basis.

The governing chain is:

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
DATE
      ↓
SCOPE
      ↓
REACHABILITY
      ↓
SIGNATURE / VERIFICATION
      ↓
CONFLICTING EVIDENCE
      ↓
SUPERSESSION / REVERT
      ↓
AUTHORITY STATUS
```

No authority is inferred from:

- branch name;
- commit message;
- filename;
- `MUST` / `SHALL` wording alone;
- a document's self-description as `CANONICAL`, `FINAL`, `ACCEPTED`, or `FROZEN`;
- implementation behaviour;
- mere presence on `main`;
- PR merge alone where the governing process requires an additional approval act.

## 2. Authority status vocabulary

| Status | Meaning |
|---|---|
| `EVIDENCED` | Authority act is directly supported by primary evidence and its scope is identifiable. |
| `CLAIMED_ONLY` | Artifact asserts authority, but the required authority act has not been independently established. |
| `PROPOSED` | Artifact explicitly remains proposal/draft/review state. |
| `NON_AUTHORITY` | Artifact explicitly performs audit, review, evidence, or implementation work without authority to decide. |
| `REVERSED` | The repository state produced by the authority-claiming act was explicitly reverted. |
| `SUPERSESSION_UNPROVEN` | A later artifact appears related/replacement-like, but explicit supersession authority is not established. |
| `CONFLICTED` | Material authority evidence points in incompatible directions and no competent resolution is established. |
| `UNRESOLVED` | Required authority evidence has not yet been located or is insufficient to classify the claim. |

## 3. Governing authority model recovered from current repository

Current `GOVERNANCE.md` identifies the Chief Architect as having final and sole approval authority over Constitution amendments, APS status transitions, invariant additions/removals, and recognition of new reference implementations. It separately assigns ADR, ARR, RFC, ADC, ACI and EPR roles. fileciteturn299file0L2-L2

For major protocol changes, the documented process is RFC → comment period → Architecture Review Board assessment → Chief Architect approval → RFC transition to APPROVED, followed by implementation. The ADR process separately states that merging an ADR accepts the ADR and that its status is set to ACCEPTED. fileciteturn299file0L2-L2

Therefore Stage 07 must test each claimed authority against the authority mechanism applicable to that artifact type. It must not use a single generic "merged = authoritative" rule across all artifact classes.

## 4. Authority Evidence Records

### AE-001 — Repository governance hierarchy

**Semantic delta:** governance model / repository lifecycle  
**Claimed authority:** `GOVERNANCE.md` states the authority hierarchy and lifecycle.  
**Authority source:** `GOVERNANCE.md`, GOV-001, current `main`.  
**Actor:** repository governance document identifies Chief Architect, ARB, Specification Contributors and AI Assistants by role.  
**Act / approval:** document-level governance declaration; no separate approval act established by this record.  
**Date:** current file; historical establishment date requires commit genealogy.  
**Scope:** repository governance and change process.  
**Reachability:** current `main`.  
**Signature / verification:** Git-level provenance exists; no separate governance signature is established here.  
**Conflicting evidence:** other artifacts contain more specific/variant authority models and must be compared before treating every statement as operative.  
**Supersession / revert:** not established here.  
**Authority status:** `CLAIMED_ONLY`.

### AE-002 — ADR-001 document model

**Semantic delta:** ARC → SPEC → APS document/authority model.  
**Claimed authority:** ADR-001 proposes canonical document classes, ownership and lifecycle.  
**Authority source:** `adrs/ADR-001_DOCUMENT_MODEL.md`.  
**Actor:** authors identify `Chief Specification Architect`; Decision Owner is `Protocol Custodian`.  
**Act / approval:** **none evidenced in the current artifact**. The document explicitly states `Status: PROPOSED` and requires explicit Protocol Custodian approval.  
**Date:** `2026-08-02`.  
**Scope:** documentation architecture and traceability.  
**Reachability:** current `main`.  
**Signature / verification:** Git provenance only; no accepted-by line is present.  
**Conflicting evidence:** current artifact itself requires approval before canonicalization.  
**Supersession / revert:** not established.  
**Authority status:** `PROPOSED`. fileciteturn301file0L2-L2

### AE-003 — ADR-CK003-DQ006 canonical serialization decision

**Semantic delta:** RFC 8785 JCS canonical representation and related byte-domain contract.  
**Claimed authority:** ADR declares `Status: ACCEPTED (decision)` and identifies APS-200 §8 as normative home.  
**Authority source:** `ck003/dq-006-canonical-serialization/ADR-CK003-DQ006-CANONICAL-SERIALIZATION.md`.  
**Actor:** ADR content identifies a decision but the inspected current file does not independently provide a named Chief Architect approval act for the DQ-006 closure verdict.  
**Act / approval:** decision recorded in ADR; **Chief Architect ratification of the DQ-006 closure verdict is explicitly still required**.  
**Date:** reconciled `2026-08-20`; current file records execution evidence separately.  
**Scope:** canonical serialization decision, not automatically the complete DQ-006 closure.  
**Reachability:** current `main`.  
**Signature / verification:** Git provenance is available; separate authority signature/approval evidence not established by this artifact.  
**Conflicting evidence:** the same ADR explicitly distinguishes accepted decision from unclosed closure gate; current `GOVERNANCE.md` assigns final approval authority for major protocol changes to the Chief Architect.  
**Supersession / revert:** no supersession of the decision itself established.  
**Authority status:** `CLAIMED_ONLY` for independent Chief-Architect ratification; `EVIDENCED` only as a recorded ADR decision if the repository's ADR merge rule is the applicable authority mechanism. fileciteturn300file0L2-L2

### AE-004 — P0-1 Canonical Representation Contract

**Semantic delta:** explicit RFC 8785 JCS canonical representation contract.  
**Claimed authority:** artifact states `ACCEPTED BY CHIEF ARCHITECT — 2026-08-22`.  
**Authority source:** `closures/P0-1_CANONICAL_REPRESENTATION_CONTRACT.md`.  
**Actor:** Chief Architect, as named by the artifact.  
**Act / approval:** explicit acceptance claim recorded in the artifact.  
**Date:** `2026-08-22`.  
**Scope:** canonical JSON representation profile.  
**Reachability:** branch/commit provenance established; current default-branch reachability of the exact closure artifact must be independently checked before treating it as a current authority source.  
**Signature / verification:** Git commit provenance exists; an independent cryptographic governance signature is not established by the artifact excerpt.  
**Conflicting evidence:** P0-1 itself preserves remaining evidence gates and does not declare DQ-006 evidence complete.  
**Supersession / revert:** not established.  
**Authority status:** `CLAIMED_ONLY` pending verification of the acceptance act and its reachable canonical authority path. fileciteturn305file0L3-L7

### AE-005 — P0-2 Evidence / Hash Domain Contract

**Semantic delta:** separation of canonical bytes, evidence/object digests, Merkle domains and evidence-chain linkage.  
**Claimed authority:** artifact states `ACCEPTED BY CHIEF ARCHITECT — 2026-08-22`.  
**Authority source:** `closures/P0-2_EVIDENCE_HASH_DOMAIN_CONTRACT.md`.  
**Actor:** Chief Architect, as named by the artifact.  
**Act / approval:** explicit acceptance claim recorded in artifact.  
**Date:** `2026-08-22`.  
**Scope:** evidence/hash-domain contract; explicitly leaves `previous_record_hash` mapping unresolved.  
**Reachability:** exact artifact reachability on current main requires direct verification.  
**Signature / verification:** Git provenance; separate authority signature not independently established.  
**Conflicting evidence:** P0-2 itself says the Audit Record mapping remains unresolved and that implementation behaviour is not the normative answer.  
**Supersession / revert:** not established.  
**Authority status:** `CLAIMED_ONLY` pending authority-path verification. fileciteturn306file0L3-L7

### AE-006 — DQ-003 specification reconciliation / revert

**Semantic delta:** APS-200 §6–§10 reference-reconciliation record.  
**Claimed authority:** PR #34 / reconciliation artifact operated as a governance/traceability control record, not a normative amendment.  
**Authority source:** `dq-003/specification-reconciliation` line and PR #34.  
**Actor:** branch author(s); exact competent approving actor requires PR evidence.  
**Act / approval:** PR #43 explicitly reverts commit `74220d27f6af01f335fb1423886a51eb063f90f7`; resulting main HEAD is the revert state.  
**Date:** revert merged `2026-09-10T22:09:45Z`.  
**Scope:** repository state introduced by the reverted DQ-003 reconciliation commit.  
**Reachability:** revert is on current `main`.  
**Signature / verification:** GitHub commit signature/provenance available; authority meaning of the revert is repository-state reversal, not adjudication of the underlying specification question.  
**Conflicting evidence:** the reverted artifact remains historical evidence; current main does not retain its tree state.  
**Supersession / revert:** `REVERTED` by PR #43.  
**Authority status:** `REVERSED` as repository state; underlying DQ-003 semantic propositions remain historical/unresolved unless separately ratified. fileciteturn308file0L3-L7

### AE-007 — DQ-002 closure assertions

**Semantic delta:** Merkle/hash-domain closure assertions and evidence.  
**Claimed authority:** multiple DQ-002 closure/audit artifacts report PASS/CLOSED states.  
**Authority source:** DQ-002 audit and closure artifacts.  
**Actor:** audit authors / implementation evidence authors.  
**Act / approval:** executed oracle evidence is not equivalent to Chief Architect approval; current audit explicitly states DQ-002 remained `BLOCKED` because normative and completeness gates were unmet.  
**Date:** `2026-08-20` revision 2 for the forensic closure audit.  
**Scope:** evidence and conformance status, not automatic protocol authority.  
**Reachability:** relevant branch evidence exists; exact current-main reachability varies by artifact.  
**Signature / verification:** execution evidence is reproducible according to the audit; governance approval is not established by execution alone.  
**Conflicting evidence:** audit revision 2 explicitly records `BLOCKED`, including unresolved normative Merkle profile and ADR disagreement.  
**Supersession / revert:** multiple later closure/reconciliation variants exist; explicit supersession must be determined per artifact.  
**Authority status:** `CONFLICTED` at the closure-assertion level; not evidence of a final normative closure without separate authority act. fileciteturn310file0L3-L7

### AE-008 — DQ-003 execution evidence

**Semantic delta:** execution-level conformance assessment of RI-PY and RI-RS against DQ-003 Golden Fixture.  
**Claimed authority:** fixture is described as sole authority for the comparison, but the artifact itself is a read-only execution attempt.  
**Authority source:** `conformance(dq-003): record read-only entry-point execution attempt`.  
**Actor:** audit/conformance author.  
**Act / approval:** no implementation remediation or normative decision.  
**Date:** recorded in commit lineage; exact commit date to be retained from Stage 06.  
**Scope:** conformance observation only.  
**Reachability:** branch-local evidence.  
**Signature / verification:** Git provenance plus execution claims.  
**Conflicting evidence:** RI-PY and RI-RS show different degrees of conformance; this does not itself select authority.  
**Supersession / revert:** not established.  
**Authority status:** `NON_AUTHORITY`. fileciteturn309file0L3-L7

## 5. Critical authority findings

### A-01 — "Accepted decision" and "closure verdict" are distinct

The current DQ-006 ADR explicitly separates the accepted canonical-serialization decision from the still-unratified DQ-006 closure verdict. Therefore the authority register MUST preserve two different subjects rather than collapsing them into one `ACCEPTED` state. fileciteturn300file0L2-L2

### A-02 — Repository presence is not sufficient authority

Current governance assigns different approval mechanisms to different artifact classes and requires Chief Architect approval for major protocol changes. Therefore a file being reachable from `main` cannot by itself establish protocol authority. fileciteturn299file0L2-L2

### A-03 — Execution evidence is not an approval act

The DQ-003 execution record explicitly describes itself as read-only, with no remediation and no fixture/specification modification. Its results are evidence, not an authority act. fileciteturn309file0L3-L7

### A-04 — Revert is a repository-state fact, not semantic adjudication

PR #43 explicitly reverts the DQ-003 reconciliation commit. This establishes that the introduced repository state was reversed on `main`; it does not by itself establish that every proposition contained in the reverted artifact is false or superseded. fileciteturn308file0L3-L7

### A-05 — Proposed artifacts remain proposed even when highly detailed

ADR-001 currently says `PROPOSED` and explicitly requires Protocol Custodian approval. Its content therefore cannot be promoted to authoritative document-model policy from content quality or repository reachability alone. fileciteturn301file0L2-L2

## 6. Open authority questions

1. Which exact Chief Architect acts are independently evidenced for P0-1 and P0-2, beyond the acceptance claims embedded in those artifacts?
2. What exact authority act bound the DQ-006 decision into current APS-200 §8, and what act, if any, ratified the closure verdict?
3. Which authority mechanism governs the DQ-002 Merkle tree-shape and odd-node rules, given the audit's finding that the approved Aura Merkle profile is absent?
4. Is `ADR-001` ever approved, or does its `PROPOSED` state remain current?
5. Which DQ-003 artifacts were merely audit evidence and which, if any, received a competent normative decision?
6. Which BC-02 artifacts contain decision acts versus decision proposals/review surfaces?
7. For every claimed authority, is the exact artifact reachable from the canonical branch or another explicitly accepted publication mechanism?

## 7. Stage 07 exit criteria

Stage 07 may be closed only when every Stage 06 semantic delta that claims authority has an explicit authority evidence record containing:

- primary authority source;
- actor;
- act/approval;
- date;
- scope;
- reachability;
- signature/verification state;
- conflicting evidence;
- supersession/revert relation;
- final authority status.

No `EVIDENCED` status should be assigned merely because an artifact says `ACCEPTED`, `FINAL`, `CLOSED`, or `CANONICAL`.

## 8. Current status

```text
STAGE 06 semantic inventory: CLOSED
              ↓
STAGE 07 authority reconstruction: OPEN
              ↓
authority claims separated from authority acts
              ↓
primary approval evidence still being resolved
```
