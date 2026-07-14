---
change: CHG-0027-preserve-accepted-evidence-across-valid-later-sequence-claims
artifact: plan
---

# Plan

1. Add a fail-closed helper that recognizes a fully valid later sequence-ledger owner.
2. Exclude that one evolving system path from predecessor acceptance digests while retaining current-owner hashing.
3. Add regression tests for valid successor creation, current-owner tampering, and invalid ledger ownership.
4. Update the canonical `change` contract and companions.
5. Run focused tests, strict SpecSync, the repository lane, Trust, Augur, and Attest.
