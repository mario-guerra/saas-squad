---
description: The sequence for identifying, reproducing, and fixing production bugs.
---

# Workflow: The Debug-Fix Loop

1. **Auditing**: Call `DEBUGGING_AGENT.md` with logs or stack traces to perform a forensic audit.
2. **Memory**: Call `MEMORY_PROMPT.md` to persist the Root Cause Analysis (RCA).
3. **Reproduction**: Direct the agent to generate the specific regression test required to reproduce the bug.
4. **Fixing**: Call `CODEFIX_AGENT.md` to implement the surgical remediation based on the RCA.
5. **Memory**: Call `MEMORY_PROMPT.md` to prepare the handoff for verification.
6. **Re-Audit**: Call `CODE_REVIEW_AGENT.md` to ensure the fix is secure and doesn't introduce regressions.
