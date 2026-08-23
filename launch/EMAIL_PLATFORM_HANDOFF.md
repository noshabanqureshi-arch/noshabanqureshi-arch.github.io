# Square Social Studio — Email Platform Handoff

## Goal
Connect the existing five-email sequence to a real permission-based email platform without rewriting the funnel.

## Required audience fields
- Email address
- First name (optional)
- Consent timestamp
- Consent source/form
- Lead magnet source
- Purchase status / product SKU when available

## Freebie form
Offer: `30 Content Ideas for Your Business`

Recommended form copy:

**Headline:** Get 30 useful content ideas for your business.

**Body:** A practical idea bank for service-based small businesses that want clearer content without posting for the sake of posting.

**Consent checkbox:**
`Yes, send me the free resource and occasional Square Social Studio emails with practical content-planning ideas and offers. I can unsubscribe at any time.`

Do not pre-check consent.

## Automation
Trigger: confirmed/valid lead-magnet signup with required marketing consent.

Sequence:
1. Day 0 — Deliver the free resource and set expectations.
2. Day 1 — Teach the Teach / Trust / Connect / Offer / Convert framework.
3. Day 3 — Introduce the $27 30-Day Content Starter.
4. Day 5 — Teach the Show Up Simply™ framework.
5. Day 7 — Present the logical next levels: $27 / $69 / $149 / $349 according to readiness.

Source copy already exists in `launch/WELCOME_EMAIL_SEQUENCE.md`.

## Required footer on marketing emails
- Square Social Studio sender identity
- Valid business mailing address
- Working unsubscribe link
- Business support/contact method

Do not activate marketing sends until the final business mailing address/contact identity is available.

## Segments to create
- Leads — Freebie
- Customers — Any Purchase
- Customers — SSS-P01
- Customers — SSS-P02
- Customers — SSS-P03
- Customers — SSS-P04
- Customers — SSS-P05
- Customers — SSS-P06
- Customers — SSS-B01
- Students — SSS-C01
- Students — SSS-C02

## Purchase automations
For each paid product:
- purchase/receipt handled by commerce platform;
- tag by SKU;
- exclude current product purchasers from promotional emails for that same product;
- continue useful educational emails where consent permits;
- offer the next logical product only when relevant.

## First test
Use a test email and confirm:
1. signup recorded;
2. consent recorded;
3. free resource delivered;
4. unsubscribe works;
5. sequence timing is correct;
6. purchase tags suppress duplicate sales messaging;
7. mobile email rendering is clean.