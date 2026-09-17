# AURA — STAGE 06 → STAGE 07 AUTHORITY CLAIM COVERAGE v1.0

**Source repository:** `Aura-IDToken/aura-specification`
**Forensic repository:** `vaidt/Crystal-panel-Aura-Protection`
**Purpose:** mechanically demonstrate that every Stage 06 semantic-delta record has a Stage 07 authority/evidence disposition, while isolating already-verified P0/DQ/BC-02 subjects from the remaining pass.

**Status:** OPEN — COVERAGE PASS
**Authority:** NONE
**Normative effect:** NONE

## 1. Control rule

This artifact does not redesign AURA and does not adjudicate protocol truth.

It answers only:

> Has each Stage 06 semantic-delta subject been represented in Stage 07 with an authority/evidence disposition, and which subjects still require independent authority evidence?

The governing distinction is:

```text
Stage 06: WHAT CHANGED
        ↓
Stage 07: WHAT AUTHORITY EVIDENCE EXISTS
        ↓
Stage 07 closure: ONLY AFTER COVERAGE + EVIDENCE GATE
```

A Stage 06 record classified `DOC`, `AUDIT`, or explicitly non-authority does not require a fabricated approval search result. Its Stage 07 record must instead explicitly state `NON_AUTHORITY` or equivalent and the evidence basis for that conclusion.

## 2. Coverage status vocabulary

- `MAPPED — NON_AUTHORITY`: Stage 06 content explicitly creates no authority or is editorial/audit-only.
- `MAPPED — CLAIMED_ONLY`: an authority-bearing claim exists, but independent approval/ratification has not been evidenced.
- `MAPPED — CONFLICTED`: materially conflicting authority/status evidence exists.
- `MAPPED — REVERSED`: repository-state reversal is evidenced; underlying proposition is not adjudicated by the revert itself.
- `MAPPED — PROPOSED`: authority model/instrument remains draft or unexecuted.
- `MAPPED — ALREADY VERIFIED`: subject belongs to P0/DQ/BC-02 authority work already covered; no additional deepening is authorized by this pass.
- `REQUIRES EVIDENCE CHECK`: Stage 06 authority-bearing content has not yet been reduced to an explicit Stage 07 evidence record.

## 3. Mechanical coverage matrix

| Stage 06 | Subject | Stage 07 disposition | Further pass |
|---|---|---|---|
| SD-001 | Initial specification repository bootstrap | MAPPED — CLAIMED_ONLY | Evidence absence/approval path only |
| SD-002 | Polish/English terminology normalization | MAPPED — NON_AUTHORITY | None |
| SD-003 | ARC/SPEC synchronization structure | MAPPED — CLAIMED_ONLY | Evidence absence/approval path only |
| SD-004 | DQ-002 hash-domain correction | MAPPED — ALREADY VERIFIED | No deepening |
| SD-005 | DQ-003 version-binding fixture | MAPPED — NON_AUTHORITY / DQ evidence | No deepening |
| SD-006 | CROSS-LANGUAGE-002 manifest | MAPPED — ALREADY VERIFIED | No deepening |
| SD-007 | DQ-006 closure line | MAPPED — ALREADY VERIFIED | No deepening |
| SD-008 | DQ-006 reconciliation | MAPPED — ALREADY VERIFIED | No deepening |
| SD-009 | DQ-006 final-closure execution line | MAPPED — ALREADY VERIFIED | No deepening |
| SD-010 | DQ-006 specification integration | MAPPED — ALREADY VERIFIED | No deepening |
| SD-011 | APS-200 specification recovery | MAPPED — NON_AUTHORITY | None |
| SD-012 | Documentation normalization audit | MAPPED — NON_AUTHORITY | None |
| SD-013 | Protocol handover assessment | MAPPED — NON_AUTHORITY | None |
| SD-014 | Q1 Scope Bridge preparation | MAPPED — PROPOSED / NON_AUTHORITY | Evidence of executed delegation only |
| SD-015 | BC-02 / BC-02.1 decision package | MAPPED — ALREADY VERIFIED | No deepening |
| SD-016 | BC-02 review surface | MAPPED — ALREADY VERIFIED | No deepening |
| SD-017 | Documentation normalization control baseline | MAPPED — NON_AUTHORITY | None |
| SD-018 | CK003 closure-workspace merge | MAPPED — NON_AUTHORITY / aggregation | None |
| SD-019 | DQ-006 INV-009 closure merge | MAPPED — ALREADY VERIFIED | No deepening |
| SD-020 | DQ-002 final closure assertion | MAPPED — ALREADY VERIFIED | No deepening |
| SD-021 | DQ-006 reconciliation against DQ-002 | MAPPED — ALREADY VERIFIED | No deepening |
| SD-022 | CROSS-LANGUAGE-002 execution/merge state | MAPPED — ALREADY VERIFIED | No deepening |
| SD-023 | DQ-002 forensic closure audit rev.2 | MAPPED — ALREADY VERIFIED | No deepening |
| SD-024 | DQ-002 final-closure revalidation | MAPPED — ALREADY VERIFIED | No deepening |
| SD-025 | DQ-003 read-only execution attempt | MAPPED — NON_AUTHORITY | No deepening |
| SD-026 | DQ-006 closure package supersession | MAPPED — ALREADY VERIFIED | No deepening |
| SD-027 | DQ-006 closure reconciliation branch | MAPPED — ALREADY VERIFIED | No deepening |
| SD-028 | GOV-001 DQ-006 closure traceability | MAPPED — ALREADY VERIFIED | No deepening |
| SD-029 | Q1 Chief Architect approval/delegation record | MAPPED — PROPOSED / NON_AUTHORITY | Evidence of executed act only |
| SD-030 | RI-RS P01 controlled handoff package | MAPPED — ALREADY VERIFIED | No deepening |
| SD-031 | Completion/conformance package | MAPPED — NON_AUTHORITY / completion planning | None unless explicit approval claim found |
| SD-032 | Early APS/Constitution v1.0 Active corpus | MAPPED — CLAIMED_ONLY | Independent approval/ratification search |
| SD-033 | APS documentation cleanup merge | MAPPED — NON_AUTHORITY | None |
| SD-034 | AuraProtocol migration-status documentation | MAPPED — NON_AUTHORITY | No transfer authority inferred |
| SD-035 | Identical migration README introduction | MAPPED — NON_AUTHORITY | No transfer authority inferred |
| SD-036 | SPEC-002 v0.3-DRAFT tightening | MAPPED — PROPOSED / NON_AUTHORITY | None unless approval claim found |
| SD-037 | CODEOWNERS ownership mutation | MAPPED — NON_AUTHORITY | None |
| SD-038 | README migration information removal | MAPPED — NON_AUTHORITY | None |
| SD-039 | RFC template spelling correction | MAPPED — NON_AUTHORITY | None |
| SD-040 | SPEC-002 draft formatting normalization | MAPPED — NON_AUTHORITY | None |
| SD-041 | SPEC-002 traceability row correction | MAPPED — NON_AUTHORITY | None |
| SD-042 | SPEC-002 redundant-phrasing correction | MAPPED — NON_AUTHORITY | None |
| SD-043 | Initial CODEOWNERS governance declaration | MAPPED — NON_AUTHORITY | None unless governance act explicitly claims substantive authority |
| SD-044 | CONF-003 digest-input reference rebind | MAPPED — NON_AUTHORITY | None |
| SD-045 | ADR-001 committed-SHA documentation update | MAPPED — CONFLICTED SUBJECT VIA ADR-001 | Verify duplicate ADR status/approval path |
| SD-046 | DQ-003 entry-point baseline | MAPPED — NON_AUTHORITY | No deepening |
| SD-047 | DQ-003 Custodian JCS surface decision | MAPPED — ALREADY VERIFIED | No deepening |
| SD-048 | DQ-003 specification-reconciliation merge | MAPPED — ALREADY VERIFIED | No deepening |
| SD-049 | Current main DQ-003 revert | MAPPED — REVERSED | No semantic adjudication |
| SD-050 | P0-1 canonical representation contract | MAPPED — ALREADY VERIFIED | No deepening |
| SD-051 | P0-2 evidence/hash-domain contract | MAPPED — ALREADY VERIFIED | No deepening |
| SD-052 | Reverted CODEOWNERS commit | MAPPED — REVERSED / NON_AUTHORITY | None |
| SD-053 | DQ-003 revert branch / PR #43 head | MAPPED — REVERSED | No deepening |
| SD-054 | APS-200 specification recovery control | MAPPED — NON_AUTHORITY | None |
| SD-055 | BC-02 immutable fixture handoff construction | MAPPED — ALREADY VERIFIED | No deepening |
| SD-056 | BC-02 boundary validation blocked | MAPPED — ALREADY VERIFIED | No deepening |
| SD-057 | Protocol handoff duplicate cross-check | MAPPED — NON_AUTHORITY / DEDUP | None |

## 4. Remaining authority-bearing pass

The remaining work is deliberately narrow. It is **not** another DQ/P0/BC-02 investigation.

### R-01 — Bootstrap authority claim

**Stage 06:** SD-001

Claim requiring evidence check:
- initial repository/changelog descriptions of the APS Markdown corpus as canonical;
- imported source documents described as authoritative;
- Constitution v1.0 described as FROZEN.

Required evidence search:
- PR #5 review submissions;
- PR #5 issue comments / timeline;
- commit/repository governance records explicitly establishing the claimed authority;
- signed tags/releases or separate approval records, if any.

Disposition rule:
- repository creation/merge proves repository state only;
- absence of an approval record must remain an evidence finding, not proof that no external act ever existed.

### R-02 — ARC/SPEC Chief Architect attribution

**Stage 06:** SD-003

Claim requiring evidence check:
- commit message attributes corrections to the Chief Architect.

The actual semantic delta is independently observed: ARC synchronization is made incremental, ARC→SPEC mapping is reserved until SPEC-001 approval, and template requirement identifiers are tightened.

Required evidence search:
- commit comments;
- PR review/timeline associated with the change, if discoverable;
- explicit approval/delegation record.

The commit message itself is not sufficient to establish an approval act.

### R-03 — Historical APS/Constitution Active claim

**Stage 06:** SD-032

Claim requiring evidence check:
- `docs/APS.md` and `docs/CONSTITUTION.md` were represented as v1.0.0 Active/comprehensive documents.

Required evidence search:
- PR/review evidence for the integration;
- explicit ratification or release record;
- later governance records that expressly recognize or supersede the historical Active status.

Current treatment remains `CLAIMED_ONLY` until such evidence is located.

### R-04 — ADR-001 authority representation

**Stage 06:** SD-045

This is not a P0/DQ/BC-02 deepening. It is a document-governance coverage check.

Two current-main ADR-001 representations remain relevant:
- `adrs/ADR-001_DOCUMENT_MODEL.md` — `PROPOSED`;
- `docs/adr/001-document-model.md` — `DRAFT`.

Required evidence search:
- any explicit Protocol Custodian approval;
- PR review/merge evidence satisfying the ADR's own acceptance condition;
- explicit supersession relation between the two representations.

Until then, the authority model proposed by ADR-001 remains unexecuted and the representation conflict remains `CONFLICTED`.

## 5. Negative-control rule

For all rows classified `NON_AUTHORITY`, the absence of an approval search is not itself a defect. The Stage 07 record must point to the artifact's explicit non-authority boundary where available.

For all rows classified `CLAIMED_ONLY`, the next action is evidence search, not semantic reinterpretation.

For all rows classified `ALREADY VERIFIED`, no additional semantic investigation is authorized by this coverage pass unless new contradictory evidence appears.

## 6. Closure precondition

The Stage 07 Closure Gate must not be executed merely because the matrix is populated.

The gate requires:

```text
57/57 Stage 06 subjects mapped
        ↓
all authority-bearing claims have an evidence disposition
        ↓
external approval/ratification search exhausted for remaining claims
        ↓
conflicts explicitly recorded
        ↓
reverts/supersession kept distinct
        ↓
no unresolved authority-claim row hidden by aggregation
        ↓
FORMAL STAGE 07 CLOSURE GATE
```

**Current disposition:** `OPEN`.

No Stage 08 work is authorized by this artifact.
