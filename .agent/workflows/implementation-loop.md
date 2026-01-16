---
description: The core development loop for implementing features.
---

# Workflow: Implementation Loop

1. **Ticketing**: Call `PROJECT_MANAGEMENT_AGENT.md` with your blueprints to generate dev tickets.
2. **Memory**: Call `MEMORY_PROMPT.md` to set the sprint context.
3. **Coding**: Call `CODING_AGENT.md` (or `IOS_SPECIALIST_AGENT.md`) to implement a ticket.
4. **Memory**: Call `MEMORY_PROMPT.md` to generate technical diffs/audit context.
5. **Review**: Call `CODE_REVIEW_AGENT.md` for an adversarial audit. 
6. **Fix**: If issues are found, call `CODEFIX_AGENT.md`, then call `MEMORY_PROMPT.md`, and return to Step 5.
7. **Lock**: Once clean, call `MEMORY_PROMPT.md` to update the Dashboard and add files to `.lockedfiles`.
