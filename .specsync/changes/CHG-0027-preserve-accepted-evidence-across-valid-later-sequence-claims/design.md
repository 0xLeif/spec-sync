---
change: CHG-0027-preserve-accepted-evidence-across-valid-later-sequence-claims
artifact: design
---

# Design

Before hashing acceptance inputs, validate the sequence ledger and determine whether its owner has a higher numeric sequence than the record being evaluated.

- Continue hashing the ledger for the current owner and any record that is not superseded by a valid later claim.
- Exclude only the valid later-owned ledger from an older record's acceptance digest.
- Propagate sequence validation failures so malformed, missing-owner, non-maximum, duplicate, or stale collision claims cannot suppress evidence checks.
- Keep source, canonical spec, change artifacts, and every other covered path unchanged in the digest.

This models the ledger as evidence owned by its current sequence claimant without weakening repository-wide lifecycle coverage.
