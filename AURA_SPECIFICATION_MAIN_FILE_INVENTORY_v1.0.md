# AURA Specification — Main Branch File Inventory v1.0

## Status

**Artifact type:** Forensic reconstruction / inventory
**Scope:** `Aura-IDToken/aura-specification` → `main`
**Purpose:** Establish a file-level inventory before any normative reconciliation or redesign.

## Method

For every artifact, the reconstruction records, where Git evidence permits:

- repository path;
- artifact type / role;
- artifact timestamp encoded in filename or document, when present;
- first confirmed Git appearance;
- last confirmed Git modification;
- branch provenance;
- semantic function;
- relationships to other artifacts;
- authority basis/status only when supported by repository evidence.

**Important:** filename timestamps are not treated as Git timestamps. The current `main` HEAD is commit `71133de047c71e0bc1156d58c20396fe593ace70`, created `2026-09-10T22:09:45Z`, and its message explicitly records a revert of DQ-003 reconciliation commit `74220d27f6af01f335fb1423886a51eb063f90f7`. Therefore current `main` is a historical snapshot, not a complete representation of every artifact that existed during repository history.

## Main HEAD

- Branch: `main`
- Commit: `71133de047c71e0bc1156d58c20396fe593ace70`
- Commit date: `2026-09-10T22:09:45Z`
- Tree: `bb64ae436c9bc9fab8a8e2dd597aeadf27e39e91`
- Commit message: `Revert "docs(dq-003): specification reconciliation control record (#34)" (#43)`
- Parent: `74220d27f6af01f335fb1423886a51eb063f90f7`

## Evidence rule

This inventory deliberately does **not** infer that presence on `main` makes a document normative. Normative effect is a separate field to be established from the document's own status language, governance records, approvals, decisions, and history.

---

## 1. Root-level artifacts

| Path | Function | Artifact timestamp | Git history status |
|---|---|---|---|
| `.github/CODEOWNERS` | Repository ownership / review routing control | none | Present on main; exact first/last commit requires history walk |
| `.github/ISSUE_TEMPLATE/rfc_proposal.md` | Template for RFC proposals | none | Present on main; exact first/last commit requires history walk |
| `.github/ISSUE_TEMPLATE/specification_gap.md` | Template for specification-gap reports | none | Present on main; exact first/last commit requires history walk |
| `.github/PULL_REQUEST_TEMPLATE/pull_request_template.md` | PR submission structure | none | Present on main; exact first/last commit requires history walk |
| `APS-100 — Protocol Invariants_260723_192315.pdf` | Historical/reference representation of APS-100 | 2026-07-23 19:23:15 | Present on main |
| `APS-100 — Protocol Invariants_260723_192315.txt` | Text representation/extraction of APS-100 | 2026-07-23 19:23:15 | Present on main |
| `APS-200 — Canonical Data Model_260723_192852.pdf` | Historical/reference representation of APS-200 | 2026-07-23 19:28:52 | Present on main |
| `APS-200 — Canonical Data Model_260723_192852.txt` | Text representation/extraction of APS-200 | 2026-07-23 19:28:52 | Present on main |
| `APS-300 — Evidence Model_260723_193234.pdf` | Historical/reference representation of APS-300 | 2026-07-23 19:32:34 | Present on main |
| `APS-300 — Evidence Model_260723_193234.txt` | Text representation/extraction of APS-300 | 2026-07-23 19:32:34 | Present on main |
| `APS-400 — Conformance Test Matrix_260723_193617.pdf` | Historical/reference representation of APS-400 | 2026-07-23 19:36:17 | Present on main |
| `APS-400 — Conformance Test Matrix_260723_193617.txt` | Text representation/extraction of APS-400 | 2026-07-23 19:36:17 | Present on main |
| `APS-500 Reference Fixtures_260723_194023.pdf` | Historical/reference representation of APS-500 | 2026-07-23 19:40:23 | Present on main |
| `APS-500 Reference Fixtures_260723_194023.txt` | Text representation/extraction of APS-500 | 2026-07-23 19:40:23 | Present on main |
| `APS-900 — Compliance Mapping_260723_194128.pdf` | Historical/reference representation of APS-900 | 2026-07-23 19:41:28 | Present on main |
| `APS-900 — Compliance Mapping_260723_194128.txt` | Text representation/extraction of APS-900 | 2026-07-23 19:41:28 | Present on main |
| `APS-950 — Reference Implementation Requirements_260723_194507.pdf` | Historical/reference representation of APS-950 | 2026-07-23 19:45:07 | Present on main |
| `APS-950 — Reference Implementation Requirements_260723_194507.txt` | Text representation/extraction of APS-950 | 2026-07-23 19:45:07 | Present on main |
| `AURA Constitution_260723_190157.pdf` | Historical/reference representation of AURA Constitution | 2026-07-23 19:01:57 | Present on main |
| `AURA Constitution_260723_190157.txt` | Text representation/extraction of AURA Constitution | 2026-07-23 19:01:57 | Present on main |
| `AURA Protocol Specification APS-000 — Foundation &_260723_191759.pdf` | Historical/reference representation of APS-000 | 2026-07-23 19:17:59 | Present on main |
| `AURA Protocol Specification APS-000 — Foundation &_260723_191759.txt` | Text representation/extraction of APS-000 | 2026-07-23 19:17:59 | Present on main |
| `AURA-DOCUMENTATION-NORMALIZATION-AUDIT-v1.md` | Documentation normalization audit/control artifact | none | Present on main |
| `AURA-DOCUMENTATION-NORMALIZATION-CONTROL-REVIEW-v1.md` | Documentation normalization control review | none | Present on main |
| `CHANGELOG.md` | Repository change history/documentation | none | Present on main |
| `CODE_OF_CONDUCT.md` | Contributor conduct policy | none | Present on main |
| `CONTRIBUTING.md` | Contribution workflow | none | Present on main |
| `GOVERNANCE.md` | Repository/project governance | none | Present on main |
| `LICENSE` | Repository license | none | Present on main |
| `README.md` | Repository entry point / orientation | none | Present on main |
| `ROADMAP.md` | Planned specification/project progression | none | Present on main |
| `SECURITY.md` | Security reporting/policy | none | Present on main |
| `STYLE_GUIDE.md` | Documentation/style rules | none | Present on main |
| `VERSIONING.md` | Versioning rules | none | Present on main |

## 2. APS working set on main

| Path | Function | Current role |
|---|---|---|
| `aps/APS-000_FOUNDATION_AND_TERMINOLOGY.md` | Foundation and controlled terminology | Definition layer |
| `aps/APS-100_PROTOCOL_INVARIANTS.md` | Protocol invariants | Invariant layer |
| `aps/APS-200_CANONICAL_DATA_MODEL.md` | Canonical entities, object contract, serialization/hash model | Data/canonicalization layer |
| `aps/APS-300_EVIDENCE_MODEL.md` | Evidence objects, evidence integrity, evidence chain | Evidence layer |
| `aps/APS-400_CONFORMANCE_TEST_MATRIX.md` | Conformance requirements matrix | Conformance layer |
| `aps/APS-500_REFERENCE_FIXTURES.md` | Reference fixture structure and expected vectors | Fixture layer |
| `aps/APS-900_COMPLIANCE_MAPPING.md` | Traceability/compliance mapping across specification and evidence | Traceability layer |
| `aps/APS-950_REFERENCE_IMPLEMENTATION_REQUIREMENTS.md` | Requirements for reference implementations | Implementation-assurance boundary |
| `aps/EVENT_TYPE_REGISTRY.md` | Registry of event types used by canonical/event model | Registry |
| `aps/README.md` | Orientation for APS directory | Directory index |

## 3. Conformance working set on main

The main branch contains dedicated `CONF-*` artifacts. Their function is to turn specification requirements into individually addressable conformance conditions.

| Path | Function |
|---|---|
| `conformance/CONF-001_DETERMINISTIC_EVALUATION.md` | Deterministic evaluation conformance condition |
| `conformance/CONF-002_REPLAY_VERIFICATION.md` | Replay verification condition |
| `conformance/CONF-003_CANONICAL_SERIALIZATION.md` | Canonical serialization condition |
| `conformance/CONF-004_EVIDENCE_INTEGRITY.md` | Evidence integrity condition |
| `conformance/CONF-005_TRACEABILITY.md` | Traceability condition |
| `conformance/CONF-006_PLATFORM_INDEPENDENCE.md` | Platform-independence condition |
| `conformance/CONF-007_FAIL_CLOSED.md` | Fail-closed behavior condition |
| `conformance/CONF-008_VERSION_COMPATIBILITY.md` | Version compatibility condition |
| `conformance/CONF-009_EVIDENCE_COMPLETENESS.md` | Evidence completeness condition |
| `conformance/CONF-010_CRYPTOGRAPHIC_VERIFICATION.md` | Cryptographic verification condition |
| `conformance/CONF-011_ZERO_FLOAT_RUNTIME.md` | Zero-float runtime condition |
| `conformance/CONF-012_AUDITABILITY.md` | Auditability condition |
| `conformance/CONF-013_POLICY_DETERMINISM.md` | Policy determinism condition |

## 4. ADR layer

The main tree contains at least:

| Path | Function |
|---|---|
| `adrs/ADR-001_DOCUMENT_MODEL.md` | Decision record for document model |
| `adrs/ADR-001_REPOSITORY_STRUCTURE.md` | Decision record for repository structure |
| `adrs/README.md` | ADR directory orientation |

ADR artifacts must be treated separately from APS normative content: an ADR records a decision/rationale; it does not automatically become a protocol invariant merely by existing.

## 5. Relationship model

The current main tree supports the following **structural** relationship model; authority remains a separate forensic question:

```text
AURA Constitution
       ↓
APS-000 Foundation / Terminology
       ↓
APS-100 Protocol Invariants
       ↓
APS-200 Canonical Data Model
       ├──────────────→ APS-300 Evidence Model
       ├──────────────→ APS-400 Conformance Matrix
       └──────────────→ APS-500 Reference Fixtures
                         ↓
                    CONF-xxx artifacts

APS-900 Compliance Mapping
       ↕
Constitution / APS / INV / ENT / Evidence / CONF / FIX / RI

APS-950 Reference Implementation Requirements
       ↓
Reference implementation conformance boundary

ADRs / GOVERNANCE / VERSIONING / CONTRIBUTING / templates
       ↓
Process and control environment
```

## 6. Known historical event affecting current main

Commit `74220d27f6af01f335fb1423886a51eb063f90f7` on 2026-09-10 22:09:10Z added a DQ-003 specification reconciliation control record and an APS-200 sections 6–10 reference audit. Commit `71133de047c71e0bc1156d58c20396fe593ace70`, 35 seconds later, reverted that commit. This means a file/version can have existed in Git history without being present in the current main tree.

## 7. Forensic status

This document is an **inventory baseline**, not a final authority map.

Remaining required work:

1. recursively enumerate every tree under main;
2. resolve exact first appearance and last modification commit for every blob;
3. capture full content for every text artifact and metadata for binary artifacts;
4. reconstruct file-to-file references;
5. reconstruct semantic deltas across commits;
6. map each artifact to branch provenance;
7. classify authority only from evidence;
8. write the resulting master map into the Crystal-panel repository without altering the source repository.

## Source repository

`https://github.com/Aura-IDToken/aura-specification`

## Target repository

`https://github.com/vaidt/Crystal-panel-Aura-Protection`
