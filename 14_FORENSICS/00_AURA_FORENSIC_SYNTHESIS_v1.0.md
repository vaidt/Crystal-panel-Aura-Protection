# AURA FORENSIC SYNTHESIS v1.0

**Layer:** 14 — FORENSICS  
**Mode:** controlled reconstruction / no redesign  
**Date:** 2026-09-16  
**Primary source repository:** `Aura-IDToken/aura-specification`  
**Target reconstruction repository:** `vaidt/Crystal-panel-Aura-Protection`

---

## 1. PURPOSE

This document records the current synthesis of the AURA project history reconstructed from:

1. Git repository history and branch/PR evidence from `Aura-IDToken/aura-specification`;
2. current specification artifacts and their declared statuses;
3. uploaded historical AURA archives, restore prompts and engineering records;
4. the governance/conformance work performed during the AURA reconstruction process;
5. previously established cross-repository findings for `aura-poc-a-core`, `aura-guard-v1.3`, and `aura-sign-mvp`.

This is **not a new specification**. It does not establish protocol authority, canonicality, supersession, or finality. It is a forensic synthesis baseline from which the detailed genealogy is to be expanded.

---

## 2. HARD FORENSIC RULE

No branch, commit, document, or artifact is classified as `CANONICAL`, `FINAL`, `SUPERSEDED`, `NORMATIVE`, or equivalent solely because of:

- branch name;
- filename;
- document self-description;
- PR title;
- commit message;
- apparent recency;
- presence on a branch;
- presence on `main` at some historical moment.

Status must be derived through:

```text
branch
  -> HEAD
  -> tree
  -> files
  -> commit ancestry
  -> semantic delta
  -> authority evidence
  -> status
```

The fundamental forensic distinction is:

```text
EXISTS in Git
    != REACHABLE from current main
    != CURRENT
    != AUTHORITATIVE
    != NORMATIVE
    != SUPERSEDED
```

A revert is a historical event, not proof that the reverted artifact never existed.

---

## 3. WHAT HAS BEEN ESTABLISHED ABOUT THE PROJECT'S EVOLUTION

The combined project record shows a long transition rather than one continuous, already-stable specification.

### Phase A — Genesis / conceptual system

The early AURA record developed around sovereignty, trust, entropy, behavioral identity, PoCA, vector representations, cryptographic continuity, and succession. Historical documents such as `ARCHITECT_JOURNAL_GENESIS`, `AURA_CONTEXT_BACKUP`, `CODEX_AURA`, and the early TrustMath/PoCA material belong to this conceptual layer.

These artifacts are important historical evidence of what was conceived and intended. They are not, by their existence alone, proof of present protocol authority.

### Phase B — Iron Core / frozen instrument

The project then crystallized around the ARI concept and a deterministic measurement instrument. The restore archive describes:

- Aura as Agent Reliability Measurement;
- ARI as output;
- Zero-Float Runtime;
- integer scaling by `100_000`;
- bit identity across x86/ARM/WASM;
- schema integrity gating;
- Layer 0 measurement vs Layer 2 policy separation;
- identity firewall;
- local sovereignty;
- frozen-core doctrine.

The historical restore material explicitly states that v3.3 must not be modified and that a modification creates a new lineage. fileciteturn116file3L1-L12

### Phase C — engineering reality exposes gaps

The historical `KNOWN_LIMITATIONS` record is important because it demonstrates that the frozen instrument was not equivalent to a production-complete implementation. It records, among other issues:

- evaluator layer separation leakage (`COMPLIANT` / `RISK` strings from the evaluator);
- a placeholder embedding generator based on modulo behavior;
- explicit classification of v3.3 as a structural/compliance proof-of-concept rather than a production inference engine.

The document also records a declared no-patch rule for the frozen lineage. fileciteturn116file17L1-L20

This establishes a major historical distinction: **immutability of a lineage does not prove correctness of the implementation inside that lineage.**

### Phase D — protocolization

The July 2026 system-restore work shifted the center of gravity from individual repositories toward a protocol model. The restore record explicitly describes Aura as a protocol rather than a single application and separates Mathematical Core, Evidence Model, Decision Engine, Attestation Engine, Cryptographic Core and Operational Core, with Assurance and Conformance as additional layers. fileciteturn117file1L1-L8

The same record establishes the working sequence:

```text
Specification
  -> Invariants
  -> Conformance Test Matrix
  -> Conformance Core
  -> Conformance Restoration
  -> Certification
```

It also records concrete implementation risks, including evaluator/policy leakage, global halted state, fragile hash-chain serialization, and absence of a dedicated Conformance Core. fileciteturn117file8L1-L14

### Phase E — formal specification repository

`Aura-IDToken/aura-specification` became the principal repository for APS/Constitution-oriented specification artifacts. PR #1 is the earliest established PR in the current forensic chain. It was created on 2026-07-23 and merged on the same day with merge commit `10ee452d0f2ffded08bc952f97457f994113b47e`. Its title was `[WIP] Add complete documentation for APS and Constitution`. fileciteturn114file0L2-L2

The repository subsequently accumulated APS-000, APS-100, APS-200, APS-300, APS-400, APS-500, APS-900, APS-950, Constitution, conformance records, fixtures, ADRs, governance material, evidence records and reconciliation artifacts.

### Phase F — specification hardening and reconciliation

The later branch families show a transition from merely writing specification documents toward proving canonical serialization, evidence hash domains, cross-language agreement, fixtures, conformance and governance closure.

Representative work includes:

- SPEC-002 tightening of provenance, dependency closure, hash-domain semantics and rejection behavior;
- DQ-002 hash-domain and canonical serialization work;
- CK-003 cross-language verification work;
- BC-02 boundary/fixture work;
- DQ-006 closure/reconciliation work;
- documentation normalization and reachability analysis;
- DQ-003 reference audits and reconciliation.

The forensic record must preserve these as separate historical workstreams until authority and ancestry prove how they relate.

### Phase G — governance becomes the principal blocker

The later AURA governance reconciliation established that the technical problem and the authority problem are distinct. The current governance record identified unresolved questions around:

- authority model;
- historical specification status;
- Aura-Guard lineage;
- signing role;
- specification allocation across repositories.

Therefore the current state cannot be reduced to a technical assertion such as “the latest APS documents are canonical.” The authority chain itself requires reconstruction.

---

## 4. CURRENT `aura-specification` MAIN STATE — HARD FACTS

The current `main` HEAD is:

```text
71133de047c71e0bc1156d58c20396fe593ace70
```

The commit date is `2026-09-10T22:09:45Z`.

Its commit message is:

```text
Revert "docs(dq-003): specification reconciliation control record (#34)" (#43)
```

and explicitly states that it reverts commit:

```text
74220d27f6af01f335fb1423886a51eb063f90f7
```

The current tree is therefore a **revert state** and must be treated as such in genealogy. It is not simply the chronological union of all specification work. The current main branch itself is not protected. 

The repository's forensic interpretation must therefore include both:

```text
74220d27  -- DQ-003 reconciliation state
     |
     +--> PR #43 / revert
             |
             v
71133de0  -- current main
```

The DQ-003 predecessor existed on `main` for approximately 35 seconds before the revert. The reverted state contained an APS-200 §6–10 reference audit and identified broken subsection references / missing §8.1–§8.9 material as a documented reconciliation gap. That evidence is historically real even though the artifact is not reachable from current main.

---

## 5. FIRST SPECIFICATION GENERATION EVENT

PR #1 is the first established PR in the current repository genealogy:

| Field | Evidence |
|---|---|
| PR | #1 |
| Title | `[WIP] Add complete documentation for APS and Constitution` |
| Created | 2026-07-23 18:17:09 UTC |
| Merged | 2026-07-23 19:14:08 UTC |
| Head branch | `copilot/aura-specification` |
| Head SHA | `129e66cfeeb124dc7776658a464212f6137b4e88` |
| Base | `main` |
| Merge commit | `10ee452d0f2ffded08bc952f97457f994113b47e` |

The PR's original prompt was explicitly the whole `aura-specification` documentation set, including APS and Constitution. fileciteturn114file0L2-L2

This is the beginning of the repository's formal specification genealogy, but **not necessarily the beginning of the AURA project's conceptual genealogy**. Earlier project archives predate this repository and must remain in the historical layer.

---

## 6. ARTIFACT TIMESTAMP RULE

A filename timestamp is not automatically a Git provenance timestamp.

Example established in the repository:

`APS-100 — Protocol Invariants_260723_192315.txt`

has an embedded artifact timestamp, while one of its later repository modifications occurred in commit `5f91167d0611dc91a25ebd6e1ddc3d4ce41175ca` at `2026-07-23T19:26:02Z`.

That commit performed documentation normalization across the APS set, including APS-100. Therefore future artifact cards must maintain at least two independent dates:

```text
ARTIFACT_TIMESTAMP
GIT_FIRST_APPEARANCE
```

and, where relevant:

```text
GIT_LAST_MODIFICATION
BRANCH_OBSERVED
PR_EVENT
MERGE_EVENT
REVERT_EVENT
```

The filename is evidence of an asserted document timestamp; Git is evidence of repository history. They must not be silently conflated.

---

## 7. CURRENT APS SYSTEM — FUNCTIONAL SYNTHESIS

The current repository contains a layered APS family with distinct roles:

| Artifact | Functional role | Current declared state |
|---|---|---|
| Constitution | authority / constitutional layer | requires authority reconstruction |
| APS-000 | foundation / terminology | DRAFT |
| APS-100 | protocol invariants | DRAFT |
| APS-200 | canonical data model | DRAFT |
| APS-300 | evidence model | DRAFT |
| APS-400 | conformance matrix | DRAFT |
| APS-500 | reference fixtures | DRAFT |
| APS-900 | compliance mapping | DRAFT |
| APS-950 | reference implementation requirements | DRAFT |
| EVENT_TYPE_REGISTRY | event vocabulary / registry | current artifact; authority requires provenance analysis |
| CONF-001… | concrete conformance controls | individual artifact genealogy required |
| ADR-* | architecture/decision records | authority varies; must be proven per record |
| DQ/BC/CK/GOV artifacts | reconciliation/evidence/governance | generally evidence/control material until authority is established |

The important observation is that **APS-400 and the `conformance/CONF-*` family are not the same object**: the matrix is a specification/control index, while individual CONF documents act as concrete conformance units. This relationship must be reconstructed rather than assumed.

---

## 8. MATURITY PATTERN OBSERVED IN APS

The current APS documents already contain significant formal structure, especially around deterministic data and evidence handling.

### APS-200

The current APS-200 draft defines entities ENT-001 through ENT-008, common object contracts, JCS/RFC8785 canonicalization, SHA-256 canonical bytes, RFC6962-style Merkle hashing, a concrete canonical vector, schema/fixture references and an event registry. It still contains explicit TODOs around execution IDs, request-field schema, decision vocabulary and attestation lifecycle/authority.

Therefore:

```text
technical specificity != governance finality
```

### APS-300

The evidence model separates evidence hashes from Merkle leaf hashes, defines evidence object concepts, chain/verification concepts and retention, but still carries TODOs around the Evidence Pack and EPR.

### APS-400

The conformance matrix enumerates CONF-001 through CONF-015 but the rows are declared DRAFT. Assignment is not equivalent to PASS, and certification rules depend on the actual fixture/evidence/implementation chain.

### APS-500

The fixture specification defines the role and categories of reference fixtures, but only a placeholder/initial fixture state was established in the analyzed draft. Finalization remains a separate activity.

### APS-900

The compliance mapping defines a traceability chain:

```text
Constitution
  -> APS
  -> INV
  -> ENT
  -> Evidence
  -> CONF
  -> FIX
  -> EVID
  -> RI
  -> Release
```

This is a useful structural model, but the forensic phase must prove whether each edge is actually populated and authoritative.

### APS-950

The reference implementation requirements identify RI-PY (`aura-poc-a-core-v3.3`) and RI-RS (`aura-guard-v1.3`) as implementation surfaces. That is evidence of intended integration, not by itself proof of present canonical lineage across repositories.

---

## 9. MAJOR SEMANTIC TRANSITIONS RECONSTRUCTED SO FAR

The combined historical and repository evidence indicates at least these semantic transitions:

### 9.1 Identity → behavior

Early AURA concepts centered strongly on identity/trust continuity. Later protocol work moved toward measuring observable agent behavior rather than maintaining a universal persistent reputation.

### 9.2 Behavior → measurement

The ARI concept became the principal output of the measurement instrument.

### 9.3 Measurement → evidence

Deterministic numeric output was increasingly coupled to canonical serialization, hashes, Merkle structures and evidence objects.

### 9.4 Evidence → verification

The later conformance work treats independent verification and cross-implementation agreement as separate concerns from merely producing an output.

### 9.5 Implementation → protocol

The July system-restore work explicitly shifted the framing from individual codebases to a protocol with reference implementations. fileciteturn117file2L1-L14

### 9.6 Protocol → governed assurance

The later work introduced APS, CONF, FIX, evidence, ADR/DQ/BC/GOV artifacts and reconciliation controls. This is the stage where authority, provenance and canonicality become first-class engineering objects.

---

## 10. EARLY DESIGN ELEMENTS THAT MUST REMAIN HISTORICAL UNTIL REPROVEN

Historical archives contain concepts such as:

- Global Trust Score;
- persistent identity/reputation;
- vector identity tied to persistent agents;
- cosine similarity over R^1536;
- Sentinel `0.68`;
- Sybil penalty `-1.5`;
- exponential time decay;
- pgvector/HNSW as a core substrate;
- Cosmos/ERC-4337 as infrastructure assumptions;
- NFT/RWA/tokenization product scope;
- Shamir 3/5 succession;
- M-DISC archival claims.

These are **historically significant**, but their presence in old project documents does not automatically make them part of the current protocol. The forensic map must establish exactly where, when and whether each survived into the specification genealogy.

This is especially important because the historical `AURA_CORE_SNAPSHOT_V3` calls itself a final/canonical freeze while containing concepts that later project work explicitly separated or reconsidered. The correct forensic treatment is to record the claim and then independently trace its descendants.

---

## 11. FROZEN CORE VS CURRENT SPECIFICATION — DO NOT COLLAPSE

There are two distinct historical control systems in the record:

### Frozen Instrument lineage

The restore material treats v3.3 as an immutable instrument and explicitly says modifications create a new lineage. fileciteturn116file14L1-L8

### Specification reconstruction lineage

The `aura-specification` repository contains later drafts, reconciliations, conformance records, and governance artifacts that are themselves still subject to provenance and authority analysis.

Therefore the following equation is invalid:

```text
Frozen Iron Core
  ==
Current Specification Canon
```

The forensic project must instead model their relationship explicitly.

---

## 12. GOVERNANCE LESSON FROM THE CURRENT REPOSITORY

The strongest governance finding to date is that **Git reachability is not authority**.

The documentation-normalization control review explicitly separated:

- EXISTS;
- REACHABLE;
- AUTHORITATIVE;
- CURRENT;
- NORMATIVE.

It also stated that its own controlled review created no decisions, no conflict resolutions, no supersession and no normative modification.

That model is now adopted as a forensic principle for Layer 14.

The DQ-003 revert provides a concrete example:

```text
artifact existed
      ↓
artifact reached main
      ↓
artifact was reverted
      ↓
artifact is historically real
      ↓
artifact is not currently reachable
      ↓
its authority must be assessed separately
```

---

## 13. BRANCH GENEALOGY — CURRENTLY IDENTIFIED FAMILIES

The repository currently exposes a large branch population, including families around:

- initial specification generation (`copilot/aura-specification*`);
- specification setup/structure/overhaul;
- SPEC-002 drafting and tightening;
- CK-003 canonical serialization and cross-language verification;
- DQ-002 hash-domain work;
- DQ-003 reconciliation and custody decisions;
- DQ-006 closure/reconciliation;
- BC-02 boundary/fixture work;
- RI-RS handoff;
- documentation normalization;
- governance approval/closure;
- specification recovery;
- completion/conformance;
- revert states.

At least 62 branch refs have been identified in the current forensic boundary. Multiple branch names point to identical HEAD SHAs; these are aliases of the same Git snapshot and must be deduplicated for content analysis while remaining distinct in branch genealogy.

No branch is assigned a final normative status by this synthesis.

---

## 14. RECONSTRUCTED PROCESS OF OUR AURA WORK

The project work performed across sessions itself followed a meaningful progression:

```text
1. inspect implementations
        ↓
2. identify architectural contradictions
        ↓
3. separate As-Is from To-Be
        ↓
4. reconstruct protocol layers
        ↓
5. establish invariants / evidence / conformance concepts
        ↓
6. inspect specification repository
        ↓
7. discover branch/PR proliferation
        ↓
8. identify governance and authority ambiguity
        ↓
9. stop redesign
        ↓
10. reconstruct historical genealogy
        ↓
11. derive semantic deltas
        ↓
12. derive authority graph
        ↓
13. only then establish current canonical map
```

The important methodological transition occurred when we stopped asking:

> “How should AURA be designed?”

and started asking:

> “What did AURA actually write, when, where, through which branch, with what semantic change and with what authority basis?”

That is the correct objective for the present phase.

---

## 15. CURRENT FORENSIC OUTPUT MODEL

The eventual artifact card for every file will contain at least:

```text
FILE ID
Path
Filename
Artifact type
First appearance
Artifact timestamp
First commit
First blob SHA
Last modification
Last blob SHA
Branches observed
Branch of first appearance
Parent / ancestry
PR relation
Merge relation
Revert relation
Purpose
Inputs
Outputs
References
Referenced by
Normative effect
Authority source
Authority type
Evidence basis
Semantic changes
Evidence delta
Governance delta
Supersedes
Superseded by
Current reachability
Current status
Reason
```

This is the unit from which the Master Map will be built.

---

## 16. NEXT FORENSIC EXECUTION ORDER

The remaining reconstruction must proceed in this order:

### A. PR genealogy

```text
PR #1 → PR #43
```

For each PR:

- metadata;
- head SHA;
- base SHA;
- merge SHA;
- changed files;
- semantic delta;
- authority evidence;
- merge/revert relationship.

### B. Branch registry

All identified branch refs, independently of PR membership.

### C. HEAD/tree deduplication

Group branches sharing the same HEAD/tree snapshot.

### D. File genealogy

For every file appearing in relevant branch trees:

```text
first appearance
→ modifications
→ branch transitions
→ merge/revert events
→ current reachability
```

### E. Semantic delta register

Classify changes as:

- content-only;
- terminology;
- normative candidate;
- invariant change;
- data-model change;
- serialization/hash change;
- evidence change;
- conformance change;
- governance change;
- implementation-contract change;
- documentation-only.

### F. Authority evidence register

Identify the actual evidence supporting any authority claim.

### G. Supersession/revert/conflict register

No inferred supersession. Only evidence-backed relationships.

### H. Master map

Only after A–G are sufficiently complete.

---

## 17. CURRENT FORENSIC POSITION

The project history reconstructed so far supports the following narrow conclusions:

1. AURA did not emerge as a single specification event. It evolved through multiple conceptual, implementation, specification, conformance and governance phases.
2. The `aura-specification` repository is a major formalization phase, beginning with PR #1 on 2026-07-23.
3. The current `main` branch is a revert state and therefore cannot be interpreted as a simple latest-state aggregation.
4. The repository contains technically mature drafts, but draft maturity is not the same as authority.
5. Historical “canonical/frozen” claims must be treated as claims until their authority and descendants are reconstructed.
6. The later project work correctly moved toward deterministic evidence, conformance and governance, but the authority graph remains a separate object from the technical graph.
7. The central forensic problem is now **provenance + semantic genealogy + authority**, not feature design.
8. The correct next operation is the complete branch/PR/file genealogy, not redesign of the protocol.

---

## 18. NON-GOALS

During this forensic phase we do **not**:

- redesign AURA;
- normalize contradictory historical documents into one text;
- silently repair broken specifications;
- declare a new Constitution;
- declare a new canonical APS set;
- rewrite old history;
- merge branches for convenience;
- delete historical artifacts;
- infer authority from naming conventions.

Any such action belongs to a later, explicitly authorized governance phase.

---

## 19. CONTROL STATEMENT

> **The purpose of Layer 14 is to reconstruct the history before interpreting the canon.**
>
> The resulting model must allow an independent reviewer to trace a present AURA statement backwards to the artifact, commit, branch, PR, semantic change and authority evidence from which that statement derives.

**Status:** FORENSIC BASELINE — NOT NORMATIVE  
**Authority created by this file:** NONE
