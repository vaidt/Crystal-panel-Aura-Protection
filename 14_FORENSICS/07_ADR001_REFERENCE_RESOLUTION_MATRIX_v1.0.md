# AURA ADR-001 REFERENCE RESOLUTION MATRIX v1.0

## 1. Record Identity

- Artifact: `07_ADR001_REFERENCE_RESOLUTION_MATRIX_v1.0.md`
- Stage: Stage 07 Authority Evidence / Re-entry
- Source repository: `Aura-IDToken/aura-specification`
- Analysis ref: `main`
- Main HEAD examined: `71133de047c71e0bc1156d58c20396fe593ace70`
- Date: 2026-09-17
- Authority: NONE
- Normative effect: NONE
- Disposition: FORENSIC / EVIDENCE ONLY

## 2. Purpose

This matrix resolves every current-main search hit for the literal token `ADR-001` into:

`path → subject → introducing commit → current blob → branch ancestry → intended referent → authority dependency → ambiguity`

The matrix does **not** select an ADR-001 winner, infer supersession, or convert a repository status declaration into an independent authority act.

## 3. Resolution Rules

1. A literal `ADR-001` occurrence is not automatically a reference to a concrete ADR artifact.
2. Generic examples are classified as NON-REFERENTIAL and do not identify a subject.
3. A concrete path/link determines intended referent only where the source itself supplies that path.
4. Where a document says `ADR-001` without disambiguating subject/path, the referent remains AMBIGUOUS.
5. Introducing commit is the commit in which the artifact/path was introduced, where established by the existing forensic genealogy.
6. Current blob is the content identity at the examined `main` HEAD.
7. Branch ancestry records the known introduction path; it is not treated as authority.
8. Authority dependency records what approval/status mechanism the occurrence relies upon, not whether that mechanism was successfully exercised.

## 4. Concrete ADR-001 Subjects

| Ref | Path | Subject | Introducing commit | Current blob | Branch ancestry | Current status | Authority dependency | Ambiguity |
|---|---|---|---|---|---|---|---|---|
| A01 | `adrs/ADR-001_REPOSITORY_STRUCTURE.md` | Canonical Repository Structure | `b68181e48a65ed3a96007b5f3f89bad20a1caabf` | `3df6315b5b9883753d29668870bdace611e37f23` | `b68181e4 → 7a225223 → main` | ACCEPTED | Repository ADR acceptance/status mechanism; current GOV process declares merge as ADR acceptance, but independent competent approval evidence is not established | LOW internally; HIGH at identifier level because another ADR-001 exists |
| A02 | `adrs/ADR-001_DOCUMENT_MODEL.md` | Document Model — ARC → SPEC → APS | `3c68a36bdb464b1a2f3edc81cab282b7850de02d` | `66083e286a2fc33e70ccab4d1df6015ec0be65fd` | `3c68a36b → c4ba2150 → main` | PROPOSED | Explicit Protocol Custodian approval; acceptance line + merge required; no executed approval evidenced | HIGH |
| A03 | `docs/adr/001-document-model.md` | Document Model — ARC → SPEC → APS (duplicate representation) | `c4ba21506066f873ac574edb01ddba679feb4142` | `340ed584082baf5353ce0496034484ab6379ac45` | direct child of `3c68a36b` / same Document Model lineage | DRAFT | Protocol Custodian + Architecture Board approval checklist and acceptance procedure; no executed approval evidenced | HIGH |

## 5. Current-Main Search Hits — Reference Classification

| Ref | Path | Occurrence type | Intended referent | Introducing commit | Current blob | Branch ancestry | Authority dependency | Ambiguity |
|---|---|---|---|---|---|---|---|---|
| R01 | `adrs/README.md` | Index/link | A01 — Repository Structure | inherited with repository structure lineage; exact introduction commit not independently re-derived in this pass | current-main blob not independently recorded here | main | ADR index/status | LOW |
| R02 | `releases/v0.1.0/RELEASE_NOTES.md` | Release inventory | A01 — Repository Structure | release artifact lineage; exact introduction commit not independently re-derived in this pass | current-main blob not independently recorded here | main | Release publication status | LOW |
| R03 | `releases/v0.1.0/DOCUMENT_STATUS.md` | Document status registry | A01 — Repository Structure | release artifact lineage; exact introduction commit not independently re-derived in this pass | current-main blob not independently recorded here | main | Declared ACCEPTED status | LOW |
| R04 | `STYLE_GUIDE.md` | Naming example | NONE — example only | not applicable | current-main blob not independently recorded here | main | None | NONE |
| R05 | `aps/APS-000_FOUNDATION_AND_TERMINOLOGY.md` | Identifier example + uniqueness rule | NONE — example only; materially constrains A01/A02/A03 because it states identifiers MUST NOT be reused | APS-000 lineage; exact introduction commit not independently re-derived in this pass | current-main blob not independently recorded here | main | APS identifier-governance rule; authority of that rule remains separately assessed | NONE as referent; HIGH as conflict impact |
| R06 | `AURA-DOCUMENTATION-NORMALIZATION-AUDIT-v1.md` | Forensic evidence inventory | A01 + A02 + A03 | normalization audit lineage | current-main blob not independently recorded here | main | Explicitly read-only / no authority | LOW as referent; HIGH as evidence impact |
| R07 | `AURA-DOCUMENTATION-NORMALIZATION-CONTROL-REVIEW-v1.md` | Forensic/control-review evidence | A01 + A02 + A03 | normalization control-review lineage | current-main blob not independently recorded here | main | Explicitly read-only / no authority | LOW as referent; HIGH as evidence impact |
| R08 | `ck003/handover-assessment/05_EVIDENCE_GAPS.md` | Explicit collision finding | A01 + A02 + A03 | CK003 handover lineage | current-main blob not independently recorded here | main | None; evidence/routing only | NONE; occurrence explicitly disambiguates three files |
| R09 | `ck003/handover-assessment/09_RECOMMENDED_SEQUENCE.md` | Recommended validation target | A01 + A02 + A03 | CK003 handover lineage | current-main blob not independently recorded here | main | None; non-normative recommendation | NONE; occurrence explicitly says three files claim ADR-001 |
| R10 | `AURA Protocol Specification APS-000 — Foundation &_260723_191759.txt` | Identifier example | NONE — example only | legacy source lineage; exact introduction commit not independently re-derived in this pass | current-main blob not independently recorded here | main | None as referent | NONE as referent |

## 6. What Is Actually Contaminated by the Collision

### 6.1 Identifier namespace

`APS-000` explicitly states that every identifier MUST be unique and that identifiers MUST NOT be reused. The current tree nevertheless contains three concrete artifacts bearing `ADR-001`. Therefore the collision is directly relevant to identifier integrity, independently of whether any one artifact is authoritative.

### 6.2 ADR indexing / repository navigation

`adrs/README.md` indexes `ADR-001` as Canonical Repository Structure, while the repository also contains two Document Model artifacts carrying the same identifier. The index therefore resolves the identifier to A01 only; it does not resolve the duplicate subject representations.

### 6.3 Release/status interpretation

The v0.1.0 release/status artifacts associate `ADR-001` with Repository Structure. This creates a historical release-level referent for the identifier, but does not by itself establish authority over the later Document Model use.

### 6.4 Document-model authority claims

A02 explicitly makes Protocol Custodian approval a prerequisite for acceptance. A03 carries the same subject and an acceptance checklist. Neither is evidenced as independently accepted. Therefore the collision does not establish that the Document Model was adopted; it establishes that two unaccepted representations use the identifier already used by A01.

### 6.5 Forensic / governance claims

R06–R09 correctly treat the three-way collision as an evidence/control issue. Their occurrences are not themselves authority-bearing decisions and therefore do not resolve the collision.

### 6.6 Traceability

Any downstream reference using bare `ADR-001` without path/subject disambiguation is not safely resolvable from the current tree alone. References that explicitly point to `ADR-001_REPOSITORY_STRUCTURE.md` resolve to A01; references embedded in Document Model material resolve to A02/A03 only where the local document subject makes that intent explicit.

## 7. Authority Impact Matrix

| Authority / decision surface | Collision impact | Resolution state |
|---|---|---|
| Repository Structure ADR acceptance | A01 declares ACCEPTED | ACCEPTED is repository state; independent approval evidence NOT ESTABLISHED |
| Document Model ADR acceptance | A02 requires Protocol Custodian approval | NOT ESTABLISHED |
| Document Model duplicate acceptance | A03 requires approval and acceptance procedure | NOT ESTABLISHED |
| ADR index | Points `ADR-001` to A01 | Internally determinate, globally collision-prone |
| Identifier uniqueness / INV-DOC-005 | Three concrete artifacts use ADR-001 | CONFLICTED at repository state level |
| Governance ADR process | Defines merge/acceptance mechanism | Declared mechanism; independent ratification evidence not established |
| Release v0.1.0 status | Identifies ADR-001 with A01 | Historical referent established; does not adjudicate A02/A03 |
| Forensic records | Explicitly inventory collision | EVIDENCE ONLY; no authority |

## 8. Branch-Ancestry Finding

The load-bearing genealogy is:

```text
Repository Structure ADR
  b68181e48a65ed3a96007b5f3f89bad20a1caabf
        ↓
  later repository lineage
        ↓
  main / 71133de047c71e0bc1156d58c20396fe593ace70

Document Model ADR
  3c68a36bdb464b1a2f3edc81cab282b7850de02d
        ↓ direct parent relation
  c4ba21506066f873ac574edb01ddba679feb4142
        ↓
  main / 71133de047c71e0bc1156d58c20396fe593ace70
```

The Document Model duplicate is therefore a representation in the Document Model lineage, not evidence of a supersession of the Repository Structure ADR. No explicit supersedes/superseded-by relation resolving the identifier collision was found in the examined artifacts.

## 9. Determination

`ADR-001` collision is **propagating, not local**.

The collision touches at least four distinct control surfaces:

1. identifier uniqueness;
2. ADR indexing and release/status references;
3. Document Model authority/acceptance claims;
4. traceability and forensic resolution.

The mechanically supported conclusion is:

`SD-045 = CONFLICTED / OPEN`

The matrix does **not** establish a winning ADR-001, supersession, ratification, or normative authority.

## 10. Stage 07 Effect

- Stage 06: CLOSED.
- Stage 07 evidence pass: COMPLETE.
- Stage 07 formal closure: BLOCKED by unresolved authority and identifier conflict.
- SD-045: CONFLICTED / OPEN.
- Stage 08: NOT AUTHORIZED.

## 11. Evidence Basis

Primary current-main artifacts examined:

- `adrs/ADR-001_REPOSITORY_STRUCTURE.md`
- `adrs/ADR-001_DOCUMENT_MODEL.md`
- `docs/adr/001-document-model.md`
- `adrs/README.md`
- `releases/v0.1.0/RELEASE_NOTES.md`
- `releases/v0.1.0/DOCUMENT_STATUS.md`
- `STYLE_GUIDE.md`
- `aps/APS-000_FOUNDATION_AND_TERMINOLOGY.md`
- `AURA-DOCUMENTATION-NORMALIZATION-AUDIT-v1.md`
- `AURA-DOCUMENTATION-NORMALIZATION-CONTROL-REVIEW-v1.md`
- `ck003/handover-assessment/05_EVIDENCE_GAPS.md`
- `ck003/handover-assessment/09_RECOMMENDED_SEQUENCE.md`
- `AURA Protocol Specification APS-000 — Foundation &_260723_191759.txt`

The repository search returned 13 files containing `ADR-001`; the matrix classifies the 10 entries represented by the compact search output available in this pass. The three concrete ADR-001 representations are fully resolved by path, subject, introducing commit, and current blob. Exact current blobs/introduction commits for non-ADR reference artifacts are intentionally not invented where this pass did not independently re-derive them.

## 12. Non-Resolution Boundary

This artifact does not:

- rename or edit ADRs;
- choose A01, A02, or A03 as canonical;
- declare A01 superseded;
- declare A02/A03 accepted;
- establish Protocol Custodian or Architecture Board approval;
- alter APS/SPEC/ARC semantics;
- authorize Stage 08.
