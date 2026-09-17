# AURA BRANCH GENEALOGY v1.0

**Artifact:** `14_FORENSICS/04_BRANCH_GENEALOGY_v1.0.md`  
**Repository under analysis:** `Aura-IDToken/aura-specification`  
**Forensic workspace:** `vaidt/Crystal-panel-Aura-Protection`  
**Status:** FORENSIC BASELINE / CONTROLLED ANALYSIS  
**Authority:** NONE  
**Normative effect:** NONE  
**Purpose:** reconstruct the surviving branch topology without redesigning, normalizing, or silently resolving AURA governance.

---

## 1. FORENSIC DIRECTIVE

This artifact records the branch state observed in `Aura-IDToken/aura-specification` and treats branches as historical evidence, not as competing authorities.

The governing reconstruction rule is:

```text
branch
  -> HEAD SHA
  -> tree / snapshot
  -> commit ancestry
  -> branch-local artifacts
  -> semantic delta
  -> evidence delta
  -> governance delta
  -> PR / merge / revert relation
  -> authority evidence
  -> status
```

No branch is classified as `CANONICAL`, `FINAL`, `NORMATIVE`, `SUPERSEDED`, or `AUTHORITATIVE` solely because of its name, recency, content, or implementation quality.

The following states remain distinct:

- **EXISTS** — the branch/ref is present in the observed Git repository.
- **REACHABLE** — its referenced commit/tree is reachable through an analyzed ref.
- **CURRENT** — its state is the current state of the subject under the selected baseline.
- **AUTHORITATIVE** — an identifiable governance act grants authority.
- **NORMATIVE** — the artifact has protocol-level normative force.
- **SUPERSEDED** — evidence establishes replacement by a later authoritative act.
- **REVERTED** — a later Git action explicitly reverses the change.

Therefore:

```text
exists in Git != current != approved != normative
```

---

## 2. REPOSITORY BASELINE

### 2.1 Observed repository

`Aura-IDToken/aura-specification`

### 2.2 Observed branch count

**62 surviving branches/refs** were enumerated in the GitHub repository branch endpoint at the time of reconstruction.

### 2.3 Main baseline

| Field | Value |
|---|---|
| Branch | `main` |
| HEAD | `71133de047c71e0bc1156d58c20396fe593ace70` |
| Tree | `bb64ae436c9bc9fab8a8e2dd597aeadf27e39e91` |
| Commit date | `2026-09-10T22:09:45Z` |
| Message | `Revert "docs(dq-003): specification reconciliation control record (#34)" (#43)` |
| Meaning | Current main is a revert state, not simply the accumulation of all preceding work. |

The reverted predecessor was:

| Field | Value |
|---|---|
| Commit | `74220d27f6af01f335fb1423886a51eb063f90f7` |
| Date | `2026-09-10T22:09:10Z` |
| Parent | `091bacb5f8576ac928a6691c8d5067d0b4dd6965` |
| Meaning | DQ-003 reconciliation/control record existed on main briefly before PR #43 reverted it. |

PR #43 merged the revert at `71133de...` and explicitly states that it reverts Aura-IDToken/aura-specification#34. This is a concrete Git-level `REVERTED` relation; it is not, by itself, a statement that every underlying DQ-003 observation is false or historically nonexistent.

---

## 3. HEAD DEDUPLICATION

Branch names are not unique snapshots. The following exact HEAD aliases were observed:

### 3.1 HEAD `628359db85f844be82ecc40790a29092a8c5fb53`

- `BC-02-IMMUTABLE-FIXTURE-HANDOFF`
- `BC-02_BOUNDARY_VALIDATION_RECORD.md`

**Forensic consequence:** analyze the commit/tree once; retain both branch aliases as independent refs.

### 3.2 HEAD `93f677fe34bf3f3fe0e8abffd6c8fdfd92b7958f`

- `copilot/add-branch-protection-rules`
- `copilot/add-github-governance-steps`

### 3.3 HEAD `b08433bd245923a4746802cc7db2b5ef394d2ac3`

- `copilot/aura-specification`
- `copilot/aura-specification-setup`

### 3.4 HEAD `7c1cc66c137fac6a07bbe916eb13e05ce2f23e2b`

- `copilot/aura-specification-overhaul`
- `copilot/aura-specification-structure`

### 3.5 HEAD `62d2d6bcc1a46dd505ebfe400ad01fa3c6a25bf0`

- `copilot/evidence-reconciliation-pass-spec-002`
- `copilot/spec-002-review-issues`

All other observed branch heads are unique within this inventory.

**Rule:** identical HEAD SHA means identical commit snapshot at the ref tip. It does not mean the branches have identical genealogy, creation time, or intended purpose.

---

## 4. COMPLETE SURVIVING BRANCH REGISTER

The following is the complete 62-ref inventory. Where full ancestry/semantic reconstruction has not yet been independently expanded, the status is deliberately marked `RECONSTRUCTION PENDING` rather than inferred from the branch name.

| # | Branch | HEAD SHA | Primary forensic family | Status |
|---:|---|---|---|---|
| 01 | `BC-02-IMMUTABLE-FIXTURE-HANDOFF` | `628359db85f844be82ecc40790a29092a8c5fb53` | BC-02 | observed / dedup |
| 02 | `BC-02_BOUNDARY_VALIDATION_RECORD.md` | `628359db85f844be82ecc40790a29092a8c5fb53` | BC-02 | observed / dedup |
| 03 | `ck003/closure-workspace` | `bfd2fbe82fa6ee728c6a0c6d5a7bf02b038548be` | CK003 | observed |
| 04 | `ck003/cross-language-002` | `ac6a7c86ac282d2a806da6bfde3e67a30dc4c035` | CK003 / DQ-002 | observed |
| 05 | `ck003/dq-002-hash-domain` | `f12a667b252a66f8b2243d1187b927d46ed26468` | DQ-002 | observed |
| 06 | `ck003/dq-003-versioning-snapshot` | `d858a902a934d50d82788f9551fa34fc5c6b6842` | DQ-003 | observed |
| 07 | `ck003/dq-006-closure` | `632d307169540fe0bb13d75c10a1ff55e4885349` | DQ-006 | observed |
| 08 | `ck003/dq-006-closure-inv-009` | `d61c44293bcf80ddf4bca4d8050d2564db6abd5b` | DQ-006 / INV-009 | observed |
| 09 | `ck003/dq-006-closure-package` | `b6bc7992fd15cf18f2e44e0f17b35ad97ed50e10` | DQ-006 | observed |
| 10 | `ck003/dq-006-closure-reconciliation` | `184670cc316b9208c4fe163a840fa5ac36069a72` | DQ-006 | observed |
| 11 | `ck003/dq-006-final-closure-execution` | `ad7548cc6ff830ac8af68a1ec09bffd201f27e58` | DQ-006 | observed |
| 12 | `ck003/specification-integration-dq006` | `7826db9e3e28d356693ba24618f320c44e3120b1` | DQ-006 integration | observed |
| 13 | `claude/aps-200-spec-recovery-b7wc2h` | `84e4962d418058488d08bcd5d3c3a5577c4b6f8f` | APS-200 recovery | observed |
| 14 | `claude/aura-cross-language-002-6t2kdo` | `68054e35487fa7169ae71345e683d72ad5a348b5` | cross-language | observed |
| 15 | `claude/aura-docs-normalization-audit-xkvflu` | `d2d26903d01865899a2424b0230fc3f6c72a5eb8` | documentation audit | observed |
| 16 | `claude/aura-protocol-handover-80wawo` | `bfa61f1f1c44a10d3102c7a7eb85602ba42206d9` | handover | observed |
| 17 | `claude/aura-q1-scope-bridge-c8qm8v` | `eb263ce3f325fd14213c49fff1ab2da3453c426f` | Q1 scope | observed |
| 18 | `claude/bc-02-1-consistency-analysis-8ewd0q` | `dd11311bff7c19ace8cddc002402ce2e04a3c3c4` | BC-02.1 | observed |
| 19 | `claude/bc-02-1-pre-01-schema-kvvm8z` | `a10ca5c567a0a5497ef30d270cf531b346a90d9b` | BC-02.1 / schema | observed |
| 20 | `claude/bc-02-boundary-validation-q0h7yg` | `b90112b83a7a7771028a7dfadee527b4895ba8a3` | BC-02 | observed |
| 21 | `claude/bc-02-immutable-fixture-handoff-3s3fkp` | `e2066bdd05664cc63656ce5623319bccf817acb4` | BC-02 | observed |
| 22 | `claude/ck003-canonical-serialization-hjlaba` | `3be90c21ae43d6e816e2486cd2a76ef290713118` | CK003 / canonical serialization | observed |
| 23 | `claude/dq-002-final-closure-i5s60o` | `b816edf6f69d3bbc73d225a110e790e8fdc720f7` | DQ-002 | observed |
| 24 | `claude/dq-003-conformance-audit-4ok63x` | `ecdb52fc4ff4689e7fe674829acd24e4ce630079` | DQ-003 | observed |
| 25 | `claude/dq-006-closure-98ky0s` | `8f1a2e0cfa9a4410a21de7dcf310c8728465063e` | DQ-006 | observed |
| 26 | `claude/dq-006-closure-i8u8u6` | `018d2987562b751b6301c3af675072cf11e18aaa` | DQ-006 | observed |
| 27 | `claude/dq-006-closure-reconciliation-j3httg` | `f02b087e9ce857603d1d45b7386e46323ca8e32d` | DQ-006 | observed |
| 28 | `claude/gov-001-dq-006-closure-bufnzf` | `436732485be54b3f5d610644010c3e46fa914e5d` | GOV-001 / DQ-006 | observed |
| 29 | `claude/q1-chief-architect-approval-fempmk` | `6002c4910c1eefd056aff77229707904cffb3d30` | Q1 authority | observed |
| 30 | `claude/ri-rs-p01-handoff-ga84l6` | `31c238bd5a4b14ca5989338d84623cb6451e39c3` | RI-RS | observed |
| 31 | `completion/aura-specification-conformance` | `466fbec7042fcdadfb0ea26bd28b89a973eca3dc` | conformance completion | observed |
| 32 | `copilot/add-branch-protection-rules` | `93f677fe34bf3f3fe0e8abffd6c8fdfd92b7958f` | governance / GitHub | observed / dedup |
| 33 | `copilot/add-github-governance-steps` | `93f677fe34bf3f3fe0e8abffd6c8fdfd92b7958f` | governance / GitHub | observed / dedup |
| 34 | `copilot/aura-specification` | `b08433bd245923a4746802cc7db2b5ef394d2ac3` | initial specification | observed / dedup |
| 35 | `copilot/aura-specification-again` | `e639d9c699204bad06f0cb5a135b380c1f837b9c` | specification | observed |
| 36 | `copilot/aura-specification-overhaul` | `7c1cc66c137fac6a07bbe916eb13e05ce2f23e2b` | specification overhaul | observed / dedup |
| 37 | `copilot/aura-specification-setup` | `b08433bd245923a4746802cc7db2b5ef394d2ac3` | setup | observed / dedup |
| 38 | `copilot/aura-specification-structure` | `7c1cc66c137fac6a07bbe916eb13e05ce2f23e2b` | structure | observed / dedup |
| 39 | `copilot/create-aura-protocol-organization` | `30da63225158039da523e237e10984d659f4b516` | organization setup | observed |
| 40 | `copilot/create-github-organization` | `6ad45f3cc998a910bf2f783ff5910364dc5c4076` | organization setup | observed |
| 41 | `copilot/evidence-reconciliation-pass-spec-002` | `62d2d6bcc1a46dd505ebfe400ad01fa3c6a25bf0` | SPEC-002 | observed / dedup |
| 42 | `copilot/gap-001-implementation-gap-report` | `657b508e0816e9c45b2c735704b2654b342a1d6e` | GAP-001 | observed |
| 43 | `copilot/implement-aura-protocol` | `7a22522350a0e917fa773d724854796778623147` | implementation | observed |
| 44 | `copilot/implement-aura-protocol-specifications` | `176f7abb3659ff34855d5693d89317b5dfe14290` | specification implementation | observed |
| 45 | `copilot/spec-002-draft-constitution-artifact-contract` | `0dfcc8b444c53f50465798ac0af73c3c661ef754` | SPEC-002 | observed |
| 46 | `copilot/spec-002-review-issues` | `62d2d6bcc1a46dd505ebfe400ad01fa3c6a25bf0` | SPEC-002 | observed / dedup |
| 47 | `copilot/spec-002-v03-draft` | `15c2e425e6ded49e61e3a359e792b45fce1ae8da` | SPEC-002 | observed |
| 48 | `copilot/sprawdz-i-popraw-dokumentacje` | `5f91167d0611dc91a25ebd6e1ddc3d4ce41175ca` | documentation | observed |
| 49 | `copilot/tighten-spec-002` | `81c04781ff94707ab71a6d3e82f355d088280c45` | SPEC-002 | observed |
| 50 | `copilot/understand-codebase-structure` | `07afb8a38de8a649d76e18a41486a6c077a91a50` | reconnaissance | observed |
| 51 | `custodian/conf-003-rebind-4-5` | `14d455b0ee615e0ddd189fe07efe8995f870a513` | custodian / CONF-003 | observed |
| 52 | `docs/adr-001-document-model` | `c25e990ca94e59ff2db073502b70f47899a2e543` | ADR | observed |
| 53 | `dq/dq-003-audit-record-hash-domain` | `8de397b26250c8c0a767f86302baf8c99d31ff04` | DQ-003 | observed |
| 54 | `dq-003/custodian-jcs-decision` | `e0011cab2b8a19807781033984c6415f94b0ca21` | DQ-003 / JCS | observed |
| 55 | `dq-003/specification-reconciliation` | `0e89408beac178da79ef4ed0bc770de345ff4ae5` | DQ-003 | observed |
| 56 | `main` | `71133de047c71e0bc1156d58c20396fe593ace70` | current baseline | CURRENT BASELINE |
| 57 | `p0/p0-1-canonical-representation-contract` | `4154cc0d89b5cb3490d1d60b2efe43687c9e1ff5` | P0 / canonical representation | observed |
| 58 | `p0/p0-2-evidence-hash-domain-contract` | `cb0494524da740399416020151db305c48aa316b` | P0 / evidence hash | observed |
| 59 | `revert-6-copilot/understand-codebase-structure` | `aa7e141a4eaf3c0fd380daab8580d17fa245b8d6` | revert | observed / revert family |
| 60 | `revert-34-dq-003/specification-reconciliation` | `2b1ab54eac2185ab86e79cc7c794d55cb0c41dd7` | revert PR #43 | REVERT REF |
| 61 | `spec/sync-arc-spec-001` | `102423256e33ad3dea54461f692819aeebaa0700` | ARC/SPEC sync | observed |
| 62 | `specification-recovery/reconciliation-aps200` | `327dacdab83ad33fd5ffafe4300b793a58bb211e` | APS-200 recovery | observed |

---

## 5. BRANCH FAMILIES AND WHAT THEY REPRESENT

The family labels below are **descriptive classifications**, not authority claims.

### 5.1 Early specification / Copilot family

Branches beginning `copilot/aura-specification*`, `copilot/implement-aura-protocol*`, `copilot/create-*`, and `copilot/understand-*` belong to the earlier specification/bootstrap/repository-construction period.

They must be analyzed as historical authored work. Their names do not establish that their proposed specification or architecture was later ratified.

### 5.2 SPEC-002 family

The `copilot/spec-002-*`, `copilot/tighten-spec-002`, and `copilot/evidence-reconciliation-pass-spec-002` refs form a draft/review/reconciliation lineage around the Constitution Artifact/Vector contract.

Known semantic constraint from the reconstructed corpus:

- SPEC-002 remained **DRAFT**.
- Its normative effect was explicitly **NONE until APPROVED**.
- Candidate values such as `32`, `100000`, `int32`, little-endian, and round-half-to-even were not to be silently converted into normative values.

Therefore branch-local SPEC-002 content must not be promoted to protocol authority without a separate authority act.

### 5.3 P0 / CK003 / DQ-002 family

Branches in the `p0/*`, `ck003/*`, and associated Claude branches represent increasingly precise work on canonical representation, evidence hash domain, cross-language verification, fixtures, and closure.

Known reconstructed deltas include:

- canonical byte-domain clarification;
- RFC 8785 JCS binding work;
- separation of evidence-hash and Merkle-leaf domains;
- raw-byte leaf handling;
- recursive Merkle split semantics;
- fixture correction and independently recomputed digest;
- cross-language machine manifest work;
- conformance/closure evidence.

These are semantic and evidentiary changes. They are **not automatically authority acts**.

### 5.4 DQ-003 family

The `dq-003/*`, `dq/dq-003-*`, `claude/dq-003-*`, `ck003/dq-003-*`, and revert branch form a distinct genealogy around audit-record hash domain and specification reconciliation.

A critical Git event is established:

```text
PR #34 change
   ↓
74220d27...
   ↓
merged briefly into main
   ↓
PR #43 explicit revert
   ↓
71133de...
```

The DQ-003 audit content therefore has at least two independent forensic properties:

1. it **EXISTED** in Git history;
2. the specific merged state was later **REVERTED** from `main`.

Reversion of the Git state must not be misread as deletion of historical evidence.

### 5.5 DQ-006 / canonical serialization family

The DQ-006 family contains multiple closure, reconciliation, package, and final-execution branches. Their names and content indicate an extended governance/conformance process around canonical serialization.

The PR #26 semantic delta reconstructed earlier is material:

- APS-200 §8 was changed to bind RFC 8785 JCS canonical serialization;
- canonical UTF-8 bytes became the stated digest input;
- prohibited digest inputs were enumerated;
- SHA-256 and RFC 6962 byte-domain rules were tightened;
- APS-300 evidence hashing was bound to APS-200 §8;
- evidence hash and Merkle leaf domains were explicitly separated;
- CONF-003 was strengthened with independent RI-PY/RI-RS evidence and negative controls;
- DQ-006 closure was reopened/withheld pending discriminating evidence and ratification conditions.

These statements describe the semantic content of the reconstructed change. They do not independently establish that the governance authority required to make every statement normative was present.

### 5.6 BC-02 family

BC-02 branches concern fixture boundary validation, consistency analysis, schema/pre-01 work, immutable fixture handoff, and boundary validation records.

They should be treated as a separate evidence/conformance lineage until cross-reference analysis establishes their exact parent/child relationships.

### 5.7 Governance / Custodian / Q1 family

Branches such as:

- `claude/gov-001-dq-006-closure-bufnzf`
- `claude/q1-chief-architect-approval-fempmk`
- `custodian/conf-003-rebind-4-5`
- `dq-003/custodian-jcs-decision`

are potentially important for authority reconstruction because their stated purpose concerns decisions or custodial acts.

**Important:** a branch containing a document named “decision”, “approval”, or “closure” is not itself proof that the act was ratified. The actual artifact, signer/actor, authority basis, date, scope, and subsequent treatment must be reconstructed.

### 5.8 Documentation audit / handover family

`claude/aura-docs-normalization-audit-xkvflu` is explicitly associated with documentation normalization/control review.

The reconstructed control-review semantics are important:

- read-only analysis;
- separation of EXISTS / REACHABLE / AUTHORITATIVE / CURRENT / NORMATIVE;
- no decision, resolution, or supersession by the audit itself;
- reachability changes were distinguishable from content changes.

This family is evidence about the repository state and governance process, not an automatic source of protocol authority.

### 5.9 Revert family

Two explicit revert-oriented refs exist in the surviving branch inventory:

- `revert-6-copilot/understand-codebase-structure`
- `revert-34-dq-003/specification-reconciliation`

A revert branch is a Git event and must be retained in the genealogy even when the resulting state is not current.

---

## 6. KNOWN HIGH-VALUE COMMIT NODES

### 6.1 PR #1 — repository/specification genesis

- PR: `#1`
- Title: `[WIP] Add complete documentation for APS and Constitution`
- Created: `2026-07-23T18:17:09Z`
- Merged: `2026-07-23T19:14:08Z`
- Head branch: `copilot/aura-specification`
- Head SHA: `129e66cfeeb124dc7776658a464212f6137b4e88`
- Merge commit: `10ee452d0f2ffded08bc952f97457f994113b47e`
- Base main at time: `d2b12cdebe47216431e5960bec5cfd7b3781d396`

This establishes an early merge point for the specification corpus. It does not, by itself, establish that all documents introduced there remained authoritative later.

### 6.2 PR #26 — canonical serialization semantic delta

PR #26 is a high-value semantic node because its patch explicitly altered APS-200, APS-300, APS-001, CONF-003, ADR-CK003-DQ006, DQ-006 closure status, and invariant mapping.

Its forensic treatment must separate:

```text
document claim
vs
Git merge fact
vs
authority/ratification evidence
vs
execution evidence
```

### 6.3 PR #37 — documentation normalization control review

The documentation normalization control review was read-only and explicitly distinguished reachability from authority. The branch/PR genealogy therefore records an evidence/control event rather than a protocol amendment.

### 6.4 PR #43 — DQ-003 revert

- PR: `#43`
- Title: `Revert "docs(dq-003): specification reconciliation control record"`
- Created: `2026-09-10T22:09:34Z`
- Merged: `2026-09-10T22:09:45Z`
- Head branch: `revert-34-dq-003/specification-reconciliation`
- Head SHA: `2b1ab54eac2185ab86e79cc7c794d55cb0c41dd7`
- Merge commit: `71133de047c71e0bc1156d58c20396fe593ace70`
- Base SHA: `74220d27f6af01f335fb1423886a51eb063f90f7`

This is the strongest currently reconstructed example of an explicit superseding Git action: the prior merged state was reverted.

---

## 7. BRANCH-LOCAL SEMANTIC DELTA REGISTER — PHASE 1

Only deltas already reconstructed from evidence are listed as factual observations. No branch name is treated as sufficient evidence for a semantic claim.

| Family / node | Reconstructed semantic delta | Evidence class | Authority conclusion |
|---|---|---|---|
| `copilot/aura-specification*` | initial APS/Constitution documentation and repository structure | specification artifact / merge history | not independently sufficient |
| `copilot/spec-002-*` | draft Constitution Artifact/Vector contract; unresolved source/hash/provenance boundaries | specification draft | explicitly non-normative until approval |
| `p0/p0-1-*` | canonical representation contract work | specification/conformance | authority requires separate validation |
| `p0/p0-2-*` | evidence hash-domain contract work | specification/conformance | authority requires separate validation |
| `ck003/dq-002-hash-domain` | fixture length/digest corrected and independently recomputed | evidence delta | evidence, not automatic ratification |
| `ck003/cross-language-002` | machine manifest, raw-byte leaf contract, recursive split, cross-language preflight | conformance evidence | evidence, not automatic ratification |
| `claude/ck003-canonical-serialization-*` | audit of canonical serialization and oracle execution | audit evidence | audit-only; no production semantics by itself |
| `dq/dq-003-audit-record-hash-domain` | RI-PY/Rust entry-point baseline classification | audit evidence | no implementation remediation authorized |
| `dq-003/custodian-jcs-decision` | stated custodial JCS decision lineage | governance candidate evidence | ratification chain must be verified |
| `dq-003/specification-reconciliation` | specification reconciliation record | governance/specification evidence | later merged state was reverted from main |
| `claude/aura-docs-normalization-audit-*` | control review separating existence/reachability/authority/currentness/normativity | governance audit | explicitly not a resolution |
| DQ-006 closure family | repeated closure/reconciliation work around canonical serialization | governance + conformance evidence | closure authority must be independently established |
| `revert-34-*` / PR #43 | explicit reversal of PR #34 state | Git governance event | prior merged state is REVERTED on main |

---

## 8. BRANCH GENEALOGY RULES FOR CONTINUATION

### Rule B-001 — HEAD identity

A branch is first represented by its exact HEAD SHA. Human-readable branch names are aliases around Git objects.

### Rule B-002 — Tree identity

If two different commits have the same tree SHA, the file snapshot is identical at that point even if their ancestry or messages differ. The commit genealogy remains distinct.

### Rule B-003 — Ancestry before interpretation

Before classifying a branch as a fork, continuation, merge, or independent line, inspect its parent commit(s). Branch names alone are insufficient.

### Rule B-004 — File genealogy linkage

A branch entry must link to `03_FILE_GENEALOGY_v1.0.md` at the artifact level. The same file may have different blob SHAs and meanings across branch lines.

### Rule B-005 — PR is not authority

A merged pull request proves a Git integration event. It does not automatically prove that the semantic content was formally ratified as protocol authority.

### Rule B-006 — Revert is not erasure

A revert changes the current reachable state. It does not erase the historical commit, branch, or artifact from Git history.

### Rule B-007 — Audit is not decision

A control review or forensic audit must not be interpreted as a governance decision unless the artifact itself explicitly constitutes such an authorized act and the authority chain is established.

### Rule B-008 — Branch name is not status

Words such as `final`, `closure`, `approval`, `recovery`, `canonical`, `implementation`, or `complete` are descriptive branch labels until independently supported.

### Rule B-009 — No silent reconciliation

If two branches contain incompatible semantics, retain both branches as evidence until an authority-bearing act resolves the conflict.

### Rule B-010 — Current main is its own forensic state

`main@71133de...` must be analyzed independently from the newest branch by date or from a branch whose name appears more authoritative.

---

## 9. CURRENT FORENSIC FINDINGS

### F-001 — The repository contains a substantial multi-line development history

The 62 surviving refs are not one linear specification history. They form multiple work families around specification bootstrap, canonical serialization, evidence hashing, cross-language conformance, fixture validation, DQ closure, governance review, and reversions.

### F-002 — Branch multiplicity materially affects authority reconstruction

Several branches carry overlapping names or subject matter but different HEADs. Some branch names are aliases of identical HEADs. Therefore a simple “latest branch” model is insufficient.

### F-003 — The DQ-006/JCS lineage is not reducible to a single branch

The canonical serialization question was processed through multiple branches, commits, audits, and closure packages. The semantic history must therefore be reconstructed from the commit graph and artifact deltas rather than from the surviving branch with the most authoritative-sounding name.

### F-004 — Main is explicitly a revert state

The current main HEAD is PR #43's revert merge. Therefore any reconstruction that reads only current main loses historical information about the briefly merged DQ-003 reconciliation state.

### F-005 — Historical evidence survives Git reversion

The existence of the reverted DQ-003 commit and branch is a factual part of repository history. Its later reversion is a separate factual event.

### F-006 — Authority remains a separate reconstruction axis

The current branch inventory alone does not prove which semantic changes were formally authorized. Authority evidence must be reconstructed from the relevant decision, custodian, approval, governance, and merge records.

### F-007 — Branch genealogy is not yet complete at parent/ancestor depth

This v1.0 artifact establishes the complete surviving branch inventory, exact HEADs, known duplicate snapshots, high-value genealogy nodes, and the semantic families already reconstructed. Full per-branch ancestry, first divergence, merge-base, branch-local file set, and branch-local semantic delta remain a continuation task where not independently reconstructed here.

This limitation is intentional. No missing ancestry is invented.

---

## 10. OPEN FORENSIC QUESTIONS

1. What is the exact parent chain of each unique branch HEAD?
2. What is the merge-base of each branch family against `main`?
3. Which branches were created from which PR heads?
4. Which branch-local files first appeared on each line?
5. Which files changed semantically versus only being copied/renamed?
6. Which branches contain the same tree under different commit histories?
7. Which branches contain artifacts that were later merged, reverted, or superseded?
8. Which branch-local documents constitute actual authority acts rather than analysis or proposals?
9. Which governance acts are themselves reachable from current `main`?
10. Which semantic conflicts remain unresolved after PR #43?

---

## 11. NEXT FORENSIC PASS

The next pass should not redesign or normalize the specification. It should mechanically deepen this genealogy:

```text
04_BRANCH_GENEALOGY_v1.0
        ↓
per unique HEAD
        ↓
commit metadata
        ↓
parent(s)
        ↓
merge-base vs main
        ↓
first divergence
        ↓
branch-local tree
        ↓
file first appearance / last modification
        ↓
semantic delta
        ↓
PR relation
        ↓
revert / supersession relation
        ↓
authority evidence
```

Only after that pass should the branch map be used to build the cross-referenced Master Branch Map.

---

## 12. CONTROLLED CONCLUSION

At this stage the repository can be described accurately as follows:

> `Aura-IDToken/aura-specification` contains a 62-ref surviving branch topology with multiple independent work families and several exact HEAD aliases. The current `main` state is a post-revert state. Canonical serialization, evidence hashing, DQ closure, cross-language conformance, fixture validation, and governance review were developed through multiple branch lines rather than one linear authority chain. Git existence and merge history establish historical occurrence; they do not by themselves establish present authority or normative force.

This document therefore records **genealogy**, not a reconstructed “final AURA”.

---

## 13. SOURCE / EVIDENCE INDEX

Primary Git evidence reconstructed for this artifact:

- GitHub branch enumeration for `Aura-IDToken/aura-specification` — 62 surviving refs.
- `main@71133de047c71e0bc1156d58c20396fe593ace70`.
- PR #1 and merge commit `10ee452d0f2ffded08bc952f97457f994113b47e`.
- PR #26 semantic patch reconstruction.
- PR #37 documentation normalization control review lineage.
- PR #43 and revert commit `71133de...`.
- Reverted DQ-003 predecessor `74220d27f6af01f335fb1423886a51eb063f90f7`.
- Existing `03_FILE_GENEALOGY_v1.0.md` forensic baseline.

**Evidence discipline:** this document does not claim that unexamined branch names constitute semantic evidence. Where metadata is not yet reconstructed to commit/parent/file depth, the artifact explicitly leaves the question open.

---

**END — AURA BRANCH GENEALOGY v1.0**
