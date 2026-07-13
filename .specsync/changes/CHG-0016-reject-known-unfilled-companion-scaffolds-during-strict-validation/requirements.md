---
change: CHG-0016-reject-known-unfilled-companion-scaffolds-during-strict-validation
artifact: requirements
---

# Requirements

### Companion scaffold detection

The validator SHALL report an unfilled canonical companion when a non-fenced
line exactly matches a scaffold instruction emitted by a supported built-in
context, requirements, or testing template.

Acceptance Criteria
- Each finding identifies the companion artifact, repository-relative path,
  line number, and required correction.
- Strict enforcement fails when a finding remains; advisory enforcement emits
  the warning through the existing validation result.
- Concrete companion prose passes.
- Fenced examples and non-matching prose about placeholders, TODOs, or future
  work do not trigger the rule.
