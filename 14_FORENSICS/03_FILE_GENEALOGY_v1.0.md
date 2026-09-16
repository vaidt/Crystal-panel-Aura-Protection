# AURA FILE GENEALOGY v1.0

## 1. Purpose

This document is a forensic reconstruction artifact for `Aura-IDToken/aura-specification`.

Its purpose is to establish, file by file, **what AURA actually wrote, when it appeared, where it lived, through which branch/commit/PR it travelled, what semantic change occurred, and what authority evidence exists**.

This is **not** a redesign, specification rewrite, canonization act, or supersession decision.

Status: `ACTIVE — FORENSIC RECONSTRUCTION`
Authority created: `NONE`
Normative effect: `NONE`

---

## 2. Hard forensic rule

No file receives `CANONICAL`, `FINAL`, `SUPERSEDED`, `NORMATIVE`, or equivalent status from filename, directory, branch name, PR title, commit message, or apparent intent alone.

Required evidence chain:

```text
FILE
  ↓
FIRST APPEARANCE
  ↓
COMMIT SHA
  ↓
BRANCH / PR
  ↓
ANCESTRY
  ↓
SUBSEQUENT BLOBS
  ↓
SEMANTIC DELTA
  ↓
AUTHORITY EVIDENCE
  ↓
REVERT / MERGE / DESCENDANTS
  ↓
CURRENT REACHABILITY
  ↓
FORENSIC STATUS
```

The following properties are kept separate:

- `EXISTS` — the artifact occurred in Git history;
- `REACHABLE` — the artifact is reachable from the analyzed ref;
- `CURRENT` — it is the current representation for a subject;
- `AUTHORITATIVE` — an identified authority act gives it authority;
- `NORMATIVE` — it contains protocol requirements with established normative force;
- `SUPERSEDED` — evidence identifies a replacement;
- `REVERTED` — a later change explicitly reverted it;
- `HISTORICAL` — preserved as evidence of an earlier state.

Therefore:

```text
EXISTS ≠ REACHABLE ≠ CURRENT ≠ AUTHORITATIVE ≠ NORMATIVE
```

---

## 3. Repository baseline used for this phase

Repository: `Aura-IDToken/aura-specification`

Observed current `main` HEAD:

```text
71133de047c71e0bc1156d58c20396fe593ace70
```

Observed current main commit:

```text
2026-09-10T22:09:45Z
Revert "docs(dq-003): specification reconciliation control record (#43)"
```

This matters because the current main tree is a **revert state**. The genealogy must therefore preserve both the current reachable state and the reverted predecessor state.

The immediately preceding DQ-003 commit was:

```text
74220d27f6af01f335fb1423886a51eb063f90f7
2026-09-10T22:09:10Z
```

It existed on main before PR #43 reverted it.

---

# 4. File genealogy master register — phase 1

The entries below establish the first controlled baseline for the principal specification corpus. They are not a claim that all files in the repository have yet been completely genealogized.

## FG-001 — AURA Constitution

**Artifact:** `AURA Constitution_260723_190157.pdf` and corresponding `.txt`; canonical Markdown representation also exists in later repository structure.

**Functional role:** constitutional / governance foundation candidate.

**Embedded artifact timestamp:** `2026-07-23 19:01:57` (from filename).

**Git provenance:** introduced through the initial specification documentation work associated with PR #1; exact per-file first-blob timestamp remains a required ancestry query in the next forensic pass.

**Initial PR:** PR #1 — `[WIP] Add complete documentation for APS and Constitution`.

**PR #1 merge:** `10ee452d0f2ffded08bc952f97457f994113b47e`, `2026-07-23T19:14:08Z`.

**Observed function:** establishes the highest-level constitutional framing used by subsequent APS documents.

**Semantic role:** defines the governing principles against which later APS material is presented.

**Authority:** repository/document claims must be distinguished from a separately proven authority act. Presence in PR #1 does not by itself prove later normative authority.

**Status:** `UNRESOLVED — GENEALOGY BASELINE`.

**Reason:** artifact existence and initial incorporation are established, but complete first-blob ancestry, all later representations, and authority chain still require file-level reconstruction.

---

## FG-002 — APS-000 Foundation & Terminology

**Artifact:** `AURA Protocol Specification APS-000 — Foundation &_260723_191759.pdf`, corresponding `.txt`, later `aps/APS-000_FOUNDATION_AND_TERMINOLOGY.md`.

**Embedded artifact timestamp:** `2026-07-23 19:17:59`.

**Functional role:** foundation and terminology layer.

**Initial corpus relation:** part of the APS corpus introduced during the initial documentation phase.

**Observed current representation:** `aps/APS-000_FOUNDATION_AND_TERMINOLOGY.md`.

**Semantic role:** establishes foundational vocabulary and document-level protocol context used by downstream APS documents.

**Known later change:** PR #4 corrected documentation artifacts in APS-000, including stray `text` lines in sections 4 and 9.

**PR #4 semantic class:** documentation normalization / content correction, not a demonstrated protocol redesign.

**Authority:** must be traced through Constitution/APS hierarchy and later governance evidence; filename and placement do not independently establish authority.

**Status:** `UNRESOLVED — GENEALOGY BASELINE`.

---

## FG-003 — APS-100 Protocol Invariants

**Artifact:** `APS-100 — Protocol Invariants_260723_192315.pdf`, `.txt`, and later `aps/APS-100_PROTOCOL_INVARIANTS.md`.

**Embedded artifact timestamp:** `2026-07-23 19:23:15`.

**Functional role:** invariant definition layer.

**Observed semantic payload:** defines protocol invariants such as deterministic evaluation, replay, canonical serialization, evidence immutability, traceability, platform independence, fail-closed behavior, version compatibility, conformance completeness, cryptographic evidence integrity, audit trail requirements, and related controls.

**Known Git evidence:** commit `5f91167d0611dc91a25ebd6e1ddc3d4ce41175ca`, `2026-07-23T19:26:02Z`, corrected documentation errors across APS files. The APS-100 change specifically removed a stray `text` artifact in the section 5 traceability matrix.

**Important timestamp distinction:** embedded timestamp `19:23:15` precedes the documented correction commit at `19:26:02`. The filename timestamp is therefore not treated as Git first appearance or last modification.

**Status:** `UNRESOLVED — GENEALOGY BASELINE`.

---

## FG-004 — APS-200 Canonical Data Model

**Artifact:** `APS-200 — Canonical Data Model_260723_192852.pdf`, `.txt`, and `aps/APS-200_CANONICAL_DATA_MODEL.md`.

**Embedded artifact timestamp:** `2026-07-23 19:28:52`.

**Functional role:** canonical data model / entity / serialization / cryptographic representation boundary.

**Current MD blob observed on main:** `0488eec04e102e87b5724ca385a534d0c5f4e1cd`.

**Current size observed:** 11,445 bytes.

**Current document status:** `DRAFT`.

**Observed content:** ENT-001 through ENT-008, common object contract, JCS/RFC 8785 references, SHA-256 canonical-byte binding, RFC 6962 leaf/interior domains, CANONICAL-001 vector, schemas, event registry and traceability. The document itself retains TODOs concerning execution_id, request_fields, decision vocabulary and attestation lifecycle/authority.

**Known major semantic transition:** PR #26 changed APS-200 §8 from a TODO to an explicit canonical serialization profile, including RFC 8785 JCS, UTF-8 `canonical_bytes`, prohibited digest inputs, hash/Merkle byte domains, cross-implementation byte identity, scope boundaries and migration.

**PR #26 semantic classification:** specification-layer reconciliation / attempted normative binding, while the PR simultaneously recorded DQ-006 as still open.

**Important evidence:** the PR text itself calls §8 the single normative authority for canonical serialization, but this is a declaration within the change and must not be conflated with independent governance ratification.

**Later DQ-003 event:** a reconciliation control record concerning APS-200 §6–§10 was committed as `74220d27...` and subsequently reverted by PR #43. The associated reference-audit artifact is therefore historical evidence, not current-main content.

**Status:** `UNRESOLVED — HIGH-VALUE FORENSIC TARGET`.

---

## FG-005 — APS-300 Evidence Model

**Artifact:** `APS-300 — Evidence Model_260723_193234.pdf`, `.txt`, and `aps/APS-300_EVIDENCE_MODEL.md`.

**Embedded artifact timestamp:** `2026-07-23 19:32:34`.

**Functional role:** evidence object model, evidence hashing, chaining, integrity and verification layer.

**Current MD blob observed:** `347112b0aa6140b91e3dff7a505912069991a186`.

**Current status:** `DRAFT`.

**Known PR #26 transition:** replaced the earlier TODO for `evidence_hash` with canonical-byte binding, domain separation between evidence hashes and Merkle leaf/node hashes, and an explicit migration rule. It also tightened `previous_evidence_hash` semantics.

**Semantic classification:** cryptographic evidence-model tightening / reconciliation.

**Authority status:** unresolved independently of content claims.

**Status:** `UNRESOLVED — HIGH-VALUE FORENSIC TARGET`.

---

## FG-006 — APS-400 Conformance Test Matrix

**Artifact:** `APS-400 — Conformance Test Matrix_260723_193617.pdf`, `.txt`, and `aps/APS-400_CONFORMANCE_TEST_MATRIX.md`.

**Embedded artifact timestamp:** `2026-07-23 19:36:17`.

**Functional role:** conformance control matrix mapping invariants to CONF tests, evidence and implementation coverage.

**Current MD blob observed:** `769dab5fae5331f35408422ad787fb875ea9aec7`.

**Current status:** `DRAFT`.

**Observed current content:** CONF-001 through CONF-015 are represented; rows are DRAFT and assignments are not equivalent to executed PASS evidence.

**Known PR #4 transition:** CONF-009 gained its missing `Related Invariant` entry `INV-004 · INV-005` and documentation artifacts were cleaned.

**Status:** `UNRESOLVED — GENEALOGY BASELINE`.

---

## FG-007 — APS-500 Reference Fixtures

**Artifact:** `APS-500 Reference Fixtures_260723_194023.pdf`, `.txt`, and `aps/APS-500_REFERENCE_FIXTURES.md`.

**Embedded artifact timestamp:** `2026-07-23 19:40:23`.

**Functional role:** fixture corpus definition and certification basis.

**Current MD blob observed:** `efeaceafcbae49c6b5e17f9bf0fec869bbe6dbbb`.

**Current status:** `DRAFT`.

**Observed current content:** fixture structure/categories and FIX-001 placeholder, with TODOs for corpus finalization.

**Important semantic distinction:** fixture definitions, fixture execution, and fixture authority are separate states.

**Status:** `UNRESOLVED — GENEALOGY BASELINE`.

---

## FG-008 — APS-900 Compliance Mapping

**Artifact:** `APS-900 — Compliance Mapping_260723_194128.pdf`, `.txt`, and `aps/APS-900_COMPLIANCE_MAPPING.md`.

**Embedded artifact timestamp:** `2026-07-23 19:41:28`.

**Functional role:** traceability and compliance mapping layer.

**Current MD blob observed:** `86978670a45c9c6757ce2dbea1a66b18b1f9302c`.

**Current status:** `DRAFT`.

**Observed traceability chain:** Constitution → APS → INV → ENT → Evidence → CONF → FIX → EVID → RI → Release.

**Semantic role:** describes how claims and controls are connected across the specification/conformance stack.

**Authority:** mapping is not itself proof that every linked object is authoritative.

**Status:** `UNRESOLVED — GENEALOGY BASELINE`.

---

## FG-009 — APS-950 Reference Implementation Requirements

**Artifact:** `APS-950 — Reference Implementation Requirements_260723_194507.pdf`, `.txt`, and `aps/APS-950_REFERENCE_IMPLEMENTATION_REQUIREMENTS.md`.

**Embedded artifact timestamp:** `2026-07-23 19:45:07`.

**Functional role:** requirements for reference implementations, repository structure, tests, builds, documentation and releases.

**Current MD blob observed:** `c5d7f04002925f9d0b9b8c62b4c6b82f01e02ae9`.

**Current status:** `DRAFT`.

**Observed content:** RI-PY and RI-RS are listed as Active in the document, but broader governance evidence records unresolved lineage/canonicality questions. Therefore the table is treated as document content, not independent proof of current authority.

**Status:** `UNRESOLVED — HIGH-VALUE FORENSIC TARGET`.

---

## FG-010 — EVENT_TYPE_REGISTRY

**Artifact:** `aps/EVENT_TYPE_REGISTRY.md`.

**Current blob observed:** `a329f8635b3fc858868f43c33f753636af1737f3`.

**Functional role:** event-type vocabulary and registry control.

**Forensic significance:** later governance/evidence records identify tension between the registry state and fixture/event tokens. This must be reconstructed as a separate genealogy rather than inferred from the registry filename.

**Status:** `UNRESOLVED — GOVERNANCE/SEMANTIC TARGET`.

---

## FG-011 — CONF-001 … CONF-* individual conformance records

**Functional role:** individual executable/conformance requirement definitions beneath the APS-400 matrix.

**Observed examples:** CONF-001 deterministic evaluation, CONF-002 replay verification, CONF-003 canonical serialization, CONF-004 evidence integrity, CONF-005 traceability, CONF-006 platform independence, CONF-007 fail-closed, CONF-008 version compatibility, CONF-009 evidence completeness, CONF-010 cryptographic verification, CONF-011 zero-float runtime, CONF-012 auditability, CONF-013 policy determinism, with additional entries requiring complete inventory.

**Important rule:** existence of a `CONF-*` file does not equal executed conformance. `CONF identifier exists` ≠ `PASS`.

**Status:** `UNRESOLVED — COMPLETE INVENTORY REQUIRED`.

---

## FG-012 — ADR corpus

**Functional role:** architecture/governance decision records.

**Known examples:** repository structure/document model ADRs and CK-003/DQ-006 decision material.

**Forensic rule:** an ADR is an evidence-bearing decision record, but `PROPOSED`, `ACCEPTED`, `REJECTED`, `SUPERSEDED`, etc. must be established from the actual record and its governance context. A filename or PR title cannot create authority.

**Known important transition:** PR #26 describes `ADR-CK003-DQ006` as changed from `PROPOSED` to `ACCEPTED`, while the same PR's closure narrative states DQ-006 remained open. This is a high-priority semantic genealogy target because the decision-state history must be reconstructed rather than normalized by interpretation.

**Status:** `UNRESOLVED — HIGH-VALUE GOVERNANCE TARGET`.

---

## FG-013 — SPEC-002

**Artifact family:** Constitution Artifact / Constitution Vector contract.

**Known versions:** v0.1-DRAFT → v0.2-DRAFT → v0.3-DRAFT.

**Functional role:** future contract for deterministic Constitution Artifact/Vector generation and verification.

**Observed rule:** `Normative effect: NONE until APPROVED`.

**PR #11:** initial draft.

**PR #12:** v0.2-DRAFT; source boundary, identity separation, hash-domain separation, verification split, traceability expansion, registration/freeze separation and independent-implementer test were strengthened.

**PR #13:** v0.3-DRAFT; added provenance/determinism boundary, dependency closure, per-domain canonical bytes, stronger rejection semantics and additional negative integrity cases.

**Forensic significance:** SPEC-002 explicitly demonstrates the desired separation between candidate architecture and approved protocol authority.

**Status:** `DRAFT / NON-AUTHORITATIVE BY ITS OWN DECLARATION` unless later evidence establishes otherwise.

---

## FG-014 — DQ-002 evidence and closure family

**Functional role:** cross-language Merkle/hash-domain reconciliation and evidence.

**Known artifacts/branches:**

- `ck003/dq-002-hash-domain`
- `ck003/cross-language-002`
- `claude/ck003-canonical-serialization-hjlaba`
- `claude/dq-002-final-closure-i5s60o`
- `dq/dq-003-audit-record-hash-domain` contains an RI entry-point baseline related to the reconciliation surface.

**Known semantic facts:** independently generated vectors, RFC 6962 oracle, audit paths, cross-language comparison, and explicit defects were recorded. Multiple records state DQ-002 remained open or blocked despite equality evidence.

**Critical distinction:** implementation equality evidence is not automatically protocol approval.

**Status:** `HISTORICAL / ACTIVE-EVIDENCE FAMILY — FINAL AUTHORITY UNRESOLVED`.

---

## FG-015 — DQ-006 closure family

**Functional role:** canonical serialization cross-language closure/reconciliation.

**Known branch/PR family:** PR #17 onward, including PRs #24–#27 and associated `ck003/*` and `claude/*` branches.

**Known semantic transition:** evidence initially recorded PASS/equality for CANONICAL-001, while later analysis identified that the vector was JCS-degenerate and could not discriminate RFC 8785 from sorted JSON. Closure therefore remained conditional/open in some records.

**Forensic significance:** this family is a major example of why `PASS`, `CLOSED`, `ACCEPTED`, `NORMATIVE`, and `RATIFIED` must be represented as separate properties.

**Status:** `UNRESOLVED — HIGH-VALUE GENEALOGY TARGET`.

---

## FG-016 — DQ-003 specification reconciliation family

**Functional role:** specification reconciliation control record for APS-200 §6–§10 and related gaps.

**PR #33 / PR #34:** DQ-003 control record, explicitly non-normative, with DQ-003 remaining OPEN and C4 NOT AUTHORIZED.

**Reverted state:** commit `74220d27f6af01f335fb1423886a51eb063f90f7` introduced the DQ-003 reconciliation control record and APS-200 §6–§10 reference audit.

**Revert:** PR #43 merged commit `71133de047c71e0bc1156d58c20396fe593ace70` and returned main to the predecessor state.

**Forensic classification:** the reverted artifact **exists historically** but is not reachable from current main.

**Status:** `HISTORICAL / REVERTED` for the affected artifact(s); authority impact remains unresolved.

---

## FG-017 — Documentation Normalization Audit v1

**Functional role:** observational normalization audit.

**PR #37:** read-only, observational; explicitly states nothing was resolved, no authority was created, no supersession was established and no main branch was touched.

**Semantic contribution:** establishes a rigorous distinction among `EXISTS`, `REACHABLE`, `AUTHORITATIVE`, `CURRENT`, and `NORMATIVE`.

**Forensic significance:** this artifact is a methodological precedent for the current genealogy work.

**Status:** `EVIDENCE_ONLY / CONTROLLED_ANALYSIS`.

---

## FG-018 — Documentation Normalization Control Review v1

**Functional role:** controlled read-only review of identity, provenance, reachability, lineage and status classification.

**PR #38:** records identity entries, lineage relations, declaration-vs-content divergences, absence claims, conflicts and governance-review items.

**Explicit effect:** no decision, no supersession, no authority creation.

**Forensic significance:** directly supports the methodological rule that repository presence or merge does not itself create governance authority.

**Status:** `EVIDENCE_ONLY / CONTROLLED_ANALYSIS`.

---

## FG-019 — Q1 Scope Bridge governance instruments

**Artifacts:**

- `BC-02-Q1-CHIEF-ARCHITECT-CUSTODIAN-SCOPE-BRIDGE.md`
- `BC-02-Q1-CHIEF-ARCHITECT-APPROVAL-DELEGATION-RECORD.md`

**PRs:** #39, #40, #41, #42 family.

**Functional role:** prepare jurisdictional/approval instruments without executing the authority act.

**Explicit state:** Q1 jurisdiction not established; selection gate closed; package none; approval pending/unexecuted; implementation unauthorized.

**Forensic significance:** these files are governance instruments, not evidence that the underlying approval actually occurred.

**Status:** `GOVERNANCE_ONLY / UNEXECUTED` unless later approval evidence is found.

---

# 5. Timestamp discipline

For every file, at least three dates must be kept separate when available:

| Date field | Meaning |
|---|---|
| Embedded artifact timestamp | timestamp encoded in filename or document metadata |
| First Git appearance | first commit/tree/blob in repository history |
| Modification timestamp | commit in which the relevant content changed |

A fourth field is required when applicable:

| Date field | Meaning |
|---|---|
| Reachability date | first/last known point at which the representation was reachable from a specified branch/ref |

Example already established for APS-100:

```text
Embedded filename timestamp: 2026-07-23 19:23:15
Documentation correction commit: 2026-07-23 19:26:02
```

Therefore the filename timestamp must not be substituted for Git provenance.

---

# 6. Representation genealogy rule

PDF, TXT and Markdown representations are not automatically treated as the same artifact.

For each pair, the reconstruction must determine whether the relation is:

```text
SAME_ARTIFACT / REPRESENTATION
DERIVED_COPY
NORMALIZED_COPY
SEMANTICALLY_MODIFIED_COPY
INDEPENDENT_ARTIFACT
UNKNOWN
```

The same rule applies to:

- duplicated ADRs;
- copied closure packages;
- branch-local evidence;
- regenerated fixtures;
- renamed documents;
- files with similar names but different content.

Content identity and semantic identity are separate properties.

---

# 7. Semantic delta taxonomy

Every file modification will be classified into one or more of:

- `FORMAT_ONLY`
- `TYPO_ONLY`
- `DOCUMENTATION_CORRECTION`
- `CLARIFICATION`
- `NEW_REQUIREMENT`
- `REQUIREMENT_TIGHTENING`
- `REQUIREMENT_RELAXATION`
- `NEW_INVARIANT`
- `INVARIANT_CHANGE`
- `DATA_MODEL_CHANGE`
- `SERIALIZATION_CHANGE`
- `HASH_DOMAIN_CHANGE`
- `EVENT_SEMANTICS_CHANGE`
- `CONFORMANCE_CHANGE`
- `FIXTURE_CHANGE`
- `EVIDENCE_CHANGE`
- `GOVERNANCE_CHANGE`
- `AUTHORITY_CHANGE`
- `STATUS_CHANGE`
- `REVERT`
- `REACHABILITY_ONLY`
- `UNKNOWN`

This taxonomy is descriptive. It does not itself assign authority.

---

# 8. Authority evidence model

For each file, authority must be represented independently from content.

Required fields:

```text
Authority type:
Authority source:
Authority act:
Authority actor/role:
Approval date:
Approval evidence:
Scope:
Limitations:
Revocation/revert evidence:
```

Possible authority sources include, but are not limited to:

- explicit constitutional provision;
- approved ADR;
- approved governance act;
- ratification record;
- release decision;
- designated custodian act;
- competent human approval.

A commit message saying `canonical`, `final`, `approved`, or similar is **not sufficient evidence by itself**.

---

# 9. Current forensic conclusions from phase 1

### 9.1 The specification corpus has multiple layers

The repository contains at least these distinct functional layers:

```text
Constitution
    ↓
Foundation / Terminology
    ↓
Invariants
    ↓
Data Model
    ↓
Evidence Model
    ↓
Conformance
    ↓
Fixtures
    ↓
Compliance / Traceability
    ↓
Reference Implementation Requirements
```

Around that core are:

```text
ADR / RFC / Governance
Evidence / DQ / CK-003
Templates / Operations
Historical / Reverted material
```

### 9.2 The repository contains specification evolution, not one static specification

The file families show repeated transitions from:

```text
TODO
  → proposal
  → evidence
  → reconciliation
  → attempted binding
  → conditional closure
  → later governance challenge / revert
```

The genealogy must preserve those transitions rather than flatten them into one current narrative.

### 9.3 `main` is not sufficient to reconstruct AURA

Current main is a revert state. Important DQ-002, DQ-003, CK-003 and governance material exists on branches and/or in historical commits.

Therefore the forensic corpus is:

```text
main
+ merged history
+ reverted history
+ surviving branches
+ branch-local artifacts
+ PR metadata
+ commit ancestry
```

### 9.4 Semantic status cannot be inferred from reachability

A document can be:

- present on main but DRAFT;
- absent from main but historically important;
- merged but explicitly non-binding;
- marked PASS while a closure gate remains open;
- described as accepted inside a PR while broader ratification remains unresolved.

This is why the final file genealogy will not use a single `status` field without its evidence basis.

---

# 10. Remaining file-genealogy work

This v1.0 is a **baseline**, not a claim of complete per-file reconstruction.

Next passes must:

1. enumerate every path in every relevant main-tree and branch-tree snapshot;
2. identify the first commit containing each path;
3. identify the first blob SHA;
4. retrieve every later blob SHA for semantically relevant files;
5. map every modification to its commit and branch;
6. map every modification to PR where available;
7. compare representations byte-for-byte where possible;
8. compare semantic content where byte identity differs;
9. identify reverts and reachability changes;
10. identify authority evidence separately;
11. record unresolved conflicts rather than resolving them by interpretation;
12. link each file to the branch genealogy and PR genealogy;
13. produce a machine-readable companion register after the human-readable forensic map stabilizes.

---

# 11. Required next artifact

The next forensic artifact should be:

`04_BRANCH_GENEALOGY_v1.0.md`

Its purpose is to enumerate the surviving branch set, deduplicate branches by HEAD/tree identity, preserve branch aliases, reconstruct ancestry, and identify branch-local artifacts.

After that:

```text
03_FILE_GENEALOGY
        ↓
04_BRANCH_GENEALOGY
        ↓
05_SEMANTIC_DELTA_REGISTER
        ↓
06_AUTHORITY_EVIDENCE_REGISTER
        ↓
07_REVERT_SUPERSESSION_CONFLICT_REGISTER
        ↓
08_FORENSIC_CROSS_REFERENCE
        ↓
09_MASTER_BRANCH_MAP
```

---

## 12. Forensic statement

> **AURA is reconstructed here as a sequence of authored artifacts and controlled changes, not as a retrospective story.**
>
> Every claim about what AURA became must ultimately be traceable to an artifact, its Git provenance, its semantic delta, and an identifiable authority basis—or explicitly marked unresolved.

---

**Document class:** Forensic Reconstruction / Evidence Map

**Authority:** None

**Normative effect:** None

**Current status:** ACTIVE — FORENSIC RECONSTRUCTION

**Do not use this document as protocol authority.**
