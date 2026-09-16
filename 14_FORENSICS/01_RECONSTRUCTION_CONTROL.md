# AURA FORENSIC RECONSTRUCTION CONTROL

**Layer:** `14_FORENSICS`  
**Repository:** `vaidt/Crystal-panel-Aura-Protection`  
**Source:** `Aura-IDToken/aura-specification` + established AURA historical evidence  
**Mode:** reconstruction only / no redesign

## Objective

Reconstruct, with evidence, how AURA became its current observable state.

The reconstruction records **what was actually written**, **when**, **where**, **through which branch/commit/PR**, **what changed semantically**, and **what authority evidence existed at that point**.

## Mandatory evidence chain

```text
BRANCH
  ↓
HEAD SHA
  ↓
TREE SHA
  ↓
FILE INVENTORY
  ↓
BLOB / CONTENT
  ↓
COMMIT ANCESTRY
  ↓
PR / MERGE / REVERT RELATION
  ↓
SEMANTIC DELTA
  ↓
NORMATIVE DELTA
  ↓
EVIDENCE DELTA
  ↓
GOVERNANCE DELTA
  ↓
AUTHORITY EVIDENCE
  ↓
FORENSIC STATUS
```

## Status discipline

Until the chain above is established, use `UNRESOLVED` or a narrower evidence-only description.

Do not infer:

- `CANONICAL` from branch name;
- `FINAL` from filename or PR title;
- `SUPERSEDED` without replacement evidence;
- `NORMATIVE` from document self-description;
- `CURRENT` merely because an artifact is recent;
- `AUTHORITATIVE` merely because an artifact reached `main`.

## Date discipline

For every artifact, distinguish:

1. embedded artifact timestamp;
2. first known Git appearance;
3. first commit;
4. last modification;
5. branch observation;
6. PR creation/merge/revert event.

These timestamps are different evidence classes.

## Historical preservation

A reverted artifact remains part of AURA's history. A deleted file remains part of history if its Git provenance is recoverable. A branch that never merged remains evidence of a development path, but not automatically of authority.

Contradictions, duplicate artifacts, aliases, incomplete work, failed closure attempts and broken references are preserved as historical facts.

## Scope

### Primary repository genealogy

`Aura-IDToken/aura-specification`

### Target forensic repository

`vaidt/Crystal-panel-Aura-Protection`

### PR boundary

`PR #1 → PR #43`

### Branch boundary

All identified surviving branch refs, currently 62 in the forensic boundary.

### Artifact boundary

Every relevant file appearing in the examined trees, including specifications, evidence, conformance, fixtures, governance, ADRs, templates, reports and historical records.

## Output contract

The completed Layer 14 reconstruction must allow an independent reviewer to trace a current or historical AURA statement backwards to:

```text
statement
  → artifact
  → blob/content
  → commit
  → branch
  → PR/event
  → ancestry
  → semantic change
  → authority evidence
```

## Explicit non-goals

This phase does not:

- redesign AURA;
- repair historical specifications;
- silently reconcile contradictions;
- create protocol authority;
- declare a new canonical set;
- delete historical material;
- rewrite Git history;
- substitute model inference for missing evidence.

## Current control status

`ACTIVE — FORENSIC RECONSTRUCTION`

**Authority created by this control record:** NONE  
**Normative effect on AURA protocol:** NONE
