---
change: CHG-0026-use-the-release-candidate-specsync-binary-in-the-trust-workflow
artifact: context
---

# Context

The hosted Trust workflow is pinned to Trust v1.0.0, whose contract gate always
downloads released SpecSync 5.0.1. That binary predates canonical-successor
governance, so it reports CHG-0024 as stale even though this pull request's
SpecSync binary and the ordinary hosted `spec-check` job validate the accepted
CHG-0025 successor successfully.

Trust v1.0.1 adds a fail-closed release-validation input for an exact SpecSync
version and an authority-free `file://` mirror confined beneath `runner.temp`.
The workflow can therefore package the pull request's release binary with its
SHA-256 checksum and pass that runner-local mirror to the immutable Trust action.
Lifecycle, contract, Augur risk, and Attest provenance gates remain enabled.
