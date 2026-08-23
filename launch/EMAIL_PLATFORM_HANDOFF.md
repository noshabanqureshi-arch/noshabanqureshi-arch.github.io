# Square Social Studio — Email Platform Handoff

## Goal
Add a permission-based marketing sequence later without holding up the current self-serve Payhip product/download funnel.

## Phase 1 — CURRENT

### Transactional delivery
Use Payhip for:
- paid order/receipt records;
- protected paid downloads;
- the upcoming $0 freebie order/download;
- the email address needed to create and deliver the Payhip order/download.

Do **not** automatically describe the Payhip freebie order as consent to ongoing Square Social Studio marketing email.

The freebie Payhip product should therefore have **Automatically subscribe customers to mailing list = OFF** during the first setup.

## Phase 2 — PERMISSION-BASED MARKETING EMAIL
Activate only after Square Social Studio has:
- a branded sender/support email;
- a valid business mailing address suitable for the commercial-email footer;
- a selected email platform;
- clear consent language;
- consent timestamp/source records;
- a working unsubscribe mechanism;
- tested mobile rendering.

## Required audience fields
When the marketing platform is connected, capture at minimum:
- Email address
- First name (optional)
- Consent timestamp
- Consent source/form
- Lead magnet source
- Purchase status / product SKU when available

## Recommended marketing consent copy

**Headline:** Get practical content-planning ideas from Square Social Studio.

**Body:** Useful systems, examples and relevant product updates for service- and expertise-based small businesses.

**Consent checkbox:**
`Yes, send me occasional Square Social Studio emails with practical content-planning ideas and relevant offers. I can unsubscribe at any time.`

Do not pre-check the box.

## Marketing automation
Trigger: valid signup with the required marketing consent.

Sequence:
1. Day 0 — orient the subscriber and link to the free resource.
2. Day 1 — Teach / Trust / Connect / Offer / Convert framework.
3. Day 3 — introduce the $27 30-Day Content Starter.
4. Day 5 — teach Clarify → Plan → Create → Publish → Repeat.
5. Day 7 — show logical next levels without pretending unfinished courses are already open.

Source copy:
`launch/WELCOME_EMAIL_SEQUENCE.md`

## Required marketing-email footer
- Square Social Studio sender identity
- valid business mailing address
- working unsubscribe link
- business support/contact method

## Suggested segments
- Leads — Freebie / Marketing Consent
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

## Purchase automation rules
When a provider is connected:
- let Payhip handle receipts/downloads;
- sync/tag purchases by SKU where possible;
- exclude a current purchaser from repeated promotional email for the same product;
- continue useful educational email only where consent permits;
- offer the next logical product only when it is actually ready and relevant.

## First marketing-email test
Before scheduling the sequence, confirm:
1. consent is recorded;
2. sender identity is correct;
3. business mailing address is in the footer;
4. unsubscribe works;
5. sequence timing is correct;
6. purchase tags/suppression work where available;
7. mobile rendering is clean;
8. Email 1 contains the final freebie access link.
