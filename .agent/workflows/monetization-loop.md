---
description: Build your revenue engine with Stripe.
---

# Workflow: The Monetization Loop

1. **Architecture**: Call `SW_ARCHITECTURE_AGENT.md` and define your subscription model.
2. **Memory**: Call `MEMORY_PROMPT.md` to persist the revenue model.
3. **Integration**: Call `PAYMENTS_AGENT.md` to generate the Stripe logic.
4. **Memory**: Call `MEMORY_PROMPT.md` to generate audit context for payment logic.
5. **Audit**: Call `CODE_REVIEW_AGENT.md` (SCOPE: FILE) to perform a security audit.
6. **Deploy**: Update your environment with `STRIPE_API_KEY` and call `MEMORY_PROMPT.md` to finalize.
