# AURA — DATA RETENTION POLICY v1.0

**Classification:** Operational governance / forensic evidence handling
**Authority:** NONE — proposed operational control
**Scope:** `vaidt/Crystal-panel-Aura-Protection` and project evidence maintained for AURA reconstruction
**Status:** PROPOSED

## 1. Purpose

This policy defines retention classes for project information and prevents accidental deletion, mutation, or uncontrolled accumulation of evidence.

It distinguishes three different meanings of retention:

1. **Data Retention** — how long project information and evidence are kept.
2. **Backup Retention** — how long recovery copies are retained.
3. **Employee/Talent Retention** — an HR metric and is outside the repository evidence lifecycle.

This file does not itself establish legal compliance, a statutory retention period, or an authority to delete evidence.

## 2. Forensic Evidence Retention

Evidence used to reconstruct AURA history MUST remain immutable at the content level while its governance status is unresolved.

### 2.1 Evidence classes

| Class | Examples | Default retention |
|---|---|---|
| EVIDENCE_SOURCE | E1–E15 source artifacts, Git blob identities, provenance manifests | Indefinite while the forensic matter remains open |
| FORENSIC_DERIVED | reconstruction records, genealogy, semantic/authority registers | Indefinite while referenced by an open finding; thereafter archive |
| GOVERNANCE_DECISION | approvals, revocations, supersession acts, closure decisions | Indefinite for auditability |
| WORKING_MATERIAL | temporary notes and non-authoritative drafts | Delete/archive when no longer required, subject to applicable legal/operational requirements |
| PERSONAL_DATA | personal information contained in project records | Retain only for the documented purpose and applicable requirement; minimize and restrict access |

## 3. Immutability Rule

Source evidence MUST NOT be overwritten in place.

Corrections or additions MUST be represented by:

```text
new artifact
    ↓
new Git object / commit
    ↓
explicit relation to predecessor
    ↓
retained predecessor
```

A corrected artifact does not erase the historical artifact it corrects.

## 4. Deletion / Disposition

Deletion of evidence that is part of an unresolved governance reconstruction is prohibited by this operational policy.

A future deletion or disposal decision requires:

- explicit scope;
- identified data class;
- documented purpose and reason for disposal;
- confirmation that no open forensic, audit, contractual, security, or legal hold applies;
- recorded decision and effective date;
- preservation of a non-sensitive disposition record where appropriate.

Where applicable law requires deletion or restriction of personal data, the legal requirement takes precedence over this operational policy, subject to preservation of the minimum lawful evidence necessary for a legitimate purpose.

## 5. Backup Retention

Backup retention is separate from source-evidence retention.

A backup may be deleted under an approved backup lifecycle even when the authoritative Git evidence remains retained. Conversely, a backup MUST NOT be treated as the canonical source of an evidence artifact when the corresponding Git object is available.

The project should maintain a documented backup schedule covering at least:

- backup frequency;
- retention period by backup class;
- encryption/access controls;
- restore testing;
- ransomware/recovery considerations;
- deletion and expiration mechanism.

No specific GFS duration is mandated by this document because the required recovery objectives have not been established here.

## 6. Personal Data and RODO/GDPR Boundary

Repository retention decisions involving personal data MUST be evaluated separately from technical evidence retention.

The project should apply data minimisation, purpose limitation, access control, and documented retention/disposal criteria appropriate to the applicable legal context.

This document does not determine the project's legal role, lawful basis, statutory retention periods, or sector-specific obligations. Those require a separate legal/compliance determination.

## 7. Automation

Automated lifecycle management MAY be introduced for eligible working data and backups.

Automation MUST NOT automatically delete unresolved forensic source evidence.

Any automated deletion rule MUST identify:

- data class;
- retention clock;
- exclusion/hold conditions;
- deletion mechanism;
- audit record;
- owner responsible for the rule.

## 8. Employee / Talent Retention

Employee retention is an HR/business metric and is not a data-retention rule for the AURA repository.

If AURA later maintains personnel or contractor records, those records require a separate HR/privacy retention schedule and access model.

## 9. Current AURA Part 6R Package

The Part 6R package under `Aura Protection/EVIDENCE/` is governed by the following minimum rule:

```text
E1–E15
  ↓
source provenance preserved
  ↓
blob SHA recorded
  ↓
no in-place mutation
  ↓
no automatic deletion while referenced by an open forensic finding
```

The package manifest is the index; the original repository objects remain the primary provenance source.

## 10. Status

**PROPOSED / NON-NORMATIVE.**

This policy creates no protocol semantics, no authority over `Aura-IDToken/aura-specification`, and no closure of Stage 07 findings.
