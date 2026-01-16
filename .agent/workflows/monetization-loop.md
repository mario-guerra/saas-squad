---
description: Build your revenue engine with Stripe.
---

# Workflow: The Monetization Loop

1. **Architecture**: Call `SW_ARCHITECTURE_AGENT.md` and define your subscription model.
2. **Integration**: Call `PAYMENTS_AGENT.md` to generate the Stripe integration runbook and webhook logic.
3. **Audit**: Call `CODE_REVIEW_AGENT.md` (SCOPE: FILE) to perform a security audit of your payments code.
4. **Deploy**: Update your cloud environment with the new `STRIPE_API_KEY` and verify via the Stripe CLI.
