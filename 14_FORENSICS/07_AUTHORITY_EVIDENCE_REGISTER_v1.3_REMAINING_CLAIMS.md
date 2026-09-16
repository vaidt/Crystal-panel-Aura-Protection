# AURA — STAGE 07 AUTHORITY EVIDENCE REGISTER v1.3

**Source repository:** `Aura-IDToken/aura-specification`
**Forensic repository:** `vaidt/Crystal-panel-Aura-Protection`
**Stage:** 07 — Authority Evidence Register
**Parent:** `07_AUTHORITY_EVIDENCE_REGISTER_v1.2_MECHANICAL_EXTENSION.md`
**Status:** OPEN — REMAINING AUTHORITY-CLAIM PASS
**Authority:** NONE
**Normative effect:** NONE

## 1. Scope

This pass continues the mechanical authority reconstruction over the remaining Stage 06 subjects that can reasonably be authority-claiming or authority-relevant.

No semantic proposition is resolved here. A repository event, document status, commit message, branch name, or embedded approval statement is not treated as an approval act unless the corresponding act is independently evidenced.

The control sequence remains:

```text
SEMANTIC DELTA
  ↓
CLAIMED AUTHORITY
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

## 2. AE-GH-018 — ADR-001 duplicate representation / authority conflict

**Subject:** ADR-001 Document Model.

Two distinct repository representations exist on current `main`:

1. `adrs/ADR-001_DOCUMENT_MODEL.md` — blob `66083e286a2fc33e70ccab4d1df6015ec0be65fd`, Status `PROPOSED`.
2. `docs/adr/001-document-model.md` — blob `340ed584082baf5353ce0496034484ab6379ac45`, Status `DRAFT`.

Both identify ADR-001 and date 2026-08-02. The `adrs/` representation explicitly requires Protocol Custodian approval and says approval is recorded by an `Accepted-by` entry plus merge. It currently remains `PROPOSED`. The `docs/adr/` representation likewise remains `DRAFT` and requires explicit approval before acceptance.

**Act / approval:** no executed Protocol Custodian approval located in either current representation.

**Reachability:** both representations are reachable from current `main`.

**Conflict:** duplicate representations have materially different status values (`PROPOSED` vs `DRAFT`) and different textual detail. This is a document-governance conflict, not evidence that either has been approved.

**Supersession:** no explicit supersession relation established.

**Authority status:** `CONFLICTED` + `PROPOSED` / `DRAFT`; no approval established.

**Evidence:** current `adrs/ADR-001_DOCUMENT_MODEL.md` explicitly states `Status: PROPOSED` and requires Protocol Custodian approval. fileciteturn344file0L2-L6 Current `docs/adr/001-document-model.md` independently states `Status: DRAFT` and requires acceptance conditions. fileciteturn343file0L2-L6

## 3. AE-GH-019 — SPEC/ARC authority model introduced by ADR-001 remains unexecuted

**Subject:** proposed document architecture authority model.

ADR-001 proposes Protocol Custodian approval for SPECs, Architecture Board ownership/approval for ARC baselines, and Release Authority ownership for APS publication. These are propositions contained inside a still-unapproved ADR.

**Act / approval:** none established. The current ADR explicitly remains `PROPOSED` / `DRAFT` and requires approval before acceptance.

**Reachability:** ADR representations are current-main reachable, but their proposed authority model is not thereby enacted.

**Conflict:** current `GOVERNANCE.md` assigns Chief Architect final/sole approval for certain major governance transitions, while ADR-001 proposes a more granular authority model. No authoritative act resolving the relationship between these models was located in this pass.

**Authority status:** `PROPOSED` / `CONFLICTED` as an unresolved governance-model relationship.

## 4. AE-GH-020 — Initial APS/Constitution v1.0 Active corpus

**Subject:** `copilot/aura-specification` HEAD `b08433bd245923a4746802cc7db2b5ef394d2ac3`.

**Semantic delta:** introduced `docs/APS.md` and `docs/CONSTITUTION.md` as `v1.0.0`, `Status: Active`, and presented them as the comprehensive documentation corpus.

**Act / approval:** repository commit/PR integration is evidenced; no separate approval act establishing these documents as the final authoritative Constitution/APS was located in the authority evidence examined.

**Reachability:** historical branch/commit; current main contains later APS/Constitution representations but not a basis for treating the historical `Active` declaration as independently ratified.

**Conflict:** later current-main governance/specification artifacts contain DRAFT statuses and explicit authority gaps. The documentation-normalization audit also records self-declared authority without external ratification evidence.

**Authority status:** `CLAIMED_ONLY` for the embedded `Active`/canonical authority claims; repository introduction itself is `EVIDENCED`.

## 5. AE-GH-021 — SPEC-002 draft tightening / v0.3

**Subject:** `copilot/spec-002-v03-draft` HEAD `62d2d6bcc1a46dd505ebfe400ad01fa3c6a25bf0`.

**Semantic delta:** expands SPEC-002 draft provenance/decision-contract material and increments the document to `0.3-DRAFT`.

**Act / approval:** no approval act; document remains explicitly draft work.

**Reachability:** branch-local historical artifact.

**Conflict:** later SPEC-002 artifacts continue to distinguish draft from approved constitutional artifact work.

**Authority status:** `PROPOSED` / `NON_AUTHORITY` for normative adoption.

## 6. AE-GH-022 — SPEC-002 constitution artifact contract final-formatting pass

**Subject:** `copilot/spec-002-draft-constitution-artifact-contract` HEAD `0dfcc8b444c53f50465798ac0af73c3c661ef754`.

**Semantic delta:** formatting/finalization of the SPEC-002 draft contract.

**Act / approval:** none. The artifact explicitly states `DRAFT ONLY / SPECIFICATION WORK` and prohibits use for implementation, generation, registration or freezing until blocking decisions are approved.

**Reachability:** historical branch artifact.

**Authority status:** `PROPOSED` / `NON_AUTHORITY`.

## 7. AE-GH-023 — Specification recovery APS-200 authority assertion

**Subject:** `specification-recovery/reconciliation-aps200` HEAD `327dacdab83ad33fd5ffafe4300b793a58bb211e`.

**Act / approval:** none. The commit creates a read-only recovery control record and explicitly states `IN PROGRESS`, no normative remediation and no DQ-003 closure authorization.

**Reachability:** branch-local.

**Important boundary:** the document calls `origin/main` APS-200 the authoritative recovery baseline for the recovery exercise. That is a scoped audit conclusion about the baseline, not a new governance approval act.

**Authority status:** `NON_AUTHORITY`.

The primary commit states the read-only scope and explicitly lists DQ-003 closure and implementation actions as unauthorized. fileciteturn328file0L3-L7

## 8. AE-GH-024 — Documentation cleanup commit 5f91167d

**Subject:** broad APS documentation cleanup.

The commit corrects formatting, terminology, a traceability relation for CONF-009 and README inventory information. It does not contain an approval act.

**Authority status:** `NON_AUTHORITY`.

Primary diff shows the changes are editorial/traceability corrections and that the README explicitly records APS-001 as referenced but not yet created. fileciteturn325file0L3-L7

## 9. AE-GH-025 — Q1 authority preparation remains unexecuted

**Subject:** Q1 Scope Bridge and Approval/Delegation Record.

The approval/delegation record commit explicitly describes itself as unexecuted. Its Section 17 approval fields remain placeholders, approval status is `PENDING`, and Q1 jurisdiction is `NOT ESTABLISHED`. fileciteturn326file0L3-L4

The related Scope Bridge is present on current `main`, but its existence is not equivalent to executed delegation. The Q1 control chain therefore remains:

```text
Scope Bridge prepared
        ↓
Approval instrument prepared
        ↓
Approval act NOT evidenced
        ↓
Q1 jurisdiction NOT established
        ↓
Selection act NOT evidenced
```

**Authority status:** `NON_AUTHORITY` for the preparation artifacts; Q1 jurisdiction `NOT ESTABLISHED`.

## 10. AE-GH-026 — BC-02 A/B package is decision preparation, not decision authority

The BC-02 package is explicitly a prepared-not-resolved package. It identifies candidate decision surfaces but does not exercise Custodian authority.

The Q1 approval preparation record independently records both candidate package identities as branch-local and explicitly says neither is selected. fileciteturn326file0L3-L4

**Act / approval:** none.

**Reachability:** package identities are branch-local; the Q1 approval record states they are not reachable from `origin/main` at that point.

**Authority status:** `NON_AUTHORITY`.

## 11. AE-GH-027 — ARC/SPEC mapping authority remains conditional

Commit `102423256e33ad3dea54461f692819aeebaa0700` is attributed in its message to Chief Architect corrections. Its actual semantic change reserves the ARC→SPEC mapping and states that mapping will be established when SPEC-001 is approved. fileciteturn330file0L3-L27

**Act / approval:** no independent approval act located in the commit.

**Reachability:** historical commit; the exact mapping state is subject to later changes.

**Authority status:** `CLAIMED_ONLY` for the attribution; the conditional mapping state is `EVIDENCED`.

## 12. AE-GH-028 — Bootstrap canonicality claim remains authority-unproven

The initial repository bootstrap commit `93f677fe...` introduced governance scaffolding, APS Markdown corpus, invariant/conformance structures and a changelog that described the imported source documents as authoritative and Constitution v1.0 as FROZEN. fileciteturn329file0L3-L7

**Act / approval:** merge/bootstrap evidenced; separate approval act for each authority declaration not located.

**Reachability:** bootstrap content entered repository history and is represented in subsequent lineage, but individual artifact reachability must remain artifact-specific.

**Authority status:** `CLAIMED_ONLY` for embedded canonical/authoritative/frozen declarations.

## 13. AE-GH-029 — Current governance hierarchy itself is a declared control, not an independently located ratification act

Current `GOVERNANCE.md` declares Chief Architect final/sole approval authority for specified major transitions and defines the ADR rule that merging a PR accepts an ADR. The document is therefore primary evidence of the repository's declared governance mechanism.

However, no separate ratification artifact for GOV-001 itself was located in the present pass.

**Authority status:** `CLAIMED_ONLY` for the declaration as an independently ratified authority source; `EVIDENCED` as the current repository governance text.

This distinction is consistent with the Stage 07 GitHub verification rule that merge proves repository-state transition, while a separate approval act is required where governance demands one. fileciteturn334file0L2-L6

## 14. Mechanical coverage result

The authority-claiming subjects identified in the Stage 06 closure and subsequent Stage 07 passes are now mapped into explicit authority records across v1.0–v1.3, including:

- bootstrap canonical/authoritative/frozen claims;
- APS/Constitution Active claims;
- ARC/SPEC authority-model corrections;
- ADR-001 document-model authority;
- DQ-002 closure assertions and audit contradictions;
- DQ-006 decision vs closure authority;
- P0-1 and P0-2 acceptance claims;
- DQ-003 reconciliation and revert;
- specification recovery claims;
- Q1 jurisdiction / delegation preparation;
- BC-02 decision packages;
- SPEC-002 draft authority claims;
- current governance hierarchy.

No item is marked authoritative merely because its document says `ACCEPTED`, `APPROVED`, `FROZEN`, `CANONICAL`, or `Chief Architect`.

## 15. Stage 07 closure gate

Stage 07 remains **OPEN**.

The current mechanical conclusion is:

```text
Authority act independently evidenced
        ↓
limited / artifact-specific

Authority merely claimed in artifact
        ↓
multiple subjects remain CLAIMED_ONLY

Explicit non-authority / unexecuted
        ↓
multiple subjects classified NON_AUTHORITY / PROPOSED

Contradictory authority evidence
        ↓
ADR-001 representation conflict
DQ-002 closure history
other historical status conflicts
        ↓
CONFLICTED / UNRESOLVED
```

### Required before Stage 08

1. Verify whether any external/non-file governance evidence exists for the remaining `CLAIMED_ONLY` records.
2. Verify complete PR review/approval evidence for every normative authority claim where the governing process requires it.
3. Resolve the ADR-001 duplicate-representation/status conflict through evidence, not inference.
4. Confirm whether any executed Chief Architect or Protocol Custodian acts exist outside the repository files already examined.
5. Maintain `CLAIMED_ONLY`, `PROPOSED`, `NON_AUTHORITY`, `CONFLICTED`, and `REVERSED` states until such evidence is found.
6. Only after the authority matrix is demonstrably complete should Stage 07 be marked CLOSED and Stage 08 begin.

**No Stage 08 semantic/supersession adjudication is performed by this artifact.**
