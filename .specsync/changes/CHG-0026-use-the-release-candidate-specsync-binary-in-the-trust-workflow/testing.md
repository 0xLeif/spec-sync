---
change: CHG-0026-use-the-release-candidate-specsync-binary-in-the-trust-workflow
artifact: testing
---

# Testing

- Validate the workflow structure with the repository's action validation task.
- Re-run the local Trust gate against `target/debug/specsync`.
- Confirm the hosted `trust` job installs the checksum-verified runner-local
  release candidate and passes lifecycle, contract, risk, and provenance gates.
- Confirm all other pull-request checks remain green.
