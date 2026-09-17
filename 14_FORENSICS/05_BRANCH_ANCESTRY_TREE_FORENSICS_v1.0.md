# AURA — BRANCH ANCESTRY / TREE FORENSICS v1.0

**Artifact:** `14_FORENSICS/05_BRANCH_ANCESTRY_TREE_FORENSICS_v1.0.md`  
**Source repository:** `Aura-IDToken/aura-specification`  
**Forensic repository:** `vaidt/Crystal-panel-Aura-Protection`  
**Status:** FORENSIC BASELINE / CONTROLLED ANALYSIS  
**Authority:** NONE  
**Normative effect:** NONE  
**Purpose:** reconstruct the ancestry and tree position of every unique surviving branch HEAD without redesigning AURA or inferring authority from branch names.

---

## 1. FORENSIC RULE

This document treats each unique HEAD SHA as a Git snapshot and preserves branch aliases separately.

```text
ref alias(es)
  -> unique HEAD
  -> parent(s)
  -> tree_sha
  -> merge-base(main)
  -> first divergence
  -> branch-local delta
  -> PR / merge / revert relation
  -> authority evidence
  -> status
```

The following are deliberately distinct:

- `EXISTS` — ref/snapshot exists in Git history.
- `REACHABLE` — snapshot is reachable from the selected `main` baseline.
- `CURRENT` — operative record for the relevant subject.
- `AUTHORITATIVE` — established by an identifiable authority act.
- `NORMATIVE` — protocol-level force.
- `SUPERSEDED` — replacement established by evidence.
- `REVERTED` — explicit Git reversal established by evidence.

`EXISTS != REACHABLE != CURRENT != AUTHORITATIVE != NORMATIVE`.

No classification below is inferred from branch naming.

---

## 2. BASELINES

### Current main

| Field | Value |
|---|---|
| Ref | `main` |
| HEAD | `71133de047c71e0bc1156d58c20396fe593ace70` |
| tree | `bb64ae436c9bc9fab8a8e2dd597aeadf27e39e91` |
| parent | `74220d27f6af01f335fb1423886a51eb063f90f7` |
| date | `2026-09-10T22:09:45Z` |
| message | `Revert "docs(dq-003): specification reconciliation control record (#34)" (#43)` |

The current main commit explicitly reverts `74220d27f6af01f335fb1423886a51eb063f90f7`. This is a verified Git-level revert relation. fileciteturn196file0L2-L2

### Deduplication

The 62 surviving refs collapse to **57 unique HEAD SHAs** because five HEADs have two aliases each. The aliases are retained below and are not treated as separate snapshots.

Known alias groups:

1. `628359db...` → `BC-02-IMMUTABLE-FIXTURE-HANDOFF`, `BC-02_BOUNDARY_VALIDATION_RECORD.md`
2. `93f677fe...` → `copilot/add-branch-protection-rules`, `copilot/add-github-governance-steps`
3. `b08433bd...` → `copilot/aura-specification`, `copilot/aura-specification-setup`
4. `7c1cc66c...` → `copilot/aura-specification-overhaul`, `copilot/aura-specification-structure`
5. `62d2d6bc...` → `copilot/evidence-reconciliation-pass-spec-002`, `copilot/spec-002-review-issues`

---

## 3. UNIQUE HEAD REGISTER — 57 RECORDS

**Notation:** `UNRESOLVED` means the field has not been independently expanded in this controlled pass. It is not a negative finding and must not be replaced by inference.

| # | Ref alias(es) | Unique HEAD | Parent(s) | tree_sha | merge-base(main) | First divergence | Branch-local files / count | PR / merge / revert | Status |
|---:|---|---|---|---|---|---|---|---|---|
| 01 | `BC-02-IMMUTABLE-FIXTURE-HANDOFF`; `BC-02_BOUNDARY_VALIDATION_RECORD.md` | `628359db85f844be82ecc40790a29092a8c5fb53` | `1b249e421de374ef23bf2bcad38fd901aed3415e` | `75a8d9dab581df1e60149de03e5482923ec7d3ac` | `628359db85f844be82ecc40790a29092a8c5fb53` | none relative to merge-base | 0 relative to merge-base; historically adds control-review artifact | PR #38; merged into main before current baseline; no revert of this commit established | ancestor of main / reachability verified |
| 02 | `ck003/closure-workspace` | `bfd2fbe82fa6ee728c6a0c6d5a7bf02b038548be` | `565ac2b7b55d4d643a7a8a154c85a79e3064f032`; `6cacb1175684ca34c8b2a496dadc585e9cc0c936` | `778200c40ec67c840c5b076f4ab7cd66b0a7cab3` | UNRESOLVED | UNRESOLVED | UNRESOLVED | merge commit: `Merge branch 'main' into ck003/closure-workspace`; PR relation UNRESOLVED | observed |
| 03 | `ck003/cross-language-002` | `ac6a7c86ac282d2a806da6bfde3e67a30dc4c035` | `fc4007acbd85ceb7be4cdecbf259c7751b1d69ea` | `07d516d996d03b5ee36eda8dc580d61ed3bab032` | `62d2d6bcc1a46dd505ebfe400ad01fa3c6a25bf0` | first unique commit after merge-base: `ac6a7c86` | 8 files in compare surface; CK003/DQ-002 manifest, evidence, ADR and fixtures | PR relation UNRESOLVED | verified compare |
| 04 | `ck003/dq-002-hash-domain` | `f12a667b252a66f8b2243d1187b927d46ed26468` | `5e504bad4ee51aab4e9cfd4e944aca5bdd186bbd` | `8fab27de667d44de537d0d67eaf2270f7382a337` | `62d2d6bcc1a46dd505ebfe400ad01fa3c6a25bf0` | `f12a667b...` is branch-local correction line | 6 files in compare surface; DQ-002 hash-domain ADR/evidence/fixture family | PR relation UNRESOLVED | observed; unsigned commit |
| 05 | `ck003/dq-003-versioning-snapshot` | `d858a902a934d50d82788f9551fa34fc5c6b6842` | UNRESOLVED | UNRESOLVED | UNRESOLVED | UNRESOLVED | DQ-003 versioning snapshot family | UNRESOLVED | observed |
| 06 | `ck003/dq-006-closure` | `632d307169540fe0bb13d75c10a1ff55e4885349` | UNRESOLVED | UNRESOLVED | UNRESOLVED | UNRESOLVED | DQ-006 closure family | UNRESOLVED | observed |
| 07 | `ck003/dq-006-closure-inv-009` | `d61c44293bcf80ddf4bca4d8050d2564db6abd5b` | UNRESOLVED | UNRESOLVED | UNRESOLVED | UNRESOLVED | DQ-006 / INV-009 family | UNRESOLVED | observed |
| 08 | `ck003/dq-006-closure-package` | `b6bc7992fd15cf18f2e44e0f17b35ad97ed50e10` | UNRESOLVED | UNRESOLVED | UNRESOLVED | UNRESOLVED | DQ-006 closure package family | UNRESOLVED | observed |
| 09 | `ck003/dq-006-closure-reconciliation` | `184670cc316b9208c4fe163a840fa5ac36069a72` | UNRESOLVED | UNRESOLVED | UNRESOLVED | UNRESOLVED | DQ-006 reconciliation family | UNRESOLVED | observed |
| 10 | `ck003/dq-006-final-closure-execution` | `ad7548cc6ff830ac8af68a1ec09bffd201f27e58` | UNRESOLVED | UNRESOLVED | UNRESOLVED | UNRESOLVED | DQ-006 final-closure execution family | UNRESOLVED | observed |
| 11 | `ck003/specification-integration-dq006` | `7826db9e3e28d356693ba24618f320c44e3120b1` | UNRESOLVED | UNRESOLVED | UNRESOLVED | UNRESOLVED | DQ-006 integration family | UNRESOLVED | observed |
| 12 | `claude/aps-200-spec-recovery-b7wc2h` | `84e4962d418058488d08bcd5d3c3a5577c4b6f8f` | UNRESOLVED | UNRESOLVED | UNRESOLVED | UNRESOLVED | APS-200 recovery family | UNRESOLVED | observed |
| 13 | `claude/aura-cross-language-002-6t2kdo` | `68054e35487fa7169ae71345e683d72ad5a348b5` | UNRESOLVED | UNRESOLVED | UNRESOLVED | UNRESOLVED | cross-language evidence family | UNRESOLVED | observed |
| 14 | `claude/aura-docs-normalization-audit-xkvflu` | `d2d26903d01865899a2424b0230fc3f6c72a5eb8` | UNRESOLVED | UNRESOLVED | UNRESOLVED | UNRESOLVED | documentation normalization audit family | PR #37 relation established in audit evidence; merged audit blob later reached main | observed |
| 15 | `claude/aura-protocol-handover-80wawo` | `bfa61f1f1c44a10d3102c7a7eb85602ba42206d9` | UNRESOLVED | UNRESOLVED | UNRESOLVED | UNRESOLVED | protocol handover family | UNRESOLVED | observed |
| 16 | `claude/aura-q1-scope-bridge-c8qm8v` | `eb263ce3f325fd14213c49fff1ab2da3453c426f` | UNRESOLVED | UNRESOLVED | UNRESOLVED | UNRESOLVED | Q1 scope bridge family | UNRESOLVED | observed |
| 17 | `claude/bc-02-1-consistency-analysis-8ewd0q` | `dd11311bff7c19ace8cddc002402ce2e04a3c3c4` | UNRESOLVED | UNRESOLVED | UNRESOLVED | UNRESOLVED | BC-02.1 consistency-analysis family | UNRESOLVED | observed |
| 18 | `claude/bc-02-1-pre-01-schema-kvvm8z` | `a10ca5c567a0a5497ef30d270cf531b346a90d9b` | UNRESOLVED | UNRESOLVED | UNRESOLVED | UNRESOLVED | BC-02.1 schema/review family | UNRESOLVED | observed |
| 19 | `claude/bc-02-boundary-validation-q0h7yg` | `b90112b83a7a7771028a7dfadee527b4895ba8a3` | UNRESOLVED | UNRESOLVED | UNRESOLVED | UNRESOLVED | BC-02 boundary-validation family | UNRESOLVED | observed |
| 20 | `claude/bc-02-immutable-fixture-handoff-3s3fkp` | `e2066bdd05664cc63656ce5623319bccf817acb4` | UNRESOLVED | UNRESOLVED | UNRESOLVED | UNRESOLVED | BC-02 immutable-fixture handoff family | UNRESOLVED | observed |
| 21 | `claude/ck003-canonical-serialization-hjlaba` | `3be90c21ae43d6e816e2486cd2a76ef290713118` | UNRESOLVED | UNRESOLVED | UNRESOLVED | UNRESOLVED | CK003 canonical-serialization audit family | UNRESOLVED | observed |
| 22 | `claude/dq-002-final-closure-i5s60o` | `b816edf6f69d3bbc73d225a110e790e8fdc720f7` | UNRESOLVED | UNRESOLVED | UNRESOLVED | UNRESOLVED | DQ-002 final-closure revalidation family | UNRESOLVED | observed |
| 23 | `claude/dq-003-conformance-audit-4ok63x` | `ecdb52fc4ff4689e7fe674829acd24e4ce630079` | UNRESOLVED | UNRESOLVED | UNRESOLVED | UNRESOLVED | DQ-003 conformance-audit family | UNRESOLVED | observed |
| 24 | `claude/dq-006-closure-98ky0s` | `8f1a2e0cfa9a4410a21de7dcf310c8728465063e` | UNRESOLVED | UNRESOLVED | UNRESOLVED | UNRESOLVED | DQ-006 closure family | UNRESOLVED | observed |
| 25 | `claude/dq-006-closure-i8u8u6` | `018d2987562b751b6301c3af675072cf11e18aaa` | UNRESOLVED | UNRESOLVED | UNRESOLVED | UNRESOLVED | DQ-006 closure family | UNRESOLVED | observed |
| 26 | `claude/dq-006-closure-reconciliation-j3httg` | `f02b087e9ce857603d1d45b7386e46323ca8e32d` | UNRESOLVED | UNRESOLVED | UNRESOLVED | UNRESOLVED | DQ-006 reconciliation family | UNRESOLVED | observed |
| 27 | `claude/gov-001-dq-006-closure-bufnzf` | `436732485be54b3f5d610644010c3e46fa914e5d` | UNRESOLVED | UNRESOLVED | UNRESOLVED | UNRESOLVED | GOV-001 / DQ-006 family | UNRESOLVED | observed |
| 28 | `claude/q1-chief-architect-approval-fempmk` | `6002c4910c1eefd056aff77229707904cffb3d30` | UNRESOLVED | UNRESOLVED | UNRESOLVED | UNRESOLVED | Q1 authority-evidence family | UNRESOLVED | observed; authority claims require separate evidence analysis |
| 29 | `claude/ri-rs-p01-handoff-ga84l6` | `31c238bd5a4b14ca5989338d84623cb6451e39c3` | UNRESOLVED | UNRESOLVED | UNRESOLVED | UNRESOLVED | RI-RS handoff family | UNRESOLVED | observed |
| 30 | `completion/aura-specification-conformance` | `466fbec7042fcdadfb0ea26bd28b89a973eca3dc` | UNRESOLVED | UNRESOLVED | UNRESOLVED | UNRESOLVED | conformance completion family | UNRESOLVED | observed |
| 31 | `copilot/add-branch-protection-rules`; `copilot/add-github-governance-steps` | `93f677fe34bf3f3fe0e8abffd6c8fdfd92b7958f` | UNRESOLVED | UNRESOLVED | UNRESOLVED | UNRESOLVED | governance/GitHub family | commit is PR #5 merge in known history | observed / alias-dedup |
| 32 | `copilot/aura-specification`; `copilot/aura-specification-setup` | `b08433bd245923a4746802cc7db2b5ef394d2ac3` | UNRESOLVED | UNRESOLVED | UNRESOLVED | UNRESOLVED | initial specification bootstrap family | tag `spec-v0.1.0` points to this SHA per normalization evidence | observed / alias-dedup |
| 33 | `copilot/aura-specification-again` | `e639d9c699204bad06f0cb5a135b380c1f837b9c` | UNRESOLVED | UNRESOLVED | UNRESOLVED | UNRESOLVED | specification iteration family | UNRESOLVED | observed |
| 34 | `copilot/aura-specification-overhaul`; `copilot/aura-specification-structure` | `7c1cc66c137fac6a07bbe916eb13e05ce2f23e2b` | UNRESOLVED | UNRESOLVED | UNRESOLVED | UNRESOLVED | specification overhaul/structure family | UNRESOLVED | observed / alias-dedup |
| 35 | `copilot/create-aura-protocol-organization` | `30da63225158039da523e237e10984d659f4b516` | UNRESOLVED | UNRESOLVED | UNRESOLVED | UNRESOLVED | organization setup family | UNRESOLVED | observed |
| 36 | `copilot/create-github-organization` | `6ad45f3cc998a910bf2f783ff5910364dc5c4076` | UNRESOLVED | UNRESOLVED | UNRESOLVED | UNRESOLVED | organization setup family | UNRESOLVED | observed |
| 37 | `copilot/evidence-reconciliation-pass-spec-002`; `copilot/spec-002-review-issues` | `62d2d6bcc1a46dd505ebfe400ad01fa3c6a25bf0` | UNRESOLVED | UNRESOLVED | UNRESOLVED | UNRESOLVED | SPEC-002 evidence-reconciliation family | acts as merge-base for `ac6a7c86` and `f12a667b` comparisons | observed / alias-dedup |
| 38 | `copilot/gap-001-implementation-gap-report` | `657b508e0816e9c45b2c735704b2654b342a1d6e` | UNRESOLVED | UNRESOLVED | UNRESOLVED | UNRESOLVED | GAP-001 family | UNRESOLVED | observed |
| 39 | `copilot/implement-aura-protocol` | `7a22522350a0e917fa773d724854796778623147` | UNRESOLVED | UNRESOLVED | UNRESOLVED | UNRESOLVED | implementation/migration-documentation family | known commit removes migration note from README | observed |
| 40 | `copilot/implement-aura-protocol-specifications` | `176f7abb3659ff34855d5693d89317b5dfe14290` | UNRESOLVED | UNRESOLVED | UNRESOLVED | UNRESOLVED | RFC template maintenance family | known commit only corrects spelling in RFC template | observed |
| 41 | `copilot/spec-002-draft-constitution-artifact-contract` | `0dfcc8b444c53f50465798ac0af73c3c661ef754` | UNRESOLVED | UNRESOLVED | UNRESOLVED | UNRESOLVED | SPEC-002 draft family | known commit preserves DRAFT-only status | observed |
| 42 | `copilot/spec-002-v03-draft` | `15c2e425e6ded49e61e3a359e792b45fce1ae8da` | UNRESOLVED | UNRESOLVED | UNRESOLVED | UNRESOLVED | SPEC-002 v0.3 family | UNRESOLVED | observed |
| 43 | `copilot/sprawdz-i-popraw-dokumentacje` | `5f91167d0611dc91a25ebd6e1ddc3d4ce41175ca` | UNRESOLVED | UNRESOLVED | UNRESOLVED | UNRESOLVED | documentation review family | UNRESOLVED | observed |
| 44 | `copilot/tighten-spec-002` | `81c04781ff94707ab71a6d3e82f355d088280c45` | UNRESOLVED | UNRESOLVED | UNRESOLVED | UNRESOLVED | SPEC-002 tightening family | UNRESOLVED | observed |
| 45 | `copilot/understand-codebase-structure` | `07afb8a38de8a649d76e18a41486a6c077a91a50` | UNRESOLVED | UNRESOLVED | UNRESOLVED | UNRESOLVED | reconnaissance family | has explicit revert ref `revert-6-...` elsewhere in corpus | observed |
| 46 | `custodian/conf-003-rebind-4-5` | `14d455b0ee615e0ddd189fe07efe8995f870a513` | UNRESOLVED | UNRESOLVED | UNRESOLVED | UNRESOLVED | Custodian / CONF-003 family | UNRESOLVED | observed |
| 47 | `docs/adr-001-document-model` | `c25e990ca94e59ff2db073502b70f47899a2e543` | UNRESOLVED | UNRESOLVED | UNRESOLVED | UNRESOLVED | ADR-001 documentation family | known SHA-update commit; PR relation UNRESOLVED | observed |
| 48 | `dq/dq-003-audit-record-hash-domain` | `8de397b26250c8c0a767f86302baf8c99d31ff04` | UNRESOLVED | UNRESOLVED | UNRESOLVED | UNRESOLVED | DQ-003 entry-point baseline family | UNRESOLVED | observed |
| 49 | `dq-003/custodian-jcs-decision` | `e0011cab2b8a19807781033984c6415f94b0ca21` | UNRESOLVED | UNRESOLVED | UNRESOLVED | UNRESOLVED | DQ-003 Custodian/JCS decision family | authority implications unresolved | observed |
| 50 | `dq-003/specification-reconciliation` | `0e89408beac178da79ef4ed0bc770de345ff4ae5` | UNRESOLVED | UNRESOLVED | UNRESOLVED | UNRESOLVED | DQ-003 specification-reconciliation family | PR #34 lineage exists; exact ancestry expansion pending | observed; later target of revert chain |
| 51 | `main` | `71133de047c71e0bc1156d58c20396fe593ace70` | `74220d27f6af01f335fb1423886a51eb063f90f7` | `bb64ae436c9bc9fab8a8e2dd597aeadf27e39e91` | self | none | 0 | PR #43 explicit revert of DQ-003 reconciliation (#34) | CURRENT baseline |
| 52 | `p0/p0-1-canonical-representation-contract` | `4154cc0d89b5cb3490d1d60b2efe43687c9e1ff5` | UNRESOLVED | UNRESOLVED | UNRESOLVED | UNRESOLVED | P0-1 canonical representation closure | authority claim is documented in artifact; PR relation UNRESOLVED | observed; authority requires separate reconciliation |
| 53 | `p0/p0-2-evidence-hash-domain-contract` | `cb0494524da740399416020151db305c48aa316b` | UNRESOLVED | UNRESOLVED | UNRESOLVED | UNRESOLVED | P0-2 evidence/hash-domain closure | authority claim is documented in artifact; PR relation UNRESOLVED | observed; authority requires separate reconciliation |
| 54 | `revert-6-copilot/understand-codebase-structure` | `aa7e141a4eaf3c0fd380daab8580d17fa245b8d6` | UNRESOLVED | UNRESOLVED | UNRESOLVED | UNRESOLVED | revert family for reconnaissance branch | explicit revert ref name; exact reverted commit relation pending expansion | observed |
| 55 | `revert-34-dq-003/specification-reconciliation` | `2b1ab54eac2185ab86e79cc7c794d55cb0c41dd7` | UNRESOLVED | UNRESOLVED | UNRESOLVED | UNRESOLVED | DQ-003 revert family | PR #43 head; reverts `74220d27...` | verified revert lineage |
| 56 | `spec/sync-arc-spec-001` | `102423256e33ad3dea54461f692819aeebaa0700` | UNRESOLVED | UNRESOLVED | UNRESOLVED | UNRESOLVED | ARC/SPEC synchronization family | UNRESOLVED | observed |
| 57 | `specification-recovery/reconciliation-aps200` | `327dacdab83ad33fd5ffafe4300b793a58bb211e` | UNRESOLVED | UNRESOLVED | UNRESOLVED | UNRESOLVED | APS-200 recovery/reconciliation family | UNRESOLVED | observed |

---

## 4. VERIFIED ANCESTRY / DIVERGENCE CASES

### 4.1 `ck003/cross-language-002`

Verified commit metadata:

```text
HEAD      ac6a7c86ac282d2a806da6bfde3e67a30dc4c035
parent    fc4007acbd85ceb7be4cdecbf259c7751b1d69ea
tree      07d516d996d03b5ee36eda8dc580d61ed3bab032
date      2026-08-18T20:28:54Z
```

Against current `main`, GitHub reports:

```text
merge-base = 62d2d6bcc1a46dd505ebfe400ad01fa3c6a25bf0
ahead_by  = 9
behind_by = 32
```

The branch-local compare surface contains eight files, including the CROSS-LANGUAGE-002 manifest/evidence and the CK003/DQ-002 hash-domain ADR/fixture family. This is a verified semantic branch-local delta, not a filename inference.

### 4.2 `ck003/dq-002-hash-domain`

Verified commit metadata:

```text
HEAD      f12a667b252a66f8b2243d1187b927d46ed26468
parent    5e504bad4ee51aab4e9cfd4e944aca5bdd186bbd
tree      8fab27de667d44de537d0d67eaf2270f7382a337
date      2026-08-17T20:31:21Z
```

Against current `main`:

```text
merge-base = 62d2d6bcc1a46dd505ebfe400ad01fa3c6a25bf0
ahead_by  = 7
behind_by = 32
```

The compare surface contains six DQ-002 hash-domain files. The HEAD commit is unsigned; this is a provenance fact and not an authority judgement. fileciteturn192file0L2-L2

### 4.3 `ck003/closure-workspace`

Verified as a two-parent merge commit:

```text
HEAD      bfd2fbe82fa6ee728c6a0c6d5a7bf02b038548be
tree      778200c40ec67c840c5b076f4ab7cd66b0a7cab3
parent 1  565ac2b7b55d4d643a7a8a154c85a79e3064f032
parent 2  6cacb1175684ca34c8b2a496dadc585e9cc0c936
date      2026-08-19T14:52:47Z
message   Merge branch 'main' into ck003/closure-workspace
```

The two-parent structure is verified directly from the Git commit object. fileciteturn193file0L2-L2

### 4.4 `628359db...`

This snapshot is itself an ancestor/merge-base for the current main comparison used in the forensic pass. Its commit object has:

```text
parent  1b249e421de374ef23bf2bcad38fd901aed3415e
tree    75a8d9dab581df1e60149de03e5482923ec7d3ac
date    2026-08-25T16:50:57Z
```

The commit message states that the review was read-only and that no authority or normative decision was created. fileciteturn191file0L2-L2

---

## 5. PR / MERGE / REVERT REGISTER

### PR #37 — documentation normalization audit

The normalization evidence records PR #37 as:

```text
head  claude/aura-docs-normalization-audit-xkvflu @ d606db4
base  main @ 528de0d
merge 1b249e4...
```

The audit blob was verified identical across the merge; the merge changed reachability, not the artifact bytes. The review explicitly states that merge into `main` does not itself create authority. fileciteturn190file0L7-L7

### PR #38 — documentation normalization control review

The current alias `628359db...` is the commit produced by the control-review merge. The commit object states that the scope covered all 57 refs plus one tag in `aura-specification`. fileciteturn190file0L2-L7

### PR #34 → PR #43 — DQ-003 reconciliation / explicit revert

Known verified chain:

```text
PR #34
  ↓
74220d27f6af01f335fb1423886a51eb063f90f7
  ↓
PR #43
  ↓
2b1ab54eac2185ab86e79cc7c794d55cb0c41dd7
  ↓
71133de047c71e0bc1156d58c20396fe593ace70 (main)
```

The final main commit explicitly states:

```text
This reverts commit 74220d27f6af01f335fb1423886a51eb063f90f7.
```

and its parent is the reverted commit. fileciteturn196file0L2-L2

This establishes **REVERTED at Git level** for the change represented by `74220d27...`. It does not establish that all observations contained in the reverted artifact are historically false.

---

## 6. BRANCH-LOCAL FILE RULE

`branch-local files` in this document means files in the **tree delta from the computed merge-base to the HEAD**, not “files whose path looks branch-specific”.

For each future expansion the required computation is:

```text
MB = merge_base(main, HEAD)
DELTA = tree(HEAD) - tree(MB)
```

Then classify every changed path:

```text
ADDED
MODIFIED
DELETED
RENAMED
UNCHANGED
```

A file existing only on a branch is not automatically normative. A file merged into main is not automatically authoritative. A file absent from main is not automatically superseded.

---

## 7. FIRST-DIVERGENCE RULE

`first divergence` means the earliest commit on the HEAD lineage after the merge-base at which the branch lineage becomes distinct from the main lineage.

It is **not**:

- branch creation timestamp;
- latest commit message;
- first file visible in the branch tree;
- first commit whose filename contains the task name.

For merge commits, first divergence must be computed from the actual ancestry graph, not from first-parent display alone.

---

## 8. AUTHORITY FIREWALL

This artifact is not allowed to transform Git topology into governance authority.

In particular:

```text
branch name             != authority
latest commit           != authority
merged PR               != authority
revert                  != proof of semantic falsity
file in main            != normative
DRAFT + approval text   != automatically authoritative
```

Authority must be established separately through the authority evidence register.

---

## 9. CURRENT FORENSIC FINDINGS

1. The repository contains **62 surviving refs but 57 unique HEAD snapshots**.
2. Several refs are aliases of the same exact commit and therefore must not be counted as independent snapshots.
3. At least one active branch is a true two-parent merge commit (`bfd2fbe...`).
4. At least two CK003 branches independently diverge from `62d2d6bc...`, producing separate DQ-002/cross-language lines.
5. Current `main` is a verified **post-revert** state.
6. The DQ-003 reconciliation change is therefore not reachable from current main in the same state it briefly occupied immediately before PR #43.
7. Branch-local existence and main reachability are separate properties.
8. Authority remains a separate forensic dimension and is not assigned by this document.

---

## 10. UNRESOLVED EXPANSION QUEUE

The following fields remain explicitly open for the next forensic pass:

- exact `parent(s)` for the remaining unique HEADs;
- exact `tree_sha` for the remaining unique HEADs;
- exact merge-base for every unique HEAD against current main;
- exact first-divergence commit for every unique HEAD;
- complete per-HEAD tree delta and exact branch-local file inventory;
- PR number/head/base for every branch where available;
- explicit supersession/revert relation for every candidate pair;
- authority evidence linkage.

These are **data-retrieval gaps**, not conclusions about the repository.

---

## 11. EVIDENCE REFERENCES

- Current branch inventory and 57-HEAD deduplication: `14_FORENSICS/04_BRANCH_GENEALOGY_v1.0.md`.
- Current main commit and explicit revert relation: GitHub commit object for `71133de...`. fileciteturn196file0L2-L2
- `628359db...` parent/tree and controlled-review scope: GitHub commit object. fileciteturn191file0L2-L2
- `bfd2fbe...` two-parent ancestry and tree: GitHub commit object. fileciteturn193file0L2-L2
- `ac6a7c86...` parent/tree and DQ-002/CROSS-LANGUAGE delta: GitHub commit/compare evidence. fileciteturn197file0L2-L2
- `f12a667...` parent/tree and DQ-002 delta: GitHub commit/compare evidence. fileciteturn192file0L2-L2
- Documentation normalization control review and 57-ref search boundary: control-review commit. fileciteturn190file0L2-L7

---

## 12. CONTROLLED CONCLUSION

This document establishes the **57 unique HEAD record surface** and preserves all 62 branch aliases without collapsing their identity.

It does **not** claim that all 57 ancestry graphs, merge-bases and tree deltas have already been independently expanded. Any field still marked `UNRESOLVED` must be resolved from Git object/compare evidence before being promoted into a final Master Branch Map.

The forensic boundary is therefore:

```text
57 unique HEADs = established inventory
62 refs        = established aliases
full ancestry  = partially expanded
full tree delta = partially expanded
authority      = separate unresolved dimension
```

No AURA semantics are redesigned or silently reconciled by this artifact.
