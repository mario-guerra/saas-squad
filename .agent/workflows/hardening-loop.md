---
description: How to inherit and stabilize an existing codebase close to launch.
---

# Workflow: The Hardening Loop

1. **Bootstrap**: Call `BOOTSTRAP_AGENT.md` and select "Option C: Project Hardening / Alignment."
2. **Memory**: Call `MEMORY_PROMPT.md` to persist the legacy context.
3. **Readiness Audit**: Call `HARDENING_AGENT.md` to perform a Stability & Readiness Audit (SRA). 
4. **Memory**: Call `MEMORY_PROMPT.md` to persist the Alignment Roadmap.
5. **Instrumentation**: Call `OBSERVABILITY_AGENT.md` to fill technical "Blind Spots" identified in the SRA.
6. **Execution**: Follow the **Implementation Loop** to codify logs, metrics, and tracing fixes.
7. **Verification**: Call `CODE_REVIEW_AGENT.md` for a deep adversarial audit of the most sensitive legacy modules.
8. **Finalization**: Implement **File Locking** for audited legacy assets using the standard `.lockedfiles` manifest.
