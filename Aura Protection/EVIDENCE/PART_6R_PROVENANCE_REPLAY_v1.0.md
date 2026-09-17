# AURA PART 6R — PROVENANCE REPLAY v1.0

**Record type:** Forensic provenance replay / evidence-containment report  
**Authority:** NONE  
**Normative effect:** NONE  
**Status:** COMPLETE — PROVENANCE REPLAY ONLY  
**Execution date:** 2026-09-17 UTC  
**Package:** `AURA-Part-6R-Evidence` v1.0  
**Package branch:** `forensics/part-6r-evidence-package`

## 1. Mandate

This artifact replays Custodian Part 6R using only the 15 evidence objects enumerated by `Aura Protection/EVIDENCE/MANIFEST.json`.

The replay answers:

1. whether each E1–E15 object is recoverable from the declared GitHub source;
2. whether the declared path and blob identity are consistent with the recovered object;
3. what provenance each object supplies;
4. what A01/A02/A03 identity, authority, acceptance and supersession evidence is actually present;
5. whether SD-045 can be resolved from E1–E15 without inference.

This replay does **not** create authority, select a canonical ADR-001, declare supersession, close SD-045, or authorize Stage 08.

## 2. Evidence-containment rule

Substantive findings in this report are restricted to E1–E15. No outside artifact is used to fill an evidence gap. Where E1–E15 contain a claim about an underlying event, that claim is reported as evidence contained in the object; it is not silently upgraded to independent authority.

The manifest itself states that its blob SHA is the Git object identity observed during mechanical recovery and that the package performs no semantic normalization or reconciliation. It also records retention of unresolved evidence without in-place mutation. [Manifest]

## 3. Mechanical recovery result

| ID | Source | Path | Declared blob | Recovery | Provenance disposition |
|---|---|---|---|---|---|
| E1 | `vaidt/Crystal-panel-Aura-Protection` | `14_FORENSICS/07_ADR001_SUPERSESSION_AUTHORITY_PATH_RECONSTRUCTION_v1.0.md` | `638bb716060216a3df6d47dab62741c23c57e1f9` | RECOVERED | VALID SOURCE OBJECT |
| E2 | `vaidt/Crystal-panel-Aura-Protection` | `14_FORENSICS/07_ADR001_SD045_CLOSURE_GATE_v1.0.md` | `00b3800f2377d1e0cf5d9df9c195ab836c2a3ebb` | RECOVERED | VALID SOURCE OBJECT |
| E3 | `vaidt/Crystal-panel-Aura-Protection` | `14_FORENSICS/07_AUTHORITY_EVIDENCE_RECORD_ADR001_COLLISION_v1.0.md` | `6eb4898b27510db25f7f41048c1a03624e39323f` | RECOVERED | VALID SOURCE OBJECT |
| E4 | `vaidt/Crystal-panel-Aura-Protection` | `14_FORENSICS/07_AUTHORITY_REENTRY_ADR001_COLLISION_v1.0.md` | `22575d167695bf089ea724bdf9bb8e81931e70f9` | RECOVERED | VALID SOURCE OBJECT |
| E5 | `Aura-IDToken/aura-specification` | `adrs/ADR-001_REPOSITORY_STRUCTURE.md` | `3df6315b5b9883753d29668870bdace611e37f23` | RECOVERED | VALID SOURCE OBJECT |
| E6 | `Aura-IDToken/aura-specification` | `adrs/ADR-001_DOCUMENT_MODEL.md` | `66083e286a2fc33e70ccab4d1df6015ec0be65fd` | RECOVERED | VALID SOURCE OBJECT |
| E7 | `Aura-IDToken/aura-specification` | `docs/adr/001-document-model.md` | `340ed584082baf5353ce0496034484ab6379ac45` | RECOVERED | VALID SOURCE OBJECT |
| E8 | `Aura-IDToken/aura-specification` | `GOVERNANCE.md` | `38acf33e95a8803f2f0a606f3f73c964aeb871bf` | RECOVERED | VALID SOURCE OBJECT |
| E9 | `Aura-IDToken/aura-specification` | `adrs/README.md` | `8f7e55d01cbbc46f4f15e0cd60d49433e75930` | RECOVERED | VALID SOURCE OBJECT |
| E10 | `Aura-IDToken/aura-specification` | `releases/v0.1.0/DOCUMENT_STATUS.md` | `08f4e0ceec088d9ca17b21e2a5957ebfa16bb6a3` | RECOVERED | VALID SOURCE OBJECT |
| E11 | `Aura-IDToken/aura-specification` | `releases/v0.1.0/RELEASE_NOTES.md` | `5b00d70e41fc0864aa9c37f2a4f6d6583ad3394d` | RECOVERED | VALID SOURCE OBJECT |
| E12 | `Aura-IDToken/aura-specification` | `ck003/handover-assessment/05_EVIDENCE_GAPS.md` | `3e32b9e541a5a6ee2fd0eeafc5aed4e4c7b6c675` | RECOVERED | VALID SOURCE OBJECT |
| E13 | `Aura-IDToken/aura-specification` | `ck003/handover-assessment/09_RECOMMENDED_SEQUENCE.md` | `f0e47faae58eb09b929cd69d9889aaabe353940c` | RECOVERED | VALID SOURCE OBJECT |
| E14 | `Aura-IDToken/aura-specification` | `AURA-DOCUMENTATION-NORMALIZATION-AUDIT-v1.md` | `00bcda956f9de2473d361a928ff7a7da7e2f5aee` | RECOVERED | VALID SOURCE OBJECT |
| E15 | `vaidt/Crystal-panel-Aura-Protection` | `14_FORENSICS/07_AUTHORITY_ACT_REGISTER_v1.0.md` | `c93b5c95c809bd7bd47297c273fe493e1b5d6726` | RECOVERED | VALID SOURCE OBJECT |

**Recovery count: 15/15.**

## 4. Provenance matrix — semantic use of E1–E15

| ID | Primary evidentiary role | Provenance-bearing facts | Authority character |
|---|---|---|---|
| E1 | A01/A02/A03 genealogy + authority-path reconstruction | Identifies three representations; records introducing commits, dates, parents, PR #5/#10, statuses, acceptance requirements, supersession search and current SD-045 disposition. | FORENSIC / NON-AUTHORITY |
| E2 | SD-045 closure-gate replay | Defines G01–G11; genealogy passes; supersession, revocation, acceptance and collision-resolution criteria fail; gate remains open. | FORENSIC GATE / NON-AUTHORITY |
| E3 | Collision evidence record | Confirms three reachable ADR-001 representations with two subjects and divergent lifecycle states; records load-bearing identity conflict. | FORENSIC / NON-AUTHORITY |
| E4 | Stage 07 re-entry | Records re-entry sequence and current dispositions; states governance conflict remains open. | FORENSIC / NON-AUTHORITY |
| E5 | A01 source artifact | ADR-001 Repository Structure; ACCEPTED; 2026-07-23; `Supersedes: —`; `Superseded By: —`. | SOURCE ARTIFACT; STATUS SELF-DECLARATION |
| E6 | A02 source artifact | ADR-001 Document Model; PROPOSED; Decision Owner Protocol Custodian; explicit `Accepted-by` + merge requirement. | SOURCE ARTIFACT; PROPOSED |
| E7 | A03 source artifact | ADR-001 Document Model duplicate; DRAFT; explicit `accepted_by` + merge requirement. | SOURCE ARTIFACT; DRAFT |
| E8 | Governance mechanism | GOV-001 is `1.0-DRAFT`; defines hierarchy and says merging a PR = accepting an ADR; AI assistants may not approve/freeze. | DECLARED GOVERNANCE; NOT INDEPENDENTLY RATIFIED IN E1–E15 |
| E9 | ADR index/process | Lists ADR-001 as Repository Structure / ACCEPTED and states merging = accepting. | INDEX / PROCESS DECLARATION |
| E10 | Release status snapshot | v0.1.0 lists Repository Structure ADR ADR-001 1.0 ACCEPTED. | HISTORICAL STATUS SNAPSHOT |
| E11 | Release provenance | v0.1.0 published 2026-07-23; says initial release establishes canonical documentation structure and includes ADR-001 repository-structure decision. | RELEASE RECORD |
| E12 | Independent evidence-gap context | Records identifier collision: three files claim ADR-001; also records missing machine verification and governance gaps. | NON-NORMATIVE EVIDENCE |
| E13 | Recommended sequence | Explicitly says it authorizes nothing; Step 0 requires a human ruling on cross-corpus precedence; notes identifier uniqueness should catch three ADR-001 files. | RECOMMENDATION / NON-AUTHORITY |
| E14 | Independent normalization audit | Read-only diagnostic; inventories A01/A02/A03 as AD-I-007/008/009 and records the collision and authority-evidence state. | OBSERVATIONAL AUDIT / NON-AUTHORITY |
| E15 | Authority-act register | Separates repository events from authority acts; classifies bootstrap and other claims; records no independent approval for embedded authority declarations. | FORENSIC REGISTER / NON-AUTHORITY |

## 5. A01 — identity replay

**Referent:** `adrs/ADR-001_REPOSITORY_STRUCTURE.md`

| Field | Replay result |
|---|---|
| Identifier | `ADR-001` |
| Subject | Canonical Repository Structure |
| Path | `adrs/ADR-001_REPOSITORY_STRUCTURE.md` |
| Blob | `3df6315b5b9883753d29668870bdace611e37f23` |
| Introducing commit | `b68181e48a65ed3a96007b5f3f89bad20a1caabf` |
| Commit date | `2026-07-23T21:03:00Z` |
| Parent | `7a22522350a0e917fa773d724854796778623147` |
| PR / merge | PR #5; merge `93f677fe34bf3f3fe0e8abffd6c8fdfd92b7958f`; merged 2026-07-23T21:06:21Z |
| Declared status | `ACCEPTED` |
| Decision owner | Not stated as Protocol Custodian in E5 |
| Supersession fields | `Supersedes: —`; `Superseded By: —` |
| Acceptance evidence | Repository merge + self-declared ACCEPTED status; no separate competent approval act established in E1/E3/E15 |
| Revocation evidence | None located in E1/E2/E3/E4/E15 |
| Supersession evidence | None located; disposition `UNPROVEN` |
| Authority result | Repository-state acceptance is evidenced; independent ratification is **not established** |

E5 directly establishes the artifact identity/status and absence of supersession markers. E1/E3/E4 preserve the genealogy and authority-path interpretation. E15 explicitly warns against treating repository merge/status alone as an independently evidenced authority act.

## 6. A02 — identity replay

**Referent:** `adrs/ADR-001_DOCUMENT_MODEL.md`

| Field | Replay result |
|---|---|
| Identifier | `ADR-001` |
| Subject | Document Model — ARC → SPEC → APS |
| Path | `adrs/ADR-001_DOCUMENT_MODEL.md` |
| Blob | `66083e286a2fc33e70ccab4d1df6015ec0be65fd` |
| Introducing commit | `3c68a36bdb464b1a2f3edc81cab282b7850de02d` |
| Commit date | `2026-08-02T19:10:34Z` |
| Parent | `812598e349bd830d688f3e9e4ba728e29a645a7d` |
| PR / merge | No associated PR established in the E1 replay record |
| Declared status | `PROPOSED` |
| Decision owner | `Protocol Custodian` |
| Acceptance condition | `Accepted-by: <Protocol Custodian>` + merge into canonical branch |
| Acceptance evidence | No executed `Accepted-by` evidence in E6; E1/E3/E4 classify acceptance as not evidenced |
| Revocation evidence | None located in E1/E2/E3/E4/E15 |
| Supersession evidence | None establishing A02 supersedes A01 |
| Authority result | `NOT ACCEPTED / ACCEPTANCE NOT EVIDENCED` |

E6 is explicit that the ADR remains PROPOSED and requires explicit Protocol Custodian approval. This replay does not substitute E8's generic merge rule for E6's local acceptance requirement.

## 7. A03 — identity replay

**Referent:** `docs/adr/001-document-model.md`

| Field | Replay result |
|---|---|
| Identifier | `ADR-001` |
| Subject | Document Model — ARC → SPEC → APS |
| Path | `docs/adr/001-document-model.md` |
| Blob | `340ed584082baf5353ce0496034484ab6379ac45` |
| Introducing commit | `c4ba21506066f873ac574edb01ddba679feb4142` |
| Commit date | `2026-08-02T19:31:16Z` |
| Parent | `3c68a36bdb464b1a2f3edc81cab282b7850de02d` |
| PR / merge | PR #10; merge `c4ba21506066f873ac574edb01ddba679feb4142` |
| Declared status | `DRAFT` |
| Decision owner | `Protocol Custodian` |
| Acceptance condition | `accepted_by` + merge before ACCEPTED |
| Acceptance evidence | No executed `accepted_by` evidence in E7; PR merge exists but artifact remains DRAFT |
| Revocation evidence | None located in E1/E2/E3/E4/E15 |
| Supersession evidence | No explicit supersession relation established |
| Authority result | `NOT ACCEPTED / ACCEPTANCE NOT EVIDENCED` |

E7 and E1/E3/E4 establish that PR #10 merge proves repository integration but does not by itself resolve the artifact's explicit acceptance condition.

## 8. Identity collision replay

E1, E3 and E4 establish the following mechanically relevant relation:

```text
A01
ADR-001 / Repository Structure
2026-07-23
        │
        │ later main lineage
        ▼
A02
ADR-001 / Document Model
2026-08-02 19:10Z
        │
        │ direct parent
        ▼
A03
ADR-001 / Document Model duplicate
2026-08-02 19:31Z
```

This proves coexistence and ancestry. It does not prove supersession.

The three representations have:

- one identifier: `ADR-001`;
- two subjects: Repository Structure and Document Model;
- three paths/blobs;
- three lifecycle declarations: ACCEPTED / PROPOSED / DRAFT;
- no explicit supersession relation resolving the collision;
- no independently evidenced competent acceptance of A02/A03 within E1–E15.

## 9. Governance-rule replay

E8 states:

- `GOV-001` is `1.0-DRAFT`;
- the hierarchy names Chief Architect, Architecture Review Board, contributors and AI assistants;
- AI assistants may not approve or freeze;
- §6 says `Merging the PR = accepting the ADR` and ADR status is set to ACCEPTED.

E6 and E7 separately impose explicit Protocol Custodian acceptance conditions on the Document Model representations.

E1/E4 explicitly record that no independent evidence in the examined pass reconciles these acceptance mechanisms for ADR-001.

**Replay result:** the evidence set establishes a governance-rule collision/interaction, not a resolved authority rule for A02/A03.

## 10. Acceptance replay

### A01

- Repository merge: evidenced.
- Artifact status ACCEPTED: evidenced as source declaration.
- Independent competent approval: **not established** by E1–E15.

### A02

- Artifact status PROPOSED: evidenced.
- Required Protocol Custodian acceptance: **not evidenced**.
- Merge satisfying acceptance: **not established**; no executed `Accepted-by` line exists in E6.

### A03

- PR #10 merge: evidenced.
- Artifact status DRAFT: evidenced.
- Required `accepted_by`: **not evidenced**.
- Therefore executed acceptance is not established from E1–E15.

## 11. Supersession / revocation replay

The evidence set contains no explicit authority act establishing:

1. A01 superseded by A02;
2. A01 superseded by A03;
3. A02 superseded by A03;
4. A01 revoked;
5. ADR-001 reassigned from Repository Structure to Document Model;
6. either Document Model representation promoted as the replacement by competent authority.

Later chronology, direct parentage, path changes, semantic similarity, and status differences are retained as genealogy/lifecycle evidence only. They are not converted into supersession.

**Supersession:** `UNPROVEN`  
**Revocation:** `UNPROVEN`

## 12. SD-045 replay

| Criterion | Result from E1–E15 |
|---|---|
| Three identities/path/blob objects established | PASS |
| A01 genealogy | PASS |
| A02 genealogy | PASS |
| A03 genealogy + PR/merge | PASS |
| Explicit A01→A02 supersession | FAIL / NOT FOUND |
| Explicit A01→A03 supersession | FAIL / NOT FOUND |
| Explicit A01 revocation | FAIL / NOT FOUND |
| A02 Protocol Custodian acceptance | FAIL / NOT FOUND |
| A03 Protocol Custodian acceptance | FAIL / NOT FOUND |
| Identifier reassignment authority act | FAIL / NOT FOUND |
| Collision resolvable without inference | FAIL |

**Replay disposition:** `SD-045 = CONFLICTED / OPEN`.

This matches E2's gate result and E4's re-entry result. E2 states that the evidence is sufficient for existence/genealogy/merge history but insufficient for valid supersession, revocation or competent acceptance resolving the collision.

## 13. Cross-source consistency

The 15-object set is internally consistent on the load-bearing finding:

- E5/E9/E10/E11 establish the early Repository Structure use of ADR-001 and its ACCEPTED declaration.
- E6 establishes the later Document Model use of ADR-001 as PROPOSED and its explicit acceptance condition.
- E7 establishes the second Document Model representation as DRAFT with its own acceptance condition.
- E1/E3/E4/E14 independently preserve the collision as a forensic finding rather than a resolved decision.
- E8 establishes a generic repository governance rule that interacts with, but does not independently reconcile, the Document Model acceptance condition.
- E15 explicitly separates repository events from authority acts.
- E12/E13 preserve the same collision/gap boundary and do not confer authority.

No E1–E15 object supplies the missing competent act that would change SD-045 to resolved.

## 14. Provenance integrity / contamination check

**Manifest identity:** package manifest declares all 15 IDs, source repository, path and blob identity.  
**Recovery:** all 15 declared objects were mechanically retrievable from the declared GitHub source.  
**Content normalization:** none performed for source identity.  
**Semantic reconciliation:** none performed on source artifacts.  
**External substitution:** none used to fill missing authority evidence.  
**Inference boundary:** chronology/ancestry/status are not promoted to authority or supersession.  
**Authority created by replay:** NONE.

## 15. Comparison with pre-replay state

The replay does not materially change the substantive Stage 07 finding. It upgrades the evidence-container state from “E1–E15 requested/recoverable” to **E1–E15 mechanically recovered and provenance-replayed**.

The load-bearing conclusion remains:

```text
A01 = ACCEPTED repository-state declaration
A02 = PROPOSED; Protocol Custodian acceptance not evidenced
A03 = DRAFT; acceptance not evidenced

Supersession = UNPROVEN
Revocation = UNPROVEN
Identifier reassignment = NOT EVIDENCED
SD-045 = CONFLICTED / OPEN
Stage 07 = OPEN
Stage 08 = NOT AUTHORIZED
```

## 16. Evidence-status counts

For this replay, the 15 evidence objects are classified by evidentiary role as follows:

- **Direct source artifacts / primary records:** E5, E6, E7, E8, E9, E10, E11 = 7
- **Forensic derived records:** E1, E2, E3, E4, E14, E15 = 6
- **Evidence-gap / recommendation records:** E12, E13 = 2
- **Total:** 15

These categories describe evidence role, not authority rank.

## 17. Final result

**PART 6R PROVENANCE REPLAY: COMPLETE**

The manifest's E1–E15 set has been mechanically recovered and replayed. The set is sufficient to establish provenance, identity, genealogy, lifecycle declarations, the repository merge events, and the existence of the ADR-001 collision. It is **not sufficient to establish the missing competent authority act** required to resolve SD-045.

Therefore:

```text
PROVENANCE = ESTABLISHED FOR E1–E15
IDENTITY = ESTABLISHED
GENEALOGY = ESTABLISHED
ACCEPTANCE A02 = NOT ESTABLISHED
ACCEPTANCE A03 = NOT ESTABLISHED
SUPERSESSION = UNPROVEN
REVOCATION = UNPROVEN
AUTHORITY RESOLUTION = NOT ESTABLISHED
SD-045 = CONFLICTED / OPEN
STAGE 07 = OPEN
STAGE 08 = NOT AUTHORIZED
```

This report is evidence-only and creates no normative effect.
