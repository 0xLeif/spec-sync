---
id: CHG-0026-use-the-release-candidate-specsync-binary-in-the-trust-workflow
state: accepted
type: operations
base_commit: 36d4751f7a32611f23b1d0f02c81b6f3b968b076
---

# Use the release candidate SpecSync binary in the Trust workflow

## Intent

Use the release candidate SpecSync binary in the Trust workflow

## Affected Canonical Specs

- None

## Acceptance Criteria

- The Trust workflow builds the pull request binary and packages it in a checksum-verified runner-local mirror while hosted Trust passes without weakening lifecycle contract risk or provenance enforcement.

## No-spec Rationale

This changes only release-validation workflow wiring; it does not change the SpecSync product contract.
