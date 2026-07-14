---
id: CHG-0027-preserve-accepted-evidence-across-valid-later-sequence-claims
state: accepted
type: bug_fix
base_commit: 36d4751f7a32611f23b1d0f02c81b6f3b968b076
---

# Preserve accepted evidence across valid later sequence claims

## Intent

Preserve accepted evidence across valid later sequence claims

## Affected Canonical Specs

- `change`

## Acceptance Criteria

- Creating a valid later change leaves prior accepted evidence current; manual sequence-ledger tampering and invalid owner claims still fail closed; focused regression tests and the full strict Trust lane pass.

## No-spec Rationale

Not applicable
