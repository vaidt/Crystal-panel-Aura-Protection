# AIC CURRENT REPOSITORY SNAPSHOT — 2026-09-17

**Role:** exact current ref/commit snapshot for AIC control records.  
**Authority created:** NONE.  
**Purpose:** prevent branch names and repository names from being treated as sufficient artifact identity.

## 1. Verified current refs

| Repository | Ref | Current commit SHA | Status |
|---|---|---|---|
| `Aura-IDToken/aura-specification` | `main` | `71133de047c71e0bc1156d58c20396fe593ace70` | VERIFIED CURRENT REF |
| `vaidt/Aura-vNEXT` | `claude/aura-vnext-genesis-xerti8` | `bdec831c165b3a5465bc25f325ed801558cbf81a` | VERIFIED DEFAULT REF; default branch is not `main` |
| `vaidt/Aura-Guard` | `main` | `7d2f5746ae61a66edcd11d75bff0787bed854363` | VERIFIED CURRENT REF |
| `AuraIDToken/Aura-Conformance-Kit` | `main` | `375391e2a07dbca532ae614ad72155c71cba5267` | VERIFIED CURRENT REF |
| `vaidt/Crystal-panel-Aura-Protection` | `main` | `17d5ed78f2469fece01d55699b4105dced12daae` | VERIFIED CURRENT REF at snapshot time |

## 2. Interpretation rules

`Aura-vNEXT` has a default branch named `claude/aura-vnext-genesis-xerti8`. This is a repository fact only; it is not itself a governance determination.

For all repositories, the AIC identity tuple remains:

```text
repository
ref
commit_sha
path
blob_sha
```

A current repository commit does not prove that every artifact in that repository is current, normative, conformant, or authorized for deployment.

## 3. Governance anchors

### Protocol

`Aura-IDToken/aura-specification` is recorded by the current governance baseline as the normative protocol specification under the D-8 authority model.

### Implementation

`vaidt/Aura-vNEXT` is recorded as the current canonical implementation role. The role does not transfer Protocol Authority to the repository.

### Guard

`vaidt/Aura-Guard` is recorded as the current Guard demonstration role under D-3. It is not recorded as successor/reimplementation/normative replacement of `Aura-IDToken/aura-guard-v1.3`.

### Conformance

`AuraIDToken/Aura-Conformance-Kit` is recorded as a conformance candidate. D-10 governs Conformance Authority, but repository allocation remains a separate question where not explicitly established.

### Control plane

`vaidt/Crystal-panel-Aura-Protection` is the ecosystem control-plane / governance mapping repository. It does not become Protocol Authority merely by storing the AIC Registry.

## 4. Snapshot limitations

This document records exact current repository refs and commits only. It does not claim that all files within those refs have been exhaustively inventoried here.

For load-bearing artifacts, the AIC Registry requires the additional exact `path` and `blob_sha` fields plus provenance and authority evidence.

## 5. Control status

```text
SNAPSHOT: VERIFIED
AUTHORITY CREATED: NONE
NORMATIVE CHANGE: NONE
IMPLEMENTATION CHANGE: NONE
USE: TRACEABILITY / EXECUTION GATING
```
