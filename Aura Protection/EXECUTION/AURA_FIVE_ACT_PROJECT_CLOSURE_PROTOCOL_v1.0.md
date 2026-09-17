# AURA FIVE-ACT PROJECT CLOSURE PROTOCOL v1.0

**Mode:** Controlled execution / no redesign  
**Control repository:** `vaidt/Crystal-panel-Aura-Protection`  
**Primary approval surface:** GitHub `main` only  
**Execution branch:** `execution/aura-five-act-closure-v1`  
**Date:** 2026-09-17

---

## 0. Mandate

This protocol converts the existing AURA forensic, governance, implementation and conformance evidence into a controlled five-act closure process.

It does **not** redesign AURA. It does not silently select a protocol, implementation, repository, ADR, canonical representation, or release target. Historical events remain evidence. A new decision is made only by an explicitly identified competent authority act.

The objective is to reach a state in which the statement **"AURA is a completed, controlled project"** can be made from reproducible evidence rather than from document volume, repository activity, or implementation maturity alone.

---

## 1. Operating Doctrine

### 1.1 Repository facts are not authority

```text
EXISTS ≠ REACHABLE ≠ CURRENT ≠ AUTHORITATIVE ≠ NORMATIVE
```

A commit, merge, branch, timestamp, author declaration, test result, or README cannot be promoted to authority merely by interpretation.

### 1.2 Evidence before decision

Every closure assertion must resolve to:

```text
repository → ref → commit → path → blob → content → evidence → decision
```

### 1.3 No redesign

During this protocol, implementation agents may repair, test, package and harden only after the governing contract for the affected item is established. Ambiguities are recorded and escalated; they are not resolved by implementation preference.

### 1.4 Main is the approval boundary

Working branches may contain reconstruction, analysis, test, preparation and proposed changes.

**Only changes intentionally promoted to the principal pipeline through GitHub `main` constitute project-level execution checkpoints.**

No direct force-push, hidden side channel, or external document is treated as a substitute for a mainline approval event.

### 1.5 Human authorization is exception-based

The operator is asked for explicit authorization only when the action can:

- create or change project authority;
- resolve a load-bearing governance conflict;
- select or replace the canonical protocol/implementation;
- authorize a release or production status;
- mutate protected/mainline project state in a way not already covered by an accepted decision.

Routine forensic reads, evidence indexing, reproducibility checks, tests, branch preparation, and non-authoritative reports do not require repeated operator approval.

---

# ACT I — AUTHORITY CLOSURE

## Objective

Close every authority blocker that prevents a single unambiguous execution chain.

## Inputs

- forensic reconstruction;
- Stage 06 semantic register (57/57 classifications);
- Part 6R E1–E15 provenance package;
- Stage 07 closure gate;
- AIC Registry/control records;
- current repository snapshots.

## Procedure

1. Replay the load-bearing conflicts mechanically.
2. Identify the exact competent authority act required for each blocker.
3. Do not infer acceptance from merge, chronology, authorship, or branch ancestry.
4. Record each resulting act with exact repository/path/commit/blob identity.
5. Re-run the Stage 07 gate.

## Current hard blocker

`SD-045 — ADR-001 identifier / subject collision`

The existing Stage 07 gate records:

```text
SD-045 = CONFLICTED / OPEN
Stage 07 = BLOCKED
Stage 08 = NOT AUTHORIZED
```

Therefore Act I cannot be declared complete merely by producing another analysis document. It requires a competent resolving act.

## Exit gate

PASS only when all load-bearing authority questions have an evidenced answer and no authority is inferred.

---

# ACT II — CANONICAL EXECUTION BASELINE

## Objective

Translate the resolved authority into one controlled execution baseline without redesigning the protocol.

## Required baseline

```text
AUTHORITY
  ↓
PROTOCOL ID + VERSION
  ↓
CANONICAL SEMANTICS
  ↓
REFERENCE IMPLEMENTATION
  ↓
CONFORMANCE CONTRACT
  ↓
GOLDEN VECTORS
```

## Procedure

1. Identify the authoritative protocol/version.
2. Bind canonical semantics to exact artifact identities.
3. Assign implementation responsibility explicitly.
4. Bind the reference implementation to an exact repository/ref/commit.
5. Bind conformance requirements and vectors.
6. Mark historical repositories as reference-only unless explicitly promoted.
7. Record all bindings in the AIC control plane.

## Forbidden shortcut

A technically mature implementation does not become canonical because it is more complete than another implementation.

## Exit gate

PASS only when an independent engineer can answer:

> What exactly is AURA, which version is being executed, which implementation is authoritative for execution, and against which conformance corpus is it judged?

without relying on inference.

---

# ACT III — IMPLEMENTATION + CONFORMANCE CLOSURE

## Objective

Bring the selected implementation to reproducible conformance with the established baseline.

## Procedure

1. Freeze the execution baseline.
2. Run the full applicable test suite.
3. Run cross-implementation checks where applicable.
4. Execute golden vectors.
5. Execute negative/tamper/failure cases.
6. Verify deterministic serialization, hashing, chain integrity and attestation rules where required by the canonical contract.
7. Record exact CI/run/commit evidence.
8. Repair only defects demonstrated against the established contract.
9. Re-run all affected gates after each repair.

## Closure condition

No statement such as `conformant`, `reference implementation`, `production ready`, or equivalent may be accepted without machine-verifiable evidence attached to an exact commit.

## Exit gate

PASS only when conformance is closed and reproducible from the frozen baseline.

---

# ACT IV — PRODUCTION HARDENING + RELEASE CONTROL

## Objective

Demonstrate that the conformant implementation can be released and operated under controlled conditions.

## Procedure

1. Security review and dependency review.
2. Failure-mode and recovery validation.
3. Load/throughput/resource validation appropriate to the actual deployment target.
4. Operational documentation.
5. Build/release reproducibility.
6. Supply-chain/provenance verification.
7. Version/tag/release candidate creation.
8. Verify that release artifacts correspond exactly to the approved commit.
9. Produce release evidence package.

## Exit gate

PASS only when the release candidate is traceable from authority through implementation, tests and build artifacts.

---

# ACT V — FINAL PROJECT CLOSURE

## Objective

Make the final project state auditable and freeze the completed baseline.

## Procedure

1. Execute the final AIC control-plane reconciliation.
2. Verify all M0–M7 gates.
3. Verify zero unresolved load-bearing authority conflicts.
4. Verify canonical protocol/version/implementation/conformance/release linkage.
5. Generate the final Project Closure Record.
6. Record the exact closure commit and release/tag.
7. Preserve the forensic corpus and decision history.
8. Freeze the completed baseline; future work becomes a new controlled change stream rather than an implicit continuation of the closed baseline.

## Final closure predicate

```text
PROJECT_CLOSED :=
  AUTHORITY_CLOSED
  ∧ CANONICAL_BASELINE_CLOSED
  ∧ CONFORMANCE_CLOSED
  ∧ PRODUCTION_HARDENING_CLOSED
  ∧ RELEASE_CLOSED
  ∧ FORENSIC_TRACEABILITY_COMPLETE
```

If any term is false, the project is **not closed**.

## Required final artifact

`Aura Protection/EXECUTION/AURA_PROJECT_CLOSURE_RECORD_v1.0.md`

It must contain at minimum:

- authoritative protocol/version;
- canonical artifact identities;
- reference implementation and exact commit;
- conformance corpus and results;
- golden-vector identity;
- security/hardening evidence;
- release identity;
- AIC control records;
- final authority act;
- final closure commit;
- residual known limitations, if any.

---

# 2. APPROVAL MODEL

## Normal flow

```text
WORK BRANCH
   ↓
EVIDENCE / TEST / PREPARATION
   ↓
PR
   ↓
REVIEW / GATE
   ↓
MAIN
   ↓
NEXT ACT
```

## Human approval required

Only the following require explicit operator authorization before execution/promotion:

**A. Authority-changing act**  
Resolves a load-bearing governance conflict or establishes a new competent authority state.

**B. Canonical selection**  
Selects the protocol/version/implementation that becomes the controlled execution baseline.

**C. Release authorization**  
Authorizes publication/release/production status after all technical gates pass.

**D. Exceptional destructive mutation**  
Deletion, history rewrite, force update, or other irreversible mutation affecting the controlled project record.

Routine implementation work after A/B authorization proceeds under the defined gates without requesting approval for every individual commit.

---

# 3. MAINLINE CONTROL RULE

The principal pipeline is:

```text
main
 ↓
Act I approval checkpoint
 ↓
main
 ↓
Act II approval checkpoint
 ↓
main
 ↓
Act III conformance checkpoint
 ↓
main
 ↓
Act IV release checkpoint
 ↓
main
 ↓
Act V closure checkpoint
 ↓
FINAL CLOSED BASELINE
```

A branch can be complete without being authoritative. A PR can be technically correct without being a project-level decision. A merge can be a repository event without being sufficient authority where a higher-order acceptance rule applies.

---

# 4. EXECUTION AGENT CONTRACT

The execution agent shall:

- inspect before modifying;
- preserve historical evidence;
- use exact SHAs and paths;
- keep evidence, governance and implementation records separate;
- work on branches first;
- create PRs for mainline promotion;
- stop at authority boundaries;
- request operator authorization only for the four material classes above;
- never manufacture approval, supersession, canonicality or release status;
- never redesign AURA merely to remove an ambiguity;
- report PASS/FAIL with evidence, not confidence language.

The agent shall not:

- rewrite history to hide prior events;
- delete conflicting evidence to make a gate pass;
- promote a historical repository without authority;
- treat test success as protocol authority;
- treat documentation volume as governance closure;
- declare M8 solely because implementation appears mature.

---

# 5. STATUS AT INITIALIZATION

This protocol is an execution framework, not a closure declaration.

At initialization, the previously established forensic state remains authoritative for process purposes:

```text
Part 6R provenance replay = COMPLETE
Stage 07 authority closure = BLOCKED
SD-045 = CONFLICTED / OPEN
Stage 08 = NOT AUTHORIZED
```

The five acts are therefore executed sequentially. No later act may be used to manufacture the missing authority required by an earlier act.

---

# 6. DEFINITION OF DONE

The project may be presented as **"ready / completed"** only when the final closure record can be independently reproduced from GitHub and the controlled evidence corpus, starting from the authority act and ending at the exact release/closure commit.

The standard is not:

> "We have enough documentation."

The standard is:

> **"Every material project assertion has a traceable authority, artifact identity, execution result and mainline record."**
