# Square Social Studio — Stripe / Payhip Payment Status

## Status: launch blocker resolved

The original Stripe-onboarding blocker described in this file has been superseded by the completed Payhip Connect onboarding flow.

Current launch evidence:
- Stripe was connected successfully from the Payhip Payment Details page;
- Payhip showed Stripe as **Connected**;
- CAD is the Payhip default currency;
- payout banking details were entered during onboarding;
- the 30-Day Content Starter product page no longer showed the “seller unable to receive payments” warning after connection;
- a 100%-off Payhip checkout test completed and the protected ZIP download worked.

The public $27 Starter now uses Payhip as the checkout/delivery layer with connected Stripe processing rather than the older standalone Stripe Payment Link path.

## Current public checkout
Website sales page:
`https://noshabanqureshi-arch.github.io/products/30-day-content-starter/`

Payhip product:
`https://payhip.com/b/1gEcw`

## Important QA distinction
The zero-dollar test proved the Payhip order/download path. A real CAD $27 card charge was not intentionally made solely for testing.

## Standalone Stripe links
Any older standalone Stripe Payment Links should be treated as fallback/reference infrastructure, not the primary public checkout for SSS-P01, unless a later launch decision deliberately changes the architecture.

## Owner setup still worth completing over time
- dedicated business phone if needed for payment/business records;
- final custom domain;
- final business/legal operating details;
- branded support/privacy email;
- regular review of payout/account notices inside Stripe and Payhip.

Do not fabricate terms acceptance, identity information or payment details in automation.
