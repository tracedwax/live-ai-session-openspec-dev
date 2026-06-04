# Worked Example — what "good" looks like

> **Illustrative** — the `guest-checkout` example from [The OpenSpec Process](openspec-process.md), not Aspenware code. This is the **target shape**: one small, full-stack increment, a spec turned into a design and tasks. Yours will be on your own story.

## The change: `guest-checkout`

### `proposal.md` — *Product owns*
- **Why:** users abandon checkout when forced to create an account; guest checkout recovers that revenue.
- **What Changes:** an unauthenticated user can complete a lift-ticket purchase, get a confirmation email, and optionally create an account afterward.
- **Capabilities:** `guest-purchase` · `order-confirmation-email` · `post-purchase-account`
- **Impact:** checkout flow, order service, email service. **Does not** change loyalty points.

### `specs/guest-purchase/spec.md` — *Product + QA own; you review*
- WHEN an unauthenticated user submits checkout with a valid card, THEN an order is created with status `pending` and a confirmation email is queued within 5 seconds.
- WHEN the payment processor returns a timeout, THEN the order is NOT created, the cart is preserved, and the user sees a specific retry message (not a generic error).
- WHEN the guest's email matches an existing account, THEN checkout still completes as guest; the email later prompts login, not account creation.
- Does NOT change loyalty-point accrual.

### `design.md` — *you own*
- **Approach:** reuse `CheckoutController`; add a guest path that skips auth middleware. Persist via existing `OrderService` with a nullable `guestEmail`. Email via the existing queue.
- **Data:** add `guestEmail` (nullable) + `isGuest` (bool) to `orders`. No new tables.
- **Risks:** (1) duplicate accounts if post-purchase creation skips the existing-email check — mitigated by the spec; (2) cart preservation on failure needs session, not DB.
- **Tradeoffs:** reuse checkout vs. fork — reuse, to avoid drift.

### `tasks.md` — *you own*
1. Add `guestEmail` / `isGuest` to the order model + migration. *(→ design: data)*
2. Add the guest path in `CheckoutController` that bypasses auth. *(→ spec: unauth submits)*
3. Preserve the cart in session on payment timeout. *(→ spec: timeout)*
4. Queue the confirmation email within 5s of order create. *(→ spec: email)*
5. Post-purchase: prompt login if the email exists, else offer account creation. *(→ spec: existing email)*
6. Tests: happy path + timeout + existing-email. *(→ all WHEN/THEN)*

> **Notice:** split full-stack by **behavior** (`guest-purchase`), not "frontend / backend." Every task **traces to a spec decision.** If `guest-purchase` had grown past ~6–8 scenarios, it would split into two specs *before* design + tasks.
