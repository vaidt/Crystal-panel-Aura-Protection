# AURA — STAGE 07 AUTHORITY EVIDENCE REGISTER v1.2

**Artifact:** `14_FORENSICS/07_AUTHORITY_EVIDENCE_REGISTER_v1.2_MECHANICAL_EXTENSION.md`
**Source repository:** `Aura-IDToken/aura-specification`
**Forensic repository:** `vaidt/Crystal-panel-Aura-Protection`
**Stage:** 07 — Authority Evidence Register
**Parent:** `07_AUTHORITY_EVIDENCE_REGISTER_v1.1_GITHUB_VERIFICATION.md`
**Status:** OPEN — MECHANICAL AUTHORITY-CLAIM EXTENSION
**Authority:** NONE
**Normative effect:** NONE

## 1. Scope

This extension continues Stage 07 mechanically. It does not redesign AURA, reconcile disputed semantics, or promote any artifact to authority.

The purpose is to cover additional Stage 06 semantic deltas that either:

1. make an explicit authority/canonical/frozen claim; or
2. establish a governance mechanism whose own authority is relevant to later claims.

The forensic test remains:

```text
SEMANTIC DELTA
  ↓
CLAIMED AUTHORITY
  ↓
PRIMARY COMMIT / PR
  ↓
ACTOR
  ↓
ACT / APPROVAL
  ↓
REACHABILITY
  ↓
CONFLICT / REVERT / SUPERSESSION
  ↓
AUTHORITY STATUS
```

No status is promoted solely from wording such as `canonical`, `frozen`, `accepted`, `Chief Architect`, or `merged`.

## 2. Additional authority-path records

### AE-GH-009 — Initial canonical repository bootstrap / PR #5

**Semantic delta:** repository-wide specification structure and initial authority declarations.

**Primary commit:** `93f677fe34bf3f3fe0e8abffd6c8fdfd92b7958f`

**Commit message:** `Merge pull request #5 from AuraIDToken/copilot/implement-aura-protocol-specifications` / `feat: build canonical repository structure for aura-specification`

**Observed content:** the commit introduces the repository governance documents, APS Markdown structure, invariant registry, conformance stubs, traceability model, ADR/RFC templates and changelog. The changelog describes the Markdown APS corpus as canonical and the initial source imports as authoritative text files; it also records `AURA Constitution v1.0 (FROZEN)`.

**Actor:** commit author/PR path is Copilot; merge commit is repository history. The commit record itself is not an independent Chief Architect approval act.

**Act / approval:** repository bootstrap / merge. No separate Chief Architect approval record was established in this pass for the claims that the imported corpus was authoritative or the Constitution was FROZEN.

**Scope:** initial repository structure, governance scaffolding and historical source import.

**Reachability:** commit is part of the surviving repository history and its introduced structure is represented on the current lineage; exact per-artifact reachability must remain artifact-specific.

**Signature / verification:** GitHub commit provenance available. This does not establish a governance signature for each embedded authority declaration.

**Conflicting evidence:** later governance/recovery records distinguish repository presence from authority and document unresolved authority questions. The current APS corpus also contains DRAFT statuses.

**Supersession / revert:** no global supersession established by this record. Individual imported artifacts may have later semantic deltas.

**Authority status:** `CLAIMED_ONLY` for the embedded canonical/authoritative/frozen declarations; `EVIDENCED` only for the repository bootstrap event itself.

**Reason:** the commit proves that the structure and declarations entered Git history. It does not independently prove the competent approval act required to establish every authority claim.

### AE-GH-010 — Terminology normalization / commit e639d9c6

**Semantic delta:** `Wersja:` → `Version:` in `docs/APS.md` and `docs/CONSTITUTION.md`; no substantive protocol rule changed.

**Primary commit:** `e639d9c699204bad06f0cb5a135b380c1f837b9c`

**Date:** `2026-07-23T19:20:27Z`

**Actor:** Copilot author; `web-flow` committer.

**Act / approval:** documentation normalization only. No approval act is claimed by the commit itself.

**Scope:** presentation/header terminology in two historical documents.

**Reachability:** branch/commit provenance established; authority reachability is not material because this delta is non-normative documentation normalization.

**Signature / verification:** GitHub reports valid signature/provenance for this commit lineage as previously recorded.

**Conflicting evidence:** none indicating a protocol-semantic change in this delta.

**Supersession / revert:** none established.

**Authority status:** `NON_AUTHORITY`.

**Reason:** the diff changes only a language label in version headers; it does not exercise protocol authority.

### AE-GH-011 — RFC template correction / commit 176f7abb

**Semantic delta:** spelling correction `summarised` → `summarized` in `templates/RFC_TEMPLATE.md`.

**Primary commit:** `176f7abb3659ff34855d5693d89317b5dfe14290`

**Date:** `2026-07-23T21:03:41Z`

**Actor:** Copilot author; `web-flow` committer.

**Act / approval:** formatting/spelling correction only.

**Scope:** RFC authoring template.

**Reachability:** commit provenance established; no protocol authority asserted.

**Signature / verification:** GitHub provenance available.

**Conflicting evidence:** none.

**Supersession / revert:** none established.

**Authority status:** `NON_AUTHORITY`.

**Reason:** no protocol semantic or governance authority is exercised by a spelling correction.

### AE-GH-012 — ARC/SPEC governance-structure correction / commit 10242325

**Semantic delta:** changes ARC/SPEC workflow and mapping structure; removes placeholder ARC→SPEC mapping and makes mapping reserved until SPEC-001 approval; adds explicit Issue → Branch → PR → Review → Merge cycle.

**Primary commit:** `102423256e33ad3dea54461f692819aeebaa0700`

**Commit message:** `docs(spec): apply Chief Architect corrections to ARC/SPEC templates and mapping structure`

**Date:** `2026-08-02T18:03:45Z`

**Actor:** Aura-IDToken author and committer.

**Act / approval:** commit message attributes the changes to `Chief Architect corrections`, but the inspected primary commit contains no separate approval/signature record establishing the underlying Chief Architect act.

**Scope:** documentation architecture, ARC/SPEC mapping lifecycle and templates.

**Reachability:** commit is an identified historical branch/commit node; exact current-main reachability of every changed representation is separate from the existence of the act.

**Signature / verification:** Git provenance available; no independent governance approval artifact located in this pass.

**Conflicting evidence:** the changed mapping itself says mapping will be established when SPEC-001 is approved, demonstrating that the commit does not itself establish SPEC-001 approval.

**Supersession / revert:** no explicit supersession/revert located for this semantic delta.

**Authority status:** `CLAIMED_ONLY` for the attributed Chief Architect correction; `EVIDENCED` as a repository documentation change.

**Reason:** the commit establishes that a correction attributed to the Chief Architect was recorded, but not the independent approval act or full authority scope.

### AE-GH-013 — Documentation normalization audit / commit 5f91167d

**Semantic delta:** broad correction of presentation errors across APS files and README; additionally adds an APS-001 README row and a related-invariant mapping entry.

**Primary commit:** `5f91167d0611dc91a25ebd6e1ddc3d4ce41175ca`

**Date:** `2026-07-23T19:26:02Z`

**Actor:** Copilot author; `web-flow` committer.

**Act / approval:** documentation repair. No governance approval act is recorded in the commit.

**Scope:** documentation presentation and traceability labels. The APS-001 row explicitly states the document was referenced but not yet created.

**Reachability:** commit provenance established; exact current artifact reachability is subordinate to later branch lineage.

**Signature / verification:** GitHub provenance available.

**Conflicting evidence:** later governance records distinguish document declarations from authority acts; current APS documents remain DRAFT where applicable.

**Supersession / revert:** no explicit supersession/revert established.

**Authority status:** `NON_AUTHORITY`.

**Reason:** the semantic effect is documentation normalization; the commit does not itself approve or freeze protocol content.

### AE-GH-014 — APS-200 recovery control / commit 327dacda

**Semantic delta:** specification recovery/reconciliation control record concerning APS-200 §§6–§10, §8 references, event registry, session semantics and chain-link documentation.

**Primary commit:** `327dacdab83ad33fd5ffafe4300b793a58bb211e`

**Commit message:** `docs(reconciliation): add APS-200 specification recovery control record`

**Act / approval:** the record explicitly classifies itself as a read-only recovery audit, `IN PROGRESS`, with no normative or implementation remediation. It surfaces Custodian inputs but does not execute them.

**Scope:** specification/reference integrity recovery only.

**Reachability:** branch-local forensic evidence; exact current-main reachability is not required to classify the act because the record explicitly disclaims authority.

**Signature / verification:** Git provenance available.

**Conflicting evidence:** the record contains statements such as current `origin/main` being the authoritative recovery baseline, but its own scope says it does not create normative remediation. Such wording is treated as a scoped audit conclusion, not a new authority grant.

**Supersession / revert:** no authority supersession established.

**Authority status:** `NON_AUTHORITY`.

**Reason:** explicit read-only/recovery boundary; it identifies decisions required elsewhere rather than deciding them.

### AE-GH-015 — Q1 Chief Architect approval/delegation preparation / commit 6002c491

**Semantic delta:** creation of a formal approval/delegation record intended to establish bounded Q1 jurisdiction.

**Primary commit:** `6002c4910c1eefd056aff77229707904cffb3d30`

**Commit message:** `govern(Q1): place Chief Architect approval/delegation record (unexecuted)`

**Act / approval:** explicitly **unexecuted**. Section 17 approval fields remain placeholders. The commit states `Approval status: PENDING`, `Q1 Jurisdiction: NOT ESTABLISHED`, and that execution is reserved to the competent authority.

**Actor:** repository author/committer records the preparation; the intended competent authority is the Chief Architect, but no executed authority act is present.

**Scope:** preparation of a bounded delegation concerning designation of the Q1 Decision Surface.

**Reachability:** branch-local preparation artifact as recorded by the commit.

**Signature / verification:** Git provenance available; governance signature absent because the approval record is unexecuted.

**Conflicting evidence:** none needed to classify the act; the artifact itself explicitly prevents inference of jurisdiction from repository placement.

**Supersession / revert:** no supersession/revert of the approval act established.

**Authority status:** `PROPOSED` / `NON_AUTHORITY`.

**Reason:** the artifact is an approval instrument, not an executed approval act. The commit explicitly says repository placement does not exercise jurisdiction.

### AE-GH-016 — Q1 Scope Bridge preparation / commit eb263ce3

**Semantic delta:** creation of bounded Chief Architect → Protocol Custodian Q1 jurisdiction instrument.

**Primary commit:** `eb263ce3f325fd14213c49fff1ab2da3453c426f`

**Commit message:** `govern(Q1): place Chief Architect -> Custodian Scope Bridge (non-binding)`

**Act / approval:** explicitly none. The artifact states `DRAFT — NON-BINDING PREPARATION`, `Authority exercised by this document: NONE`, and `Delegation effective: NO — pending competent approval`.

**Actor:** repository authoring activity; the proposed delegator is Chief Architect and proposed delegate is Protocol Custodian, but neither role execution is evidenced by this commit.

**Scope:** designation of a Q1 Decision Surface only; explicitly excludes substantive Decision A/B, C-1/C-2, ARI semantics, implementation and conformance.

**Reachability:** branch-local preparation record.

**Signature / verification:** Git provenance available; no executed approval/signature record.

**Conflicting evidence:** none required; the artifact itself establishes its non-binding state.

**Supersession / revert:** none established.

**Authority status:** `NON_AUTHORITY`.

**Reason:** the commit expressly states that it does not exercise the jurisdiction it proposes to establish.

### AE-GH-017 — BC-02 / BC-02.1 Custodian Decision Package A/B / commit dd11311b

**Semantic delta:** normalization and routing of BC-02 / BC-02.1 unresolved governance questions into a formal two-decision package.

**Primary commit:** `dd11311bff7c19ace8cddc002402ce2e04a3c3c4`

**Commit message:** `BC-02 / BC-02.1: Custodian Decision Package A/B v1 — prepared, not resolved`

**Act / approval:** explicit preparation only. The commit states `Authority: NONE`, `Conformance authority: NONE`, `Execution authority: NONE`; Decision A and B are `NOT resolved`.

**Actor:** Claude in architectural/conformance audit role; the document explicitly says Claude is neither Protocol Custodian nor Independent Reviewer and entered no key.

**Scope:** decision preparation and routing to Protocol Custodian.

**Reachability:** branch-local according to the related Q1 approval-preparation record; exact branch lineage remains separately recorded in Stage 05/06.

**Signature / verification:** Git provenance available; no Custodian decision act or signature.

**Conflicting evidence:** package contains candidate dispositions but explicitly selects none and states the A/B labels are packaging only.

**Supersession / revert:** no decision supersession established.

**Authority status:** `NON_AUTHORITY`.

**Reason:** explicit no-authority/no-resolution boundary.

## 3. Authority-path conclusions added by v1.2

### AP-07 — Initial repository canonical/frozen declarations remain claims unless their competent act is separately evidenced

The bootstrap commit establishes the repository structure and records canonical/authoritative/frozen language in its changelog. That proves the declarations entered history, not that the underlying approval act is independently evidenced.

**Status:** `CLAIMED_ONLY` for those declarations.

### AP-08 — Documentation-only deltas do not create protocol authority

The terminology, spelling and documentation-normalization commits are repository events but do not contain substantive protocol approval acts.

**Status:** `NON_AUTHORITY`.

### AP-09 — Chief Architect attribution in a commit message is not itself the approval act

Commit `10242325...` attributes corrections to the Chief Architect, but the primary commit does not contain a separate executed approval record.

**Status:** `CLAIMED_ONLY` for the attributed authority; repository change itself is evidenced.

### AP-10 — Recovery audits and decision-preparation packages explicitly withhold authority

The APS-200 recovery record, Q1 Scope Bridge, Q1 approval/delegation record, and BC-02 A/B package all contain explicit non-authority or unexecuted boundaries.

**Status:** `NON_AUTHORITY` / `PROPOSED`, as applicable.

### AP-11 — Q1 jurisdiction is not established by preparation artifacts

The Q1 approval/delegation record explicitly leaves approval pending and Q1 jurisdiction `NOT ESTABLISHED`. The Scope Bridge separately states that it becomes binding only through competent approval.

**Status:** no Q1 authority established by these commits.

## 4. Extended Stage 07 matrix

| Subject | Primary evidence | Act/approval located | Reachability | Authority status |
|---|---|---:|---|---|
| Initial canonical repository declarations | `93f677fe...` | NO independent approval located | historical/current lineage | `CLAIMED_ONLY` |
| Terminology normalization | `e639d9c6...` | N/A | historical | `NON_AUTHORITY` |
| RFC template spelling correction | `176f7abb...` | N/A | historical | `NON_AUTHORITY` |
| ARC/SPEC structure correction | `10242325...` | No independent approval act | historical branch/commit | `CLAIMED_ONLY` |
| Documentation normalization | `5f91167d...` | N/A | historical | `NON_AUTHORITY` |
| APS-200 recovery control | `327dacda...` | Explicitly none | branch-local | `NON_AUTHORITY` |
| Q1 approval/delegation instrument | `6002c491...` | **UNEXECUTED** | branch-local | `PROPOSED / NON_AUTHORITY` |
| Q1 Scope Bridge | `eb263ce3...` | **NONE** | branch-local | `NON_AUTHORITY` |
| BC-02 A/B package | `dd11311b...` | **NONE** | branch-local | `NON_AUTHORITY` |
| ADR-001 | current ADR | NONE; PROPOSED | current main | `PROPOSED` |
| DQ-006 canonical serialization decision | ADR + PR #26 | merge/ADR record; separate Chief Architect ratification not located | current main references | `CLAIMED_ONLY / DECISION-RECORDED` |
| P0-1 | PR #31 | NONE independently located | NO exact artifact on main | `CLAIMED_ONLY` |
| P0-2 | PR #32 | NONE independently located | NO exact artifact on main | `CLAIMED_ONLY` |
| DQ-006 closure assertion | PR #17 + later controls | no final ratification | historical/conflicted | `CONFLICTED` |
| DQ-003 reconciliation | PR #34 + #43 | non-normative; reverted | NO after revert | `REVERSED / NON_AUTHORITY` |

## 5. Stage 07 status

This extension materially expands the authority inventory but does **not** close Stage 07.

```text
Stage 06 semantic deltas
        ↓
Stage 07 authority claims
        ↓
primary GitHub evidence
        ↓
additional authority-claim records
        ↓
NO COMPLETE AUTHORITY MATRIX YET
        ↓
STAGE 07 = OPEN
```

## 6. Remaining mechanical work before Stage 08

1. Continue mapping **every remaining Stage 06 authority-claiming delta** to a primary PR/commit or explicit absence-of-act record.
2. For each claimed approval, search for the actual approval/ratification record, not only attribution in commit text.
3. Verify current-main reachability of each authority-bearing artifact where reachability is part of the claim.
4. Preserve `CLAIMED_ONLY`, `PROPOSED`, `NON_AUTHORITY`, `CONFLICTED`, and `REVERSED` states without normalization into a single verdict.
5. Do not open Stage 08 until the Stage 06 authority-claim set has complete Stage 07 coverage.
