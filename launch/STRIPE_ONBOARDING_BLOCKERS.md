# Square Social Studio — Stripe Onboarding Status

## Current live-account state
The Square Social Studio Stripe account exists and the product catalogue/payment link infrastructure has been created, but Stripe currently reports:

- `charges_enabled: false`
- `payouts_enabled: false`
- `details_submitted: false`

## Stripe currently requires
The account currently lists these fields as past due / currently due:

1. `business_profile.product_description`
2. `business_profile.support_phone`
3. `business_profile.url`
4. `tos_acceptance.date`
5. `tos_acceptance.ip`

## Recommended business-safe values

### Product description
Square Social Studio sells digital content-planning workbooks, templates, prompt libraries, toolkits and online educational courses for service- and expertise-based small businesses.

### Website URL
Use the current Square Social Studio website while the custom domain is being connected:
`https://noshabanqureshi-arch.github.io/`

Replace this with the custom domain after domain launch.

### Support phone
Do **not** publish a private/personal phone number just to satisfy onboarding. Use a dedicated business number. A Canadian virtual business number is acceptable if Stripe accepts it and it is actually monitored.

### Terms acceptance
The account owner must personally complete Stripe's terms acceptance. Do not automate or fabricate the acceptance IP/date.

## Checkout rule
Keep the live SSS-P01 Payment Link inactive until Stripe reports charges enabled and the delivery flow passes an end-to-end test.
