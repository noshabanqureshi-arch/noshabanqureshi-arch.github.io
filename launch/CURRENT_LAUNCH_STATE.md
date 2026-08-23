# Square Social Studio — Current Launch State

**Canonical status — August 23, 2026**

This file supersedes older launch notes that describe Stripe onboarding, Canva access or SSS-P01 delivery as unresolved.

## LIVE NOW

### Public website
- Main Square Social Studio storefront is live on GitHub Pages.
- The 30-Day Content Starter sales page is live.
- Public Privacy Notice, Digital Product Terms and Digital Product Licence are live.
- Paid customer support guidance is live at `/contact/` without exposing a personal email or phone number.

### SSS-P01 — 30-Day Content Starter
- Public price: **CAD $27**.
- Website Buy button: **LIVE**.
- Public checkout/delivery: **Payhip**.
- Payhip product link: `https://payhip.com/b/1gEcw`.
- Stripe is connected inside Payhip.
- Customer package has been replaced with the final PDF-only ZIP.
- Delivery test completed successfully using a 100%-off order on mobile; the ZIP downloaded successfully.
- A real CAD $27 card charge has not been intentionally made as part of QA.

### Current SSS-P01 deliverables
- 24-page 30-Day Content Starter workbook
- 11-page companion planning pack
- Start Here instructions
- customer licence
- PDF-only delivery; no Canva account or editable Canva template is required

## FREEBIE — READY, ONE MANUAL PAYHIP STEP LEFT

### SSS-FREE01 — 30 Content Ideas for Your Business
Ready locally:
- `SSS-FREE01_30-Content-Ideas.zip`
- 8-page PDF guide
- Start Here instructions
- `SSS-FREE01_30-Content-Ideas-Cover.png`

The website landing page is finished but intentionally does not contain a fake signup form or broken checkout URL.

Remaining action:
1. create the $0 digital product in Payhip;
2. upload the ready ZIP and cover;
3. keep it Unlisted initially;
4. copy the resulting Payhip product link;
5. replace the disabled freebie button on the website with that link.

Exact setup is in `launch/FREEBIE_PAYHIP_HANDOFF.md`.

## EMAIL

### Ready
- Five-email welcome/nurture sequence is drafted.
- CASL implementation checklist exists.
- Email platform handoff requirements exist.

### Intentionally NOT active yet
Do not automatically subscribe freebie downloaders to an ongoing marketing sequence until the business has:
- a permanent business mailing address suitable for commercial-email identification;
- branded sender/support email;
- consent records;
- working unsubscribe mechanism;
- chosen email provider/configuration.

Phase 1 freebie delivery should therefore be transactional/self-serve through Payhip. Marketing consent can be added later as a separate permission step.

## ANALYTICS

- No advertising pixel or third-party marketing analytics script has intentionally been added to the GitHub Pages site.
- UTM conventions and event names are documented.
- Use Payhip order/sales data as the first source of truth for revenue.
- A website analytics provider can be added later after the privacy/cookie setup is chosen.

## FIRST REVENUE TEST

Working experiment, not a guarantee:
- target: 1,000 qualified Starter-page visits;
- working purchase assumption: 4%;
- 40 purchases x CAD $27 = CAD $1,080 gross.

Do not add more products merely because traffic is low. After the first meaningful sample, diagnose traffic quality, page clarity, checkout friction and purchase conversion.

## OTHER OFFERS

Other low-ticket products, the $69 mini-course, $149 Toolkit and $349 flagship remain separate from the first launch. Do not publish their checkout buttons until their own protected delivery/course access is verified.

## OWNER-ONLY ITEMS THAT STILL MATTER

These do not need to block the current $27 self-serve product page, but they should be completed as the business becomes more public:
- final legal operating/trade-name structure;
- dedicated business mailing address for public/commercial-email use;
- dedicated business phone if needed;
- branded business domain;
- branded `support@` / `privacy@` / sender email;
- final email-marketing provider and consent workflow;
- professional review of final legal/customer policies for the actual business setup.

## SECURITY RULE

Never commit banking information, identity documents, private customer data, payment card data, passwords, API secrets, paid customer ZIPs or private course media to the public GitHub repository.
