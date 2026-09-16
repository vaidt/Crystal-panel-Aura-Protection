# AURA SPECIFICATION SYSTEM MAP v1.0

**Source:** `Aura-IDToken/aura-specification`  
**Target:** `vaidt/Crystal-panel-Aura-Protection`  
**Date:** 2026-09-16  
**Status:** NON-NORMATIVE VISUAL/STRUCTURAL MAP

## 1. Global architecture

```text
                         AURA SPECIFICATION
                                  │
                    ┌─────────────┴─────────────┐
                    │                           │
             GOVERNANCE / CANON            PROTOCOL
                    │                           │
             Constitution                 APS-000
                    │                           │
                    ▼                           ▼
                 APS-001  ─────────────────► APS-100
                                               │
                                               ▼
                                            APS-200
                                               │
                            ┌──────────────────┼──────────────────┐
                            ▼                  ▼                  ▼
                         APS-300            APS-400            APS-500
                         Evidence          Conformance         Fixtures
                            │                  │                  │
                            └──────────────────┼──────────────────┘
                                               ▼
                                            APS-900
                                          Traceability
                                               │
                                               ▼
                                            APS-950
                                      Reference Implementations
```

## 2. Protocol execution

```text
REQUEST
  ↓
VERSION / IDENTITY RESOLUTION
  ↓
VALIDATION
  ↓
POLICY RESOLUTION
  ↓
DETERMINISTIC EVALUATION
  ↓
CANONICAL RESULT
  ↓
EVIDENCE
  ↓
CANONICAL BYTES
  ↓
HASH / INTEGRITY
  ↓
AUDIT RECORD
  ↓
EVIDENCE PACK
  ↓
INDEPENDENT VERIFICATION
```

## 3. Conformance loop

```text
              NORMATIVE REQUIREMENT
                       │
                       ▼
                 PROTOCOL INVARIANT
                       │
                       ▼
                 CONF TEST
                       │
                       ▼
                 REFERENCE FIXTURE
                       │
                       ▼
                    EVIDENCE
                       │
                       ▼
              IMPLEMENTATION RESULT
                       │
                       └──────────► PASS / FAIL
```

## 4. CK-003 closure workstream

```text
CK-003
 │
 ├── APS001 invariant matrix
 ├── DQ-002 hash-domain work
 │     ├── ADR
 │     ├── defects
 │     ├── cross-language vectors
 │     ├── RFC6962 fixtures
 │     └── oracle tools
 │
 ├── DQ-006 canonical serialization
 │     ├── ADR
 │     ├── proposed APS-200 section
 │     ├── independent oracle
 │     └── closure state
 │
 ├── DQ-006 closure
 │     ├── cross-language evidence
 │     ├── consistency scan
 │     └── evidence manifest
 │
 ├── final closure execution
 ├── evidence consolidation
 ├── gates
 ├── handover assessment
 └── legacy reconciliation
```

## 5. Repository domains

```text
ROOT
│
├── specification/       Root protocol specifications
├── aps/                 Protocol modules
├── invariants/          Invariant registry
├── conformance/         Executable/defined conformance tests
├── fixtures/            Canonical/reference data
├── compliance/          Traceability
├── evidence/            Evidence packages/templates
├── ck003/               Closure and evidence workstream
├── reference/           Reference implementation lineage
├── constitution/        Constitution artifacts
├── adrs/                Architecture decisions
├── arc/                 Architecture review contracts/templates
├── docs/                Process/completion documentation
├── glossary/            Terminology
├── releases/            Release records
├── rfcs/                Change proposals
├── templates/           Document/test/fixture templates
├── scripts/             Tooling
└── .github/             Repository governance workflow
```

## 6. Boundary model

```text
┌──────────────────────────────────────────────┐
│                  GOVERNANCE                  │
│ authority / status / ownership / change      │
└──────────────────────┬───────────────────────┘
                       │
┌──────────────────────▼───────────────────────┐
│                    PROTOCOL                  │
│ APS-000 / APS-001 / APS-100 / APS-200       │
│ APS-300 / APS-400 / APS-500 / APS-900       │
└──────────────────────┬───────────────────────┘
                       │
┌──────────────────────▼───────────────────────┐
│                 ASSURANCE                   │
│ CONF / FIX / EVID / CK-003 / TRACEABILITY   │
└──────────────────────┬───────────────────────┘
                       │
┌──────────────────────▼───────────────────────┐
│               IMPLEMENTATION                │
│ RI-PY / RI-RS / future conformant systems   │
└──────────────────────┬───────────────────────┘
                       │
┌──────────────────────▼───────────────────────┐
│                 ECOSYSTEM                  │
│ Aura-Guard / Aura-vNEXT / integrations      │
└──────────────────────────────────────────────┘
```

## 7. Critical status rule

The repository currently contains many documents explicitly marked `DRAFT`, including the main APS chain. Therefore this map MUST NOT be interpreted as a declaration that all listed artifacts are approved normative law.

The map represents **structure and relationships observed in the repository**.

## 8. Branch rule

Branches are independent repository states. A branch name containing `closure`, `final`, `canonical`, `approval`, `dq`, or `ck003` does not itself confer authority.

Branch analysis must use:

```text
branch → HEAD → tree → file contents → diff → authority/status → evidence
```

## 9. Crystal Panel role

Crystal Panel is the coordination/map layer. It should expose:

```text
HISTORY
   ↕
CURRENT
   ↕
TARGET
   ↕
RECONCILIATION
   ↕
VERIFIED SYSTEM MAP
```

The map is intentionally non-normative.
