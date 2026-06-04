# Worked Example

An illustrative example, the guest-checkout case from the OpenSpec process page. It is not Aspenware code. It shows the shape you are aiming for: one small full-stack increment, a spec turned into a design and tasks. Yours will be on your own story.

## The change: guest-checkout

### proposal.md

Why: users abandon checkout when they are forced to create an account, and guest checkout recovers that revenue.

What changes: an unauthenticated user can complete a lift-ticket purchase, get a confirmation email, and optionally create an account afterward.

Capabilities: guest-purchase, order-confirmation-email, post-purchase-account.

Impact: the checkout flow, the order service, and the email service. It does not change loyalty points.

### specs/guest-purchase/spec.md

WHEN an unauthenticated user submits checkout with a valid card, THEN an order is created with status pending and a confirmation email is queued within 5 seconds.

WHEN the payment processor times out, THEN the order is not created, the cart is preserved, and the user sees a specific retry message rather than a generic error.

WHEN the guest's email matches an existing account, THEN checkout still completes as a guest, and the email later prompts login rather than account creation.

It does not change loyalty-point accrual.

### design.md

Approach: reuse the existing checkout controller and add a guest path that skips the auth middleware. Persist through the existing order service with a nullable guestEmail. Send the email through the existing queue.

Data: add guestEmail, nullable, and isGuest to the orders table. No new tables.

Risks: duplicate accounts if post-purchase creation skips the existing-email check, which the spec guards against; and cart preservation on failure needs the session, not the database.

Tradeoffs: reuse the checkout path rather than fork it, to avoid drift.

### tasks.md

1. Add guestEmail and isGuest to the order model, with a migration. Comes from the design's data section.
2. Add the guest path in the checkout controller that bypasses auth. Comes from the spec's unauthenticated-submit behavior.
3. Preserve the cart in the session on a payment timeout. Comes from the spec's timeout behavior.
4. Queue the confirmation email within 5 seconds of order creation. Comes from the spec's email behavior.
5. After purchase, prompt login if the email exists, otherwise offer account creation. Comes from the spec's existing-email behavior.
6. Tests for the happy path, the timeout, and the existing-email case. Cover all the WHEN/THEN behaviors.

Notice that the split is by behavior, guest-purchase, and not by frontend or backend. Every task traces to a spec decision. If guest-purchase had grown past six to eight scenarios, it would split into two specs before the design and tasks.
