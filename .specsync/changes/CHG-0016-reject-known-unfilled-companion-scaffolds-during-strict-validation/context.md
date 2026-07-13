---
change: CHG-0016-reject-known-unfilled-companion-scaffolds-during-strict-validation
artifact: context
---

# Context

Generated companion files can retain their scaffold instructions while still
passing structural and coverage checks. That produces a false green: the
repository appears governed even though its context, requirements, or testing
evidence was never written. The validator already reads canonical companion
files, so exact recognition belongs in the shared validation path.

The check is intentionally narrow. It recognizes only strings emitted by
SpecSync's legacy and current built-in templates, only when the complete line
matches, and ignores fenced examples. Ordinary prose may discuss TODOs,
placeholders, or future work without being rejected.
