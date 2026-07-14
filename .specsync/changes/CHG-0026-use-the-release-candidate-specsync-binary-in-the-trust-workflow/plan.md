---
change: CHG-0026-use-the-release-candidate-specsync-binary-in-the-trust-workflow
artifact: plan
---

# Plan

1. Build the release candidate with the locked Cargo dependency graph.
2. Package `specsync-linux-x86_64.tar.gz` beneath `runner.temp` using the exact
   filename and archive layout required by the pinned SpecSync action.
3. Generate the adjacent SHA-256 file and pin the verified Trust v1.0.1 commit.
4. Pass SpecSync version 5.0.2 and the runner-local mirror into the Trust action.
5. Verify workflow syntax and rerun the hosted Trust check without changing the
   committed Trust policy or disabling any gate.
