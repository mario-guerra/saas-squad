---
description: The core development loop for implementing features.
---

# Workflow: Implementation Loop

1. **Ticketing**: Call `PROJECT_MANAGEMENT_AGENT.md` with your blueprints to generate dev tickets.
2. **Coding**: Call `CODING_AGENT.md` (or `IOS_SPECIALIST_AGENT.md`) to implement a ticket.
3. **Review**: Call `CODE_REVIEW_AGENT.md` for an adversarial audit. 
4. **Fix**: If issues are found, call `CODEFIX_AGENT.md` and return to Step 3.
5. **Lock**: Once the audit is clean, call `MEMORY_PROMPT.md` to update the `SQUAD_DASHBOARD.md` and add finalized files to the `.lockedfiles` list.
