# AURA — PR GENEALOGY / FORENSIC BASELINE v1.0

**Repository source:** `Aura-IDToken/aura-specification`
**Registry:** `vaidt/Crystal-panel-Aura-Protection`
**Target layer:** `14_FORENSICS/`
**State:** ACTIVE — FORENSIC RECONSTRUCTION
**Authority created:** NONE
**Normative effect:** NONE
**Method:** evidence-first reconstruction

---

## 1. Cel

Ten artefakt zapisuje pierwszy kontrolowany rejestr genealogii Pull Requestów `#1–#43` repozytorium `Aura-IDToken/aura-specification`.

Nie rozstrzyga, który PR jest kanoniczny, finalny, nadrzędny, zatwierdzony ani superseded. Rejestruje wyłącznie to, co zostało zaobserwowane w historii GitHub oraz co wynika z deklaracji danego PR.

**Twarda reguła:** deklaracja w opisie PR nie jest sama w sobie dowodem authority. Status protokołu będzie ustalany dopiero przez połączenie:

`PR → HEAD → commit ancestry → tree → files → semantic delta → authority evidence`.

---

## 2. Źródło chronologii

Pobrano listę PR repozytorium przez GitHub API dla `state=all`, `sort=created`, `direction=asc`, `per_page=100`.

Źródło obejmuje PR-y `#1–#43`; w odpowiedzi wyszukiwarki nie pojawił się osobny PR `#36`, dlatego jego status pozostaje **UNRESOLVED / NOT YET RECONSTRUCTED**. Nie wolno zakładać, że PR #36 nie istniał wyłącznie na podstawie niepełnego wyniku wyszukiwania.

Dowód listy PR: fileciteturn123file0L1-L2

---

## 3. Chronologia PR

| PR | Tytuł / funkcja z rekordu | Wstępna klasyfikacja funkcjonalna | Status forensic |
|---:|---|---|---|
| #1 | `[WIP] Add complete documentation for APS and Constitution` | genesis corpus / initial APS + Constitution | RECONSTRUCT |
| #2 | `Add README.md with AuraProtocol org structure and migration status` | repository/org migration documentation | RECONSTRUCT |
| #3 | `Creating comprehensive documentation for APS and Constitution` | documentation generation / duplicate lineage candidate | RECONSTRUCT |
| #4 | `docs: fix documentation errors across all APS specification files` | documentation correction / normalization | RECONSTRUCT |
| #5 | `feat: build canonical repository structure for aura-specification` | repository structure + specification organization | RECONSTRUCT; do not infer canonical authority from title |
| #6 | `Add .github/CODEOWNERS` | governance / review control | RECONSTRUCT |
| #7 | `Revert "Add .github/CODEOWNERS"` | revert of #6 | RECONSTRUCT |
| #8 | `Add .github/CODEOWNERS file` | governance / review control | RECONSTRUCT |
| #9 | `Spec/sync arc spec 001` | specification synchronization | RECONSTRUCT |
| #10 | `adr: add ADR-001 to docs/adr/001-document-model.md...` | ADR/document model | RECONSTRUCT |
| #11 | `Draft SPEC-002 constitution artifact contract` | SPEC-002 draft contract | DRAFT CLAIMED; authority unresolved |
| #12 | `spec: tighten SPEC-002 Constitution Artifact Contract to v0.2-DRAFT` | SPEC-002 revision | DRAFT CLAIMED; authority unresolved |
| #13 | `docs(spec-002): SPEC-002 v0.3-DRAFT — Constitution Artifact Contract Tightening` | SPEC-002 revision | DRAFT CLAIMED; authority unresolved |
| #14 | `CK-003 DQ-002: establish Merkle hash-domain evidence` | evidence / DQ-002 | DRAFT / evidence-only claim to verify |
| #15 | `DRAFT: complete Aura specification and conformance closure` | completion workspace / APS-001 / closure plan | DRAFT / governance unresolved |
| #16 | `CK-003: establish controlled closure workspace` | closure workspace | RECONSTRUCT |
| #17 | `CK003: close DQ-006 and map INV-009 to CONF-008` | closure + mapping | declared closure; authority requires verification |
| #18 | `Ck003/closure workspace` | closure workspace | RECONSTRUCT |
| #19 | `Ck003/cross language 002` | cross-language evidence | RECONSTRUCT |
| #20 | `Ck003/dq 002 hash domain` | DQ-002 hash-domain evidence | RECONSTRUCT |
| #21 | `Ck003/dq 006 closure` | DQ-006 closure | RECONSTRUCT |
| #22 | `docs(ck003): HANDOVER-ASSESSMENT-001 — inherited-state assessment` | observational inherited-state assessment | NON-NORMATIVE by declaration |
| #23 | `CK-003/DQ-002: CROSS-LANGUAGE-002 evidence, independent oracle, defects` | independent evidence / oracle / defects | CONDITIONAL PASS by declaration; DQ-002 OPEN |
| #24 | `Ck003/dq 006 closure package` | closure package | RECONSTRUCT |
| #25 | `CK-003: reconcile APS-200 with DQ-006 and refresh closure controls` | specification reconciliation | controlled spec change; approval unresolved |
| #26 | `spec(dq-006): reconcile canonical serialization closure across APS-200/300, ADR, CONF-003` | normative serialization reconciliation | declared NORMATIVE; verdict internally says DQ-006 OPEN; authority must be separately proven |
| #27 | `CK-003: enforce DQ-006 final closure execution gate` | governance/execution gate | control only; no closure by declaration |
| #28 | `CK-003/DQ-002: CROSS-LANGUAGE-002 evidence, independent oracle, defects` | duplicate/parallel evidence lineage | RECONSTRUCT |
| #29 | `Claude/aura cross language 002 6t2kdo` | Claude evidence branch | RECONSTRUCT |
| #30 | `Spec/sync arc spec 001` | specification synchronization | RECONSTRUCT |
| #31 | `spec(p0-1): Canonical Representation Contract` | P0 canonical representation contract | declared protocol decision; evidence/authority unresolved |
| #32 | `spec(p0-2): Evidence / Hash Domain Contract` | P0 evidence/hash domains | explicit non-inference; authority unresolved |
| #33 | `docs(dq-003): specification reconciliation control record` | DQ-003 control record | non-normative by declaration |
| #34 | `docs(dq-003): specification reconciliation control record` | DQ-003 control record | later reverted; reconstruct both pre-revert and revert genealogy |
| #35 | `Claude/ri rs p01 handoff ga84l6` | RI-RS handoff | RECONSTRUCT |
| #36 | **NOT RESOLVED IN CURRENT SEARCH RESULT** | unknown | UNRESOLVED — must fetch directly by number/API |
| #37 | `Aura documentation normalization audit v1 (read-only, observational)` | observational normalization audit | non-normative by declaration |
| #38 | `Aura documentation normalization control review v1 (read-only, controlled analysis)` | controlled analysis / identity + lineage review | non-normative by declaration |
| #39 | `govern(Q1): place Chief Architect -> Custodian Scope Bridge (non-binding)` | governance instrument placement | non-binding preparation by declaration |
| #40 | `govern(Q1): place Chief Architect approval/delegation record (unexecuted)` | governance instrument placement | approval unexecuted by declaration |
| #41 | `Prepare Chief Architect jurisdictional instruments for Q1 Scope Bridge` | governance preparation | RECONSTRUCT |
| #42 | `Prepare Chief Architect jurisdictional instruments for Q1 Scope Bridge` | governance preparation | RECONSTRUCT |
| #43 | `Revert "docs(dq-003): specification reconciliation control record"` | revert of #34 | REVERT EVENT — reconstruct exact tree and deleted artifacts |

---

## 4. Verified high-value milestones

### PR #1 — initial specification corpus

The PR was created `2026-07-23T18:17:09Z`, merged `2026-07-23T19:14:08Z`, with merge commit `10ee452d0f2ffded08bc952f97457f994113b47e`. Its head branch was `copilot/aura-specification`, head SHA `129e66cfeeb124dc7776658a464212f6137b4e88`.

This establishes the first observed repository-level specification import event. It does **not** by itself establish later canonical authority.

### PR #4 — normalization/correction pass

The PR description explicitly records correction of APS titles, addition of an APS-001 index row, removal of stray `text` artifacts from the TXT pipeline, a spacing correction in APS-300, and completion of CONF-009 invariant mapping.

This is a semantic/documentation correction event, not merely formatting noise. The exact file-level patch still has to be captured in the forensic file genealogy.

### PR #5 — repository restructuring

The PR description declares a production-grade normative documentation repository structure and introduces `/constitution`, `/specification`, `/aps`, `/invariants`, `/conformance`, `/compliance`, `/fixtures`, `/evidence`, `/adrs`, `/rfcs`, `/templates`, `/reference`, releases and governance controls.

The word **canonical** appears in the PR description as a repository-structure objective. Forensic status remains unresolved until commit ancestry, resulting tree, file content and authority evidence are examined.

### PR #13 — SPEC-002 v0.3-DRAFT

The declared semantic delta includes new provenance/determinism and dependency-closure requirements, tightened hash-domain and serialization wording, expanded negative integrity cases, and expanded acceptance/traceability sections.

The document remained explicitly DRAFT. Therefore this event is important as a specification evolution step, but not as an approved architectural decision.

### PR #23 / #28 — CROSS-LANGUAGE-002 evidence

The PR description declares an implementation-independent RFC-6962 oracle, edge-matrix fixtures, vector comparison, RI-PY/RI-RS evidence and three defects. It explicitly says the ADR remains PROPOSED and DQ-002 remains OPEN.

The duplicate PR lineage (#23 and #28) must be compared by HEAD/tree/blob identity rather than inferred from title similarity.

### PR #26 — DQ-006 / canonical serialization reconciliation

The PR description contains a substantial normative delta: APS-200 §8, APS-300 evidence hashes, CONF-003, ADR-CK003-DQ006, closure package and consistency scan. However, the same declaration states `DQ-006 = OPEN` because residual criteria remained unmet.

This is a critical forensic case: **normative-looking text, closure machinery, and unresolved governance state coexist in one change lineage**. It must not be collapsed into a simple “closed” status.

### PR #31 — P0-1

The PR declares RFC 8785/JCS as the normative JSON canonicalization profile and exact UTF-8 JCS bytes as the canonical boundary. It simultaneously states that DQ-006 evidence gates remain incomplete.

This is a key candidate transition from evidence/reconciliation toward explicit protocol contract. Authority must be proven independently.

### PR #32 — P0-2

The PR declares explicit hash domains for integrity, evidence, input/output and Merkle leaf/node, while deliberately refusing to infer the `previous_record_hash` mapping. This explicit non-inference is itself important forensic evidence: the author recognized a missing authority boundary rather than silently deriving semantics from implementation.

### PR #33/#34/#43 — DQ-003 and revert chain

PR #33 and #34 have effectively identical titles and declared scope. PR #34's resulting commit `74220d27f6af01f335fb1423886a51eb063f90f7` was later reverted by PR #43.

Known verified chain:

`PR #34 → commit 74220d27f6af01f335fb1423886a51eb063f90f7 → PR #43 → main commit 71133de047c71e0bc1156d58c20396fe593ace70`

The reverted commit added the DQ-003 specification reconciliation control record and APS-200 §6–10 reference audit. The current main state is the revert state. Therefore the DQ-003 artifact must be preserved as **historical/reverted evidence**, not erased from genealogy.

---

## 5. Current main endpoint relevant to genealogy

Current `main` HEAD:

`71133de047c71e0bc1156d58c20396fe593ace70`

Commit date:

`2026-09-10T22:09:45Z`

Message:

`Revert "docs(dq-003): specification reconciliation control record (#34)" (#43)`

The current main tree is therefore downstream of an explicit revert event. This is why `main` must not be treated as a lossless representation of all specification work.

---

## 6. Forensic interpretation rules

### 6.1 PR title is not status

Examples:

- `canonical`
- `final`
- `closure`
- `approval`
- `normative`

are labels in human-authored metadata. They are not sufficient evidence for status.

### 6.2 PR body is evidence of intent, not automatically evidence of authority

Statements such as `NORMATIVE`, `CLOSED`, `ACCEPTED`, `APPROVED`, `CANONICAL` require a separate authority chain.

### 6.3 Revert is not deletion from history

A reverted artifact remains part of AURA's actual evolution and must be represented in historical genealogy.

### 6.4 Duplicate PRs require object identity comparison

Two PRs with identical titles may be:

- identical snapshots,
- different commits with equivalent content,
- competing revisions,
- replays,
- or independent evidence packages.

The distinction must be established from HEAD/tree/blob/ancestry.

---

## 7. Required next forensic pass

This file is only the PR chronology baseline. The next pass must execute:

1. Fetch exact metadata for every PR `#1–#43`, including PR #36 directly.
2. Record `head SHA`, `base SHA`, `merge SHA`, creation/close/merge timestamps.
3. Record changed filenames for every PR.
4. Capture full diff/patch for every PR where feasible.
5. Resolve commit ancestry for every PR head and merge commit.
6. Deduplicate PRs by HEAD SHA and tree SHA while preserving all aliases.
7. Map every changed file to its first appearance and subsequent modifications.
8. Compute semantic delta categories:
   - CONTENT
   - SPECIFICATION
   - EVIDENCE
   - GOVERNANCE
   - IMPLEMENTATION
   - INTEGRATION
   - STATUS
9. Map every declared authority claim to its actual authority evidence.
10. Produce the file-level genealogy cards under `14_FORENSICS/`.
11. Produce the branch-level genealogy after the PR layer is stable.
12. Only then construct the master branch/specification authority map.

---

## 8. No premature status assignment

At this stage the following statuses are deliberately **not assigned globally**:

- CANONICAL
- FINAL
- SUPERSEDED
- NORMATIVE
- APPROVED
- REJECTED

They may appear as **declared states inside source artifacts**, but the forensic registry does not adopt them until authority evidence is established.

---

## 9. Reconstruction principle

The target is not a narrative history of AURA.

The target is a machine-checkable genealogy answering:

> **Co AURA napisała, kiedy to napisała, gdzie to zapisała, z którego commita to pochodziło, jak zmieniało semantykę protokołu, jakie dowody to wspierały, jaka była podstawa authority i co z tym artefaktem stało się później.**

That is the control-plane record required before any canonization decision.
