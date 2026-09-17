# AURA — STAGE 07 AUTHORITY EVIDENCE REGISTER v1.1

**Artifact:** `14_FORENSICS/07_AUTHORITY_EVIDENCE_REGISTER_v1.1_GITHUB_VERIFICATION.md`  
**Source repository:** `Aura-IDToken/aura-specification`  
**Forensic repository:** `vaidt/Crystal-panel-Aura-Protection`  
**Stage:** 07 — Authority Evidence Register  
**Parent:** `07_AUTHORITY_EVIDENCE_REGISTER_v1.0.md`  
**Status:** OPEN — GITHUB AUTHORITY-PATH VERIFICATION PASS  
**Authority:** NONE  
**Normative effect:** NONE  

## 1. Purpose

This amendment records primary GitHub evidence obtained after the initial Stage 07 register. It does not replace the semantic classifications of Stage 06 and does not infer authority from labels, branch names, commit messages, or embedded acceptance statements.

The test is:

```text
CLAIMED AUTHORITY
      ↓
PR / COMMIT RECORD
      ↓
ACTOR
      ↓
REVIEW / APPROVAL ACT
      ↓
MERGE / REACHABILITY
      ↓
SCOPE OF ACT
      ↓
AUTHORITY STATUS
```

A GitHub merge proves a repository-state transition. It is not automatically proof of Chief Architect approval where the governing process requires a separate approval act.

## 2. Directly verified governance rule

Current `GOVERNANCE.md` states that the Chief Architect has final and sole approval authority for major protocol-governance transitions, including Constitution amendments, APS status transitions, invariant additions/removals, and recognition of new reference implementations. It also states that major changes follow RFC → comment period → ARB assessment → Chief Architect approval → APPROVED → implementation. The same document says that, for ADRs, merging the PR constitutes acceptance of the ADR.

**Forensic consequence:** the authority test depends on artifact class. A merged ADR may obtain authority through the documented ADR mechanism; a merged normative protocol change still requires the applicable Chief Architect approval evidence where the governance document requires it.

## 3. Primary GitHub verification records

### AE-GH-001 — PR #31 / P0-1

**PR:** `#31 — spec(p0-1): Canonical Representation Contract`  
**Head:** `p0/p0-1-canonical-representation-contract`  
**Head SHA:** `4154cc0d89b5cb3490d1d60b2efe43687c9e1ff5  `  
**Base:** `main` at `9682cf53956f27c18821ac29531a356c5ed4afa5`  
**State:** OPEN  
**Draft:** YES  
**Merged:** NO  
**PR reviews:** NONE returned by GitHub connector  
**PR comments:** NONE returned by GitHub connector  
**Created:** `2026-08-22T17:37:42Z`

The PR body describes RFC 8785/JCS as the normative canonicalization profile and says the PR closes the protocol decision while leaving DQ-006 evidence gates open. However, GitHub currently records the PR as an open draft and no submitted reviews were returned.

The branch artifact itself states `ACCEPTED BY CHIEF ARCHITECT — 2026-08-22` and later says that the Chief Architect explicitly authorized proceeding. This is an **embedded claim inside the artifact**, not an independently located approval object in the PR record.

**Reachability on current `main`:** exact P0-1 closure artifact was queried on `main` and returned `404 Not Found`.

**Authority status:** `CLAIMED_ONLY`.

**Reason:** the acceptance claim exists in the branch artifact, but the corresponding PR is still an open draft, has no submitted reviews, and the exact closure artifact is not reachable from current `main`. No independent approval act has been located in the GitHub evidence examined in this pass.

### AE-GH-002 — PR #32 / P0-2

**PR:** `#32 — spec(p0-2): Evidence / Hash Domain Contract`  
**Head:** `p0/p0-2-evidence-hash-domain-contract`  
**Head SHA:** `cb0494524da740399416020151db305c48aa316b`  
**Base:** P0-1 head `4154cc0d89b5cb3490d1d60b2efe43687c9e1ff5`  
**State:** OPEN  
**Draft:** YES  
**Merged:** NO  
**PR reviews:** NONE returned by GitHub connector  
**PR comments:** NONE returned by GitHub connector  
**Created:** `2026-08-22T17:37:47Z`

The PR body records the explicit hash domains and deliberately leaves `previous_record_hash` unresolved rather than deriving it from RI-RS implementation behaviour.

The branch artifact states `ACCEPTED BY CHIEF ARCHITECT — 2026-08-22` and records that the Chief Architect authorized proceeding with P0-1 followed by P0-2. Again, this is an embedded claim; no independent approval act was located in the PR review/comment record examined here.

**Reachability on current `main`:** exact P0-2 closure artifact was queried on `main` and returned `404 Not Found`.

**Authority status:** `CLAIMED_ONLY`.

**Reason:** open draft PR, no submitted reviews, exact closure artifact absent from current `main`, and no independent approval record located.

### AE-GH-003 — PR #25 / specification integration of DQ-006

**PR:** `#25 — CK-003: reconcile APS-200 with DQ-006 and refresh closure controls`  
**Head:** `ck003/specification-integration-dq006`  
**Head SHA:** `7826db9e3e28d356693ba24618f320c44e3120b1`  
**Merge commit:** `9682cf53956f27c18821ac29531a356c5ed4afa5`  
**State:** CLOSED / MERGED  
**Created:** `2026-08-20T18:00:43Z`  
**Merged:** `2026-08-21T16:48:57Z`  
**PR reviews:** NONE returned by GitHub connector.

The PR body calls itself a Chief Architect execution package and states that merge is the review/approval boundary. It explicitly says there is no APS-001 approval, no DQ-003/DQ-004 closure, and no CI/release closure.

**Forensic interpretation:** the merge establishes that the specification integration branch was incorporated into repository history. The PR record does not independently evidence a Chief Architect approval submission/review. Therefore merge proves repository-state acceptance of the change, but does not by itself prove a separate Chief Architect authority act for every normative proposition introduced by the branch.

**Authority status:** `CLAIMED_ONLY` for Chief-Architect protocol authority; `EVIDENCED` only for the fact of repository merge.

### AE-GH-004 — PR #26 / DQ-006 reconciliation

**PR:** `#26 — spec(dq-006): reconcile canonical serialization closure across APS-200...`  
**Head SHA:** `a0df11afc6b0c97e0a3973a796f47b1f12964337`  
**Merge commit:** `ff30e166be2511b6d5684a33efb8c7da9d63a574`  
**State:** CLOSED / MERGED  
**Created:** `2026-08-20T20:41:45Z`  
**Merged:** `2026-08-20T20:42:07Z`  
**PR reviews:** NONE returned by GitHub connector.

The PR body explicitly binds RFC 8785 JCS, SHA-256, RFC-6962-style byte domains, APS-300 §5, and changes ADR-CK003-DQ006 from PROPOSED to ACCEPTED. It also explicitly states that DQ-006 remains OPEN because the JCS-discriminating fixture, evidence reachability, RI-RS boundary and ratification requirements remain outstanding.

**Forensic interpretation:** the repository contains an accepted decision artifact and the PR was merged, but the same PR text distinguishes the decision from the unratified closure verdict. No independent Chief Architect review/approval record was returned.

**Authority status:** `CLAIMED_ONLY` for Chief-Architect ratification of the closure verdict; `EVIDENCED` as a repository-recorded ADR decision only if the repository ADR merge rule is the applicable authority mechanism.

### AE-GH-005 — PR #17 / early DQ-006 closure assertion

**PR:** `#17 — CK003: close DQ-006 and map INV-009 to CONF-008`  
**Head SHA:** `d61c44293bcf80ddf4bca4d8050d2564db6abd5b`  
**Merge commit:** `5917fe94512d6089451f628b50dbcf935f807b15`  
**State:** CLOSED / MERGED  
**Created:** `2026-08-19T14:34:02Z`  
**Merged:** `2026-08-19T14:56:24Z`

The PR body reports DQ-006 closure evidence and a PASS result, but later DQ-006 reconciliation/audit evidence records material limitations and a blocked/unratified state.

**Forensic interpretation:** PR #17 proves that a closure assertion was merged. It does not prove that the asserted closure became durable normative authority. Later evidence must be handled as conflicting state/history rather than silently rewriting the earlier record.

**Authority status:** `CONFLICTED` at the closure-assertion level; no final normative closure authority established by this PR alone.

### AE-GH-006 — PR #27 / controlled final-closure gate

**PR:** `#27 — CK-003: enforce DQ-006 final closure execution gate`  
**Head SHA:** `ad7548cc6ff830ac8af68a1ec09bffd201f27e58`  
**Merge commit:** `1611effb8ccf5c9aa520160213718f6558c1e467`  
**State:** CLOSED / MERGED  
**Created:** `2026-08-21T08:19:25Z`  
**Merged:** `2026-08-21T14:48:19Z`  
**PR reviews:** NONE returned by GitHub connector.

The PR explicitly preserves DQ-006 as OPEN and requires four residuals: JCS-discriminating fixture, authoritative RI-RS boundary, reachable evidence, and Chief Architect ratification.

**Authority status:** `NON_AUTHORITY` as a closure act. It is an execution-control record that explicitly withholds closure authority pending R1–R4.

### AE-GH-007 — PR #34 / DQ-003 reconciliation

**PR:** `#34 — docs(dq-003): specification reconciliation control record`  
**Head SHA:** `0e89408beac178da79ef4ed0bc770de345ff4ae5`  
**Merge commit:** `74220d27f6af01f335fb1423886a51eb063f90f7`  
**State:** CLOSED / MERGED  
**Merged:** `2026-09-10T22:09:10Z`

The PR explicitly characterizes the change as a non-normative Custodian control record and states that DQ-003 remains OPEN and C4 remains NOT AUTHORIZED.

PR #43 subsequently reverted PR #34's merge commit.

**Authority status:** `REVERSED` as repository state; `NON_AUTHORITY` as a normative amendment because PR #34 explicitly disclaimed normative authorization.

### AE-GH-008 — PR #43 / DQ-003 revert

**PR:** `#43 — Revert "docs(dq-003): specification reconciliation control record"`  
**Head SHA:** `2b1ab54eac2185ab86e79cc7c794d55cb0c41dd7`  
**Merge commit / current main HEAD:** `71133de047c71e0bc1156d58c20396fe593ace70`  
**State:** CLOSED / MERGED  
**Created:** `2026-09-10T22:09:34Z`  
**Merged:** `2026-09-10T22:09:45Z`

The PR body is explicit: `Reverts Aura-IDToken/aura-specification#34`.

**Authority status:** `REVERSED` for the repository state introduced by #34.

**Boundary:** the revert is evidence of repository-state reversal. It is not, without a separate adjudication act, evidence that every semantic proposition in the reverted artifact is false or superseded.

## 4. Authority-path conclusions from this verification pass

### AP-01 — No independent Chief Architect approval was located for P0-1

The exact P0-1 closure artifact contains an acceptance claim, but its associated PR #31 remains OPEN and DRAFT, with no submitted reviews returned by the connector. The exact artifact is absent from current `main`.

**Status:** `CLAIMED_ONLY`.

### AP-02 — No independent Chief Architect approval was located for P0-2

P0-2 has the same pattern: explicit acceptance claim in branch artifact, open draft PR #32, no submitted reviews returned, exact artifact absent from current `main`.

**Status:** `CLAIMED_ONLY`.

### AP-03 — DQ-006 canonical-serialization decision and DQ-006 closure are separate authority subjects

PR #26 explicitly records the canonical serialization decision while simultaneously keeping the overall DQ-006 closure OPEN and requiring additional evidence and ratification.

**Status:** preserve as two separate authority records.

### AP-04 — Merge is insufficient to establish Chief Architect approval for normative protocol changes

PR #25, #26 and #27 were merged without submitted GitHub reviews returned by the connector. Their bodies use phrases such as "Chief Architect execution package" or define merge as a review boundary, but the current governance model also identifies Chief Architect approval as the final authority for major protocol changes.

**Status:** no independent Chief Architect approval act established by these PR records.

### AP-05 — PR #27 is an explicit non-closure control

PR #27 is particularly strong negative evidence against treating the DQ-006 PASS assertions as final closure. It explicitly preserves DQ-006 as OPEN and names Chief Architect ratification as residual R4.

**Status:** `NON_AUTHORITY` for closure.

### AP-06 — PR #34 was non-normative and then reverted

The PR itself disclaims normative authority, and PR #43 later reverts its repository state.

**Status:** `REVERSED` repository state + `NON_AUTHORITY` normative effect.

## 5. Updated authority matrix

| Subject | Primary evidence | Approval evidence located | Reachability on current main | Authority status |
|---|---|---:|---:|---|
| Governance hierarchy | `GOVERNANCE.md` | document declaration only | YES | `CLAIMED_ONLY` |
| ADR-001 document model | ADR-001 | NONE; status PROPOSED | YES | `PROPOSED` |
| DQ-006 canonical serialization decision | ADR-CK003-DQ006 + PR #26 | merge evidence; no separate Chief Architect review located | YES for ADR/current APS references | `CLAIMED_ONLY` / decision-recorded |
| P0-1 | PR #31 + branch artifact | NONE independently located | NO | `CLAIMED_ONLY` |
| P0-2 | PR #32 + branch artifact | NONE independently located | NO | `CLAIMED_ONLY` |
| DQ-006 early closure assertion | PR #17 | merge only | historical | `CONFLICTED` |
| DQ-006 final closure gate | PR #27 | explicit withholding of closure | historical/current controls | `NON_AUTHORITY` |
| DQ-003 reconciliation | PR #34 | explicitly non-normative | NO after revert | `REVERSED` / `NON_AUTHORITY` |
| DQ-003 revert | PR #43 | merge proves state reversal | YES | `REVERSED` |

## 6. Stage 07 status after this pass

```text
STAGE 06 semantic inventory
        ↓
STAGE 07 authority reconstruction
        ↓
PRIMARY GITHUB AUTHORITY PATH CHECK
        ↓
P0-1              CLAIMED_ONLY
P0-2              CLAIMED_ONLY
DQ-006 decision   DECISION-RECORDED / RATIFICATION NOT ESTABLISHED
DQ-006 closure    CONFLICTED / NOT FINALLY RATIFIED
DQ-003 #34        NON_AUTHORITY + REVERSED
DQ-003 #43        REPOSITORY-STATE REVERSION EVIDENCED
        ↓
STAGE 07 REMAINS OPEN
```

## 7. Remaining mechanical work

The next Stage 07 pass should continue without semantic redesign:

1. map every Stage 06 authority-claiming delta to its exact PR/commit;
2. locate explicit approval/ratification acts, including non-PR governance records where present;
3. verify exact branch reachability of each claimed authority artifact;
4. distinguish merge acceptance from Chief Architect approval;
5. record all conflicting closure assertions without selecting a winner;
6. only after the complete authority matrix is closed, proceed to Stage 08 — Revert / Supersession / Conflict Register.

**No protocol semantics are changed by this artifact.**
