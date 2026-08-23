# Square Social Studio — Payhip Launch Integration

## Launch architecture
Use the GitHub Pages site as the public branded storefront and Payhip as the checkout/protected-delivery layer for launch. Stripe is connected inside Payhip for card-payment processing.

## SSS-P01 — LIVE

### 30-Day Content Starter
- Product type: Digital Product
- Public title: `30-Day Content Starter`
- Price: **27.00 CAD**
- Internal SKU: `SSS-P01`
- Payhip product URL: `https://payhip.com/b/1gEcw`
- Website sales page: `https://noshabanqureshi-arch.github.io/products/30-day-content-starter/`
- Customer delivery: Payhip
- Payment processing: connected Stripe account through Payhip
- Website Buy button: live

### Current package
- final customer ZIP uploaded to Payhip
- 24-page workbook
- 11-page companion planning pack
- Start Here instructions
- customer licence
- PDF-only launch edition
- no Canva account required

### QA completed
- Payhip product created
- CAD $27 price displayed
- Stripe connected
- mobile 100%-off checkout test completed
- ZIP downloaded successfully through the Payhip flow

A real CAD $27 charge was not intentionally made for QA.

## SSS-FREE01 — NEXT PAYHIP PRODUCT

### 30 Content Ideas for Your Business
Ready files:
- `SSS-FREE01_30-Content-Ideas.zip`
- `SSS-FREE01_30-Content-Ideas-Cover.png`

Exact creation instructions are in:
`FREEBIE_PAYHIP_HANDOFF.md`

Launch settings:
- Digital Product
- title: `30 Content Ideas for Your Business`
- price: `0`
- currency: CAD
- visibility: Unlisted during setup
- automatic mailing-list subscription: OFF

After creation, return the Payhip product URL so the finished website freebie button can be activated.

## Why the freebie stays transactional first
The free Payhip product can collect the email needed to create/deliver the $0 order. Do not automatically turn that transactional download into ongoing marketing email until Square Social Studio has a separate permission-based email workflow with proper sender identity, mailing address, consent record and unsubscribe.

## Product map

| SKU | Product | CAD | Public checkout state |
|---|---|---:|---|
| SSS-FREE01 | 30 Content Ideas for Your Business | 0 | Payhip product to create |
| SSS-P01 | 30-Day Content Starter | 27 | **LIVE** |
| SSS-P02 | Brand Voice Clarity Workbook | 18 | Do not publish until delivery QA |
| SSS-P03 | Caption Vault: 120 Prompts | 22 | Do not publish until delivery QA |
| SSS-P05 | Monthly Content Dashboard | 28 | Notion customer duplicate path still needs QA |
| SSS-P04 | Reels Made Simple | 34 | Do not publish until delivery QA |
| SSS-P06 | Local Business Launch Pack | 42 | Do not publish until delivery QA |
| SSS-C01 | 30 Days of Content in 60 Minutes | 69 | Course media/access pending |
| SSS-B01 | Show Up Simply™ Toolkit | 149 | Bundle QA pending |
| SSS-C02 | Show Up Simply™ Content System | 349 | Course media/access pending |

## Product creation checklist for future Payhip downloads
Before activating a website purchase button:
1. final customer package exists;
2. description matches the exact files delivered;
3. price/currency are correct;
4. customer licence/refund information is available;
5. protected delivery is configured;
6. a test order/download succeeds;
7. website page reflects the tested delivery scope.

## Course creation rule
Do not create public checkout for the $69 or $349 course merely because curriculum pages exist. Lesson media, captions/transcripts, access control and a student test must be complete first.

## Security rule
Never place paid customer ZIPs, banking details, identity documents, payment secrets or customer order data in the public GitHub repository.
