# AURA — Part 6R Source Index

**Package branch:** `forensics/part-6r-evidence-package`
**Base:** `main`
**Evidence mode:** read-only recovery / provenance preservation

## Source map

| ID | Repository | Path | GitHub ref |
|---|---|---|---|
| E1 | `vaidt/Crystal-panel-Aura-Protection` | `14_FORENSICS/07_ADR001_SUPERSESSION_AUTHORITY_PATH_RECONSTRUCTION_v1.0.md` | `main` |
| E2 | `vaidt/Crystal-panel-Aura-Protection` | `14_FORENSICS/07_ADR001_SD045_CLOSURE_GATE_v1.0.md` | `main` |
| E3 | `vaidt/Crystal-panel-Aura-Protection` | `14_FORENSICS/07_AUTHORITY_EVIDENCE_RECORD_ADR001_COLLISION_v1.0.md` | `main` |
| E4 | `vaidt/Crystal-panel-Aura-Protection` | `14_FORENSICS/07_AUTHORITY_REENTRY_ADR001_COLLISION_v1.0.md` | `main` |
| E5 | `Aura-IDToken/aura-specification` | `adrs/ADR-001_REPOSITORY_STRUCTURE.md` | `main` |
| E6 | `Aura-IDToken/aura-specification` | `adrs/ADR-001_DOCUMENT_MODEL.md` | `main` |
| E7 | `Aura-IDToken/aura-specification` | `docs/adr/001-document-model.md` | `main` |
| E8 | `Aura-IDToken/aura-specification` | `GOVERNANCE.md` | `main` |
| E9 | `Aura-IDToken/aura-specification` | `adrs/README.md` | `main` |
| E10 | `Aura-IDToken/aura-specification` | `releases/v0.1.0/DOCUMENT_STATUS.md` | `main` |
| E11 | `Aura-IDToken/aura-specification` | `releases/v0.1.0/RELEASE_NOTES.md` | `main` |
| E12 | `Aura-IDToken/aura-specification` | `ck003/handover-assessment/05_EVIDENCE_GAPS.md` | `main` |
| E13 | `Aura-IDToken/aura-specification` | `ck003/handover-assessment/09_RECOMMENDED_SEQUENCE.md` | `main` |
| E14 | `Aura-IDToken/aura-specification` | `AURA-DOCUMENTATION-NORMALIZATION-AUDIT-v1.md` | `main` |
| E15 | `vaidt/Crystal-panel-Aura-Protection` | `14_FORENSICS/07_AUTHORITY_ACT_REGISTER_v1.0.md` | `main` |

## Integrity rule

The source path and blob SHA in `MANIFEST.json` are the primary identity fields. A later source change does not retroactively change the evidence object identified by its earlier blob SHA.

## Branch rule

This branch contains package/index metadata and operational retention controls. It does not alter the source artifacts in `Aura-IDToken/aura-specification`.

The branch is intentionally **not merged automatically**. Review and merge remain separate governance events.
