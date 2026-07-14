---
change: CHG-0027-preserve-accepted-evidence-across-valid-later-sequence-claims
artifact: research
---

# Research

`acceptance_input_digest` hashes every covered nonvolatile project path. Because `.specsync/change-sequence.json` is protected, accepted CHG-0024 and CHG-0025 bind its then-current bytes. `change new` correctly advances the ledger, but no ownership rule distinguishes that legitimate evolution from tampering.

`validate_change_sequences` already proves the ledger schema, numeric ID, maximum sequence, owner existence, collision uniqueness, exact collision membership, and historical immutability. Reusing that validation before applying the narrow digest exception avoids a parallel or weaker trust decision.
