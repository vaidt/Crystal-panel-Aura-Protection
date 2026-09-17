# AURA — STAGE 06 SEMANTIC DELTA REGISTER v1.0

**Artifact:** `14_FORENSICS/06_SEMANTIC_DELTA_REGISTER_v1.0.md`  
**Source repository:** `Aura-IDToken/aura-specification`  
**Forensic repository:** `vaidt/Crystal-panel-Aura-Protection`  
**Stage:** 06 — Semantic Delta Register  
**Status:** OPEN — CONTROLLED FORENSIC RECONSTRUCTION  
**Authority:** NONE  
**Normative effect:** NONE  

## 1. Purpose

Stage 06 begins only after Stage 05 established the topology gate at 57/57 unique HEADs. Its purpose is to reconstruct what each branch actually changed semantically, without redesigning AURA and without treating branch names, chronology, filenames, or implementation behaviour as authority.

The governing chain is:

```text
verified HEAD
  -> verified topology
  -> changed artifacts
  -> content-level change
  -> semantic delta
  -> evidence delta
  -> governance delta
  -> authority evidence
```

A semantic delta is not a judgement of correctness. It is a description of what the artifact content changes relative to the appropriate Git baseline.

## 2. Classification vocabulary

| Code | Meaning |
|---|---|
| `DOC` | documentation/editorial change with no established protocol-semantic change |
| `SPEC` | specification/normative-text semantic change |
| `CONF` | conformance/test/gate semantic change |
| `FIX` | fixture/vector/hash-domain/evidence-value change |
| `GOV` | governance, authority, jurisdiction or decision-state change |
| `IMPL` | implementation or executable reference change |
| `AUDIT` | read-only audit/review/assessment; no protocol semantics asserted |
| `REVERT` | explicit Git reversal relation |
| `MIXED` | more than one semantic class in the same HEAD |
| `UNRESOLVED` | topology known, but content-level semantic classification not yet sufficiently expanded |

Status vocabulary deliberately separates observation from authority:

```text
OBSERVED
SEMANTIC DELTA IDENTIFIED
AUTHORITY EFFECT UNKNOWN
```

## 3. Forensic rules

1. Do not infer semantics from branch names.
2. Do not infer authority from commit messages.
3. Do not equate `ahead_by` with semantic-change count.
4. Do not equate changed-file count with semantic-change count.
5. Do not classify a document as normative merely because it uses MUST/SHOULD or calls itself canonical.
6. Preserve contradictory artifacts as separate historical records until an authority act establishes disposition.
7. A Git revert establishes a reversal of repository state; it does not automatically establish that the underlying historical proposition was false.
8. A branch-local assertion of `CLOSED`, `ACCEPTED`, `FINAL`, or `CANONICAL` is recorded as an assertion unless the authority chain independently supports it.

## 4. Verified semantic-delta records

### SD-001 — Initial specification repository bootstrap

**HEAD:** `93f677fe34bf3f3fe0e8abffd6c8fdfd92b7958f`  
**Class:** `MIXED` (`DOC` + `SPEC` structure)  
**Evidence:** merge PR #5; commit message `feat: build canonical repository structure for aura-specification`.

The commit introduces the repository governance/documentation structure, APS Markdown corpus, invariant registry, conformance stubs, traceability model, and RFC/ADR templates. The commit's changelog describes the Markdown corpus as canonical and the imported APS source documents as authoritative; these are recorded as historical declarations, not independently promoted here to current authority.

**Semantic effect:** establishes the initial specification-repository representation and governance/document lifecycle structure.  
**Authority effect:** not determined by this entry.  
**Historical note:** this HEAD is an ancestor of current `main`.

### SD-002 — Polish/English terminology normalization

**HEAD:** `e639d9c699204bad06f0cb5a135b380c1f837b9c`  
**Class:** `DOC`  
**Commit:** `Polish-English terminology consistency in version headers`  
**Date:** `2026-07-23T19:20:27Z`.

Changes `Wersja:` to `Version:` in `docs/APS.md` and `docs/CONSTITUTION.md`. No protocol requirement is established by the changed text itself.

### SD-003 — ARC/SPEC synchronization structure

**HEAD:** `102423256e33ad3dea54461f692819aeebaa0700`  
**Class:** `GOV` + `DOC`  
**Commit:** `docs(spec): apply Chief Architect corrections to ARC/SPEC templates and mapping structure`  
**Date:** `2026-08-02T18:03:45Z`.

The change makes ARC synchronization incremental through Issue → Branch → PR → Review → Merge, reserves ARC→SPEC mapping until SPEC-001 approval, and updates specification templates. This is a process/governance-model change in repository documentation, not proof of protocol semantic approval.

### SD-004 — DQ-002 hash-domain correction

**HEAD:** `f12a667b252a66f8b2243d1187b927d46ed26468`  
**Class:** `FIX` + `CONF`  
**Commit:** `CK-003 DQ-002: correct independently computed leaf fixture`  
**Date:** `2026-08-17T20:31:21Z`.

The cross-language fixture is changed to canonical-byte length 58, leaf-input length 59, and recorded digest `ba2749fedbcff14c1409a22c721c8de2e0f9ebd9c4177cc8b3950142b3bfd123`. The commit records independent recomputation before fixture recording.

**Semantic delta:** concrete evidence/vector values for the DQ-002 hash-domain work.  
**Authority:** fixture correction is not itself authority for the protocol rule.

### SD-005 — DQ-003 version-binding fixture

**HEAD:** `d858a902a934d50d82788f9551fa34fc5c6b6842`  
**Class:** `FIX` + `CONF`  
**Commit:** `test(ck003): add DQ-003 version binding fixture`  
**Date:** `2026-08-17T22:02:58Z`.

Adds the DQ-003 version-binding fixture. The recorded fixture status is `PROPOSED` and explicitly carries blockers. It therefore records a proposed/testable state rather than an established normative versioning rule.

### SD-006 — CROSS-LANGUAGE-002 manifest

**HEAD:** `ac6a7c86ac282d2a806da6bfde3e67a30dc4c035`  
**Class:** `CONF` + `FIX` + `AUDIT`  
**Commit:** `docs: add CROSS-LANGUAGE-002 machine manifest`  
**Date:** `2026-08-18T20:28:54Z`.

Adds a machine manifest for DQ-002, raw-leaf-byte contract, RFC-6962 recursive split, expected vectors, and preflight receiver states. The associated comparison surface contains eight files across DQ-002/CROSS-LANGUAGE-002 evidence and fixture material.

### SD-007 — DQ-006 closure line

**HEAD:** `632d307169540fe0bb13d75c10a1ff55e4885349`  
**Class:** `MIXED` (`CONF` + `FIX` + `SPEC`-adjacent + `GOV`)  
**Commit:** `docs(closure): close DQ-006 canonical serialization conformance`.

The change rewrites DQ-006 closure material and adds event-registry/matrix material. Because the branch-local corpus contains a closure assertion, the assertion must be preserved as a historical semantic state and separately tested against authority/evidence. This entry does not accept the closure assertion as current authority.

### SD-008 — DQ-006 reconciliation

**HEAD:** `f02b087e9ce857603d1d45b7386e46323ca8e32d`  
**Class:** `MIXED` (`SPEC` + `CONF` + `GOV` + `FIX`)  
**Semantic surface:** APS-200, APS-300, DQ-006 ADR/closure/evidence, CONF-003, canonical fixtures and traceability material.

This family materially changes the documented canonical-serialization contract and associated evidence/conformance state. The precise authority chain remains a separate Stage 07 question.

### SD-009 — DQ-006 final-closure execution line

**HEAD:** `ad7548cc6ff830ac8af68a1ec09bffd201f27e58`  
**Class:** `CONF` + `GOV`  
**Semantic surface:** DQ-006 closure execution-order material and CK003 README.

The branch records a final-closure execution ordering artifact. It does not, by itself, establish that execution occurred or that the resulting semantic decision became authoritative.

### SD-010 — DQ-006 specification integration

**HEAD:** `7826db9e3e28d356693ba24618f320c44e3120b1`  
**Class:** `SPEC` + `CONF` + `AUDIT`  
**Semantic surface:** APS-200, INV conformance matrix, architecture execution audit, Gate A matrix.

The comparison records direct changes to APS-200 and associated closure matrices. This is a protocol-document semantic delta and must be reconciled against prior and subsequent APS-200 representations.

### SD-011 — APS-200 specification recovery

**HEAD:** `84e4962d418058488d08bcd5d3c3a5577c4b6f8f`  
**Class:** `SPEC` + `AUDIT`  
**Commit:** `custodian: record D-1 physical APS-200 edit evidence`  
**Date:** `2026-08-23T16:22:09Z`.

Adds physical-edit evidence and recovery/audit records around APS-200. The artifact records evidence concerning a specification edit; it does not itself establish the semantic validity or authority of that edit.

### SD-012 — Documentation normalization audit

**HEAD:** `d2d26903d01865899a2424b0230fc3f6c72a5eb8`  
**Class:** `AUDIT`  
**Commit:** controlled read-only normalization review, `2026-08-25T16:47:05Z`.

Adds a 931-line normalization control review. The commit explicitly states that nothing is resolved, no supersession is established, and no authority is created or selected. This is therefore evidence/audit material, not a semantic protocol amendment.

### SD-013 — Protocol handover assessment

**HEAD:** `bfa61f1f1c44a10d3102c7a7eb85602ba42206d9`  
**Class:** `AUDIT` + `GOV`  
**Date:** `2026-08-19T17:13:01Z`.

Adds HANDOVER-ASSESSMENT-001 as an inherited-state assessment. The commit explicitly states that it is non-normative, closes nothing, reopens nothing, and routes detected conflicts for human/Protocol Custodian resolution. fileciteturn251file0L2-L2

### SD-014 — Q1 Chief Architect → Custodian Scope Bridge preparation

**HEAD:** `eb263ce3f325fd14213c49fff1ab2da3453c426f`  
**Class:** `GOV`  

Adds a proposed bounded delegation instrument for designation of the Q1 Decision Surface. Its own status is `DRAFT — AUTHORITY INSTRUMENT PREPARATION`; it expressly states that repository presence is not governance approval and that jurisdiction remains not established pending competent approval. fileciteturn249file0L3-L7

### SD-015 — BC-02 / BC-02.1 decision package

**HEAD:** `dd11311bff7c19ace8cddc002402ce2e04a3c3c4`  
**Class:** `GOV` + `AUDIT`  
**Date:** `2026-08-24T20:26:23Z`.

Adds the Custodian Decision Package A/B v1. The commit explicitly records both Decision A and Decision B as not resolved, with no execution and no normative amendment. fileciteturn252file0L2-L2

### SD-016 — BC-02 review surface

**HEAD:** `a10ca5c567a0a5497ef30d270cf531b346a90d9b`  
**Class:** `AUDIT` + `GOV`  
**Date:** `2026-08-24T22:20:34Z`.

Adds a read-only Custodian Decision Review Surface. It preserves Decision A/B as open, reports a naming discrepancy, and explicitly states that no authority, implementation, conformance, or normative amendment is created. fileciteturn253file0L2-L2

## 5. Known high-value semantic families

### Family A — Canonical serialization / DQ-006

Observed evolution includes:

```text
proposal / audit material
    ↓
CANONICAL-001 oracle work
    ↓
DQ-006 closure assertions
    ↓
APS-200 §8 / APS-300 §5 textual binding
    ↓
JCS-specific conformance material
    ↓
closure / reconciliation variants
```

The semantic question is not whether this history exists. It does. The Stage 07 question is which steps, if any, received sufficient authority to become authoritative/normative.

### Family B — DQ-002 hash domain

Observed semantic surface:

```text
hash-domain ADR
→ leaf fixture
→ cross-language manifest
→ independent recomputation evidence
→ closure/revalidation variants
```

### Family C — DQ-003

Observed semantic surface:

```text
versioning snapshot
→ audit-record hash-domain analysis
→ specification reconciliation
→ revert of PR #34 on main
```

Current `main` contains the explicit Git revert of the DQ-003 reconciliation commit. This establishes repository-state reversal; it does not erase the historical existence of the DQ-003 semantic work.

### Family D — BC-02 / governance jurisdiction

Observed semantic surface:

```text
boundary validation
→ consistency analysis
→ decision package
→ review surface
→ proposed scope bridge
→ authority evidence
```

These are governance/authority artifacts and must not be interpreted as protocol semantics merely because they discuss unresolved protocol questions.

## 6. Current Stage 06 register state

Stage 06 is **OPEN** because the 57 topology records are now verified, but a complete content-level semantic expansion of every unique HEAD has not yet been independently reproduced in this artifact.

Current distinction:

```text
57/57 TOPOLOGY VERIFIED
        ↓
16 HIGH-VALUE SEMANTIC RECORDS EXPANDED
        ↓
41 UNIQUE HEADS REQUIRE CONTENT-LEVEL SEMANTIC EXPANSION
```

This is deliberate. No row is upgraded from `UNRESOLVED` merely from branch naming or commit chronology.

## 7. Next mechanical operation

For each remaining unique HEAD:

1. obtain exact commit diff;
2. enumerate every changed path;
3. inspect content-level additions/deletions for semantic-bearing text;
4. classify `SPEC / CONF / FIX / GOV / IMPL / AUDIT / DOC / MIXED`;
5. record evidence delta separately;
6. record governance delta separately;
7. link PR/merge/revert evidence where independently established;
8. only then construct cross-HEAD semantic relationships.

Only after this content-level pass is complete may Stage 06 be considered closed.

---

**Stage 06 disposition:** `OPEN — CONTROLLED FORENSIC RECONSTRUCTION`  
**Stage 05 dependency:** `CLOSED — 57/57 UNIQUE HEADS VERIFIED`  
**Authority:** `NONE`  
**Normative effect:** `NONE`
