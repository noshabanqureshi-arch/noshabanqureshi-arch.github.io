# Square Social Studio — Payments Architecture

Purpose: keep payment administration low while matching each offer to the simplest delivery and billing system.

## Current live state

### 30-Day Content Starter — CAD $27
- Keep checkout on **Payhip**.
- Payhip handles the customer checkout and protected digital delivery.
- Stripe remains the connected payment processor behind the current setup.
- Do not rebuild this product into a custom Stripe checkout merely because Stripe is active.

## Future one-time digital products

Examples:
- Brand Voice Clarity Workbook
- Caption Vault
- Reels Made Simple
- Monthly Content Dashboard
- Local Business Launch Pack
- Show Up Simply™ Toolkit
- self-paced courses

### Recommended default
Keep these on **Payhip or the selected protected course/digital-delivery platform** when the platform can:
- take the one-time payment,
- deliver the files/access automatically,
- handle receipt/access emails,
- protect customer files better than a public static site,
- reduce owner admin.

Do not move a one-time digital product to direct Stripe unless doing so creates a clear customer or operational advantage.

## Square Social Vault — planned CAD $99/month

### Recommended billing model
- Stripe Billing
- flat-rate monthly subscription
- pay up front at signup
- no free trial by default during first validation
- no seat/usage pricing

### Recommended checkout
Use the lowest-maintenance hosted/no-code option available when the Vault delivery platform is ready:
1. Stripe-hosted subscription checkout / Payment Link, or
2. a native Stripe integration offered by the selected membership platform.

Avoid a custom checkout unless the delivery platform genuinely requires it.

### Subscription management
Enable a Stripe-hosted Customer Portal so members can:
- update payment method,
- view billing history where available,
- cancel according to the published membership terms,
- manage subscription without emailing the owner for routine billing changes.

Default cancellation approach: end access at the end of the paid billing period unless the final membership terms require another approach.

### Failed payments
Use Stripe's automated recovery tools / Smart Retries and customer billing emails when the Vault launches. Do not create a founder-managed manual chasing process for routine card failures.

## Done-for-You — maximum 3 clients

### Recommended billing approach
Because volume is intentionally tiny, use the simplest B2B process rather than building automation for dozens of accounts.

Options, in order of preference:
1. Stripe recurring billing/subscription when scope and monthly fee are fixed.
2. Stripe Invoice when scope, start date or terms need manual control.

Use hosted Stripe payment/invoice pages rather than collecting card information directly.

### Service rules
- signed agreement + first payment before onboarding,
- fee and scope tied to the 12–15 owner-hour monthly service budget,
- re-scope/re-price if actual delivery hours exceed budget repeatedly,
- no unlimited revisions,
- no daily on-call community management,
- no client #4 as a revenue solution.

## What not to build
- No shopping cart on GitHub Pages.
- No raw card collection.
- No custom Stripe Elements integration unless a future product requires capabilities hosted checkout cannot provide.
- No separate checkout technology for every product.
- No live Vault subscription until the membership content/access system passes QA.
- No paid course checkout until protected course access and lesson media pass QA.

## Sandbox test plan before Vault launch
When Vault delivery is ready:
1. Create a sandbox Vault product and CAD $99/month flat-rate recurring price.
2. Create sandbox hosted subscription checkout/payment link.
3. Complete a test subscription.
4. Confirm successful-payment state reaches the Vault access workflow.
5. Test failed payment handling.
6. Test customer portal payment-method update.
7. Test cancel-at-period-end.
8. Confirm access ends correctly after cancellation period.
9. Verify customer-facing receipts/emails and business identity.
10. Only then reproduce the tested setup in live mode.

## Decision rule
Payment technology should reduce owner administration and protect the customer experience. Revenue growth should come from better offers, recurring intellectual property and distribution—not from building a custom payments stack.
