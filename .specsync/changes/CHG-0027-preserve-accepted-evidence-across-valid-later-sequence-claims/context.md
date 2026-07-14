---
change: CHG-0027-preserve-accepted-evidence-across-valid-later-sequence-claims
artifact: context
---

# Context

CHG-0026 advances `.specsync/change-sequence.json` as part of creating a valid later change. Strict validation then reports CHG-0024 and CHG-0025 as stale because their acceptance digests include the old ledger bytes.

The ledger is protected repository evidence and must remain covered by the lifecycle. The defect is ownership: historical accepted changes should not bind future valid sequence claims, while the current ledger owner must continue to bind the exact ledger content and invalid claims must fail closed.

Implementation validates the complete current ledger before projecting canonical historical bytes for an older record: the record's own sequence and ID are combined with the ledger's preserved collision acknowledgements. This reproduces the officially written historical claim without excluding the path, while the current owner continues hashing the exact file bytes.

Focused and full Rust tests pass. Repository-wide strict validation is intentionally blocked because CHG-0024 and CHG-0025 now have legitimate source changes inside their broad accepted scopes; both require audited reopen and fresh closing approval before the active history can return green.
