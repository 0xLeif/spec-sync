---
change: CHG-0027-preserve-accepted-evidence-across-valid-later-sequence-claims
artifact: testing
---

# Testing

## Requirement Evidence

- `REQ-change-029`: the three sequence-ledger unit regressions cover valid later ownership, exact current-owner bytes, and invalid later claims.

- Unit: an accepted record remains current after a valid later change advances the ledger.
- Unit: editing the ledger while evaluating its current owner changes the acceptance digest.
- Unit: malformed, orphaned, non-maximum, duplicate, and invalid collision claims remain rejected.
- Regression: CHG-0024 and CHG-0025 no longer report stale solely because CHG-0026 or CHG-0027 owns the ledger.
- Full: formatting, lint, unit/integration tests, release build, strict SpecSync, Trust, Augur, and Attest.

## Results

- Focused ledger regressions: 3 passed.
- Rust unit tests: 1,564 passed.
- Rust integration tests: 193 passed.
- Formatting, type checking, and Clippy: passed.
- Strict lifecycle check: requirement evidence is recognized; CHG-0024 and CHG-0025 remain correctly stale because `src/change.rs` changed after their accepted evidence.
