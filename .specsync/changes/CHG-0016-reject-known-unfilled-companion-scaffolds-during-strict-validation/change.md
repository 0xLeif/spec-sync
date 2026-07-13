---
id: CHG-0016-reject-known-unfilled-companion-scaffolds-during-strict-validation
state: accepted
type: bug_fix
base_commit: 60bd655c2365addc3d7a37e95f5fc20c06a746ff
---

# Reject known unfilled companion scaffolds during strict validation

## Intent

Reject known unfilled companion scaffolds during strict validation

## Affected Canonical Specs

- `validator`

## Acceptance Criteria

- Strict checks report every exact built-in companion scaffold marker with its artifact path and line; non-strict checks warn; concrete companion content passes; fenced examples and ordinary prose discussing placeholders or future work do not trigger

## No-spec Rationale

Not applicable
