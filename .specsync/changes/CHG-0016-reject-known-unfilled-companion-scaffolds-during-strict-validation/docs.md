---
change: CHG-0016-reject-known-unfilled-companion-scaffolds-during-strict-validation
artifact: docs
---

# Docs

Update the validator contract and requirement companion to state that known
built-in companion scaffold lines are reported as actionable warnings. Strict
mode already treats warnings as errors, so no new CLI option or configuration
surface is introduced.
