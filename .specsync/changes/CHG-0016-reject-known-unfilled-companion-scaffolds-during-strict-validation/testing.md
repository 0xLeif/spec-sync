---
change: CHG-0016-reject-known-unfilled-companion-scaffolds-during-strict-validation
artifact: testing
---

# Testing

`REQ-validator-002` is exercised by the focused unit and CLI integration
coverage below.

- Unit coverage enumerates every supported marker across context,
  requirements, and testing companions and verifies artifact/path/line output.
- Unit coverage proves fenced Markdown examples and legitimate explanatory
  prose are ignored.
- A CLI integration fixture proves `check --strict --force` fails with an
  unfilled marker and passes after replacement with concrete evidence.
- Run `fledge run fmt`, `fledge run lint`, `fledge run test`, the strict spec
  check, and the repository verification lane before closing approval.
