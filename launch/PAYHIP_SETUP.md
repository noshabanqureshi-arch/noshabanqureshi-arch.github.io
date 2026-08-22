# Square Social Studio — Payhip Launch Integration

## Decision
Use the GitHub Pages site as the public branded storefront and Payhip as the checkout, protected-delivery and course-access layer for launch.

Why this fits the current business:
- Digital downloads and online courses can live in one platform.
- Customers can receive protected download links after purchase.
- Course customers can have their own account and progress through lessons.
- Checkout/cart can be linked or embedded from the Square Social Studio website.
- Start on the free plan while validating demand, then review paid plan economics as revenue grows.
- Course video hosting can be added, or external video embeds can be used.

## Product map
| Internal SKU | Product | Type | CAD Price | Build status |
|---|---|---|---:|---|
| SSS-FREE-01 | 30 Content Ideas for Your Business | Lead magnet | $0 | Built |
| SSS-P01 | 30-Day Content Starter | Digital product | $27 | Built |
| SSS-P02 | Brand Voice Clarity Workbook | Digital product | $18 | Built |
| SSS-P03 | Caption Vault: 120 Prompts | Digital product | $22 | Built |
| SSS-P04 | Reels Made Simple | Digital product | $34 | Built |
| SSS-P05 | Monthly Content Dashboard | Digital product / Notion template | $28 | Built |
| SSS-P06 | Local Business Launch Pack | Digital product | $42 | Built |
| SSS-C01 | 30 Days of Content in 60 Minutes | Course + downloads | $69 | Curriculum/assets built; video production pending |
| SSS-B01 | Show Up Simply™ Toolkit | Bundle | $149 | Built; packaging/delivery QA pending |
| SSS-C02 | Show Up Simply™ Content System | Flagship course + Toolkit | $349 | 15-lesson course master built; video production pending |

## Account setup that requires the business owner
1. Create/verify the Payhip account in the legal business owner's name.
2. Connect the owner's Stripe and/or PayPal account.
3. Enter legal business/contact/tax information.
4. Configure payout and tax settings.
5. Confirm the customer-facing business name is Square Social Studio.

Do not put payment secrets, API keys or banking information in GitHub.

## Digital product setup
For each digital product:
1. Create the Payhip product using the exact title and CAD price above.
2. Upload the final customer PDF/download package.
3. Use the product description from the matching GitHub sales page.
4. Set a sensible download limit.
5. Enable PDF stamping when appropriate for portrait PDFs.
6. Add the customer licence/refund terms before checkout.
7. Complete a 100%-off test purchase before enabling the website button.

## Course setup
### 30 Days of Content in 60 Minutes
Sections / lessons:
1. Clarify Your Goal + Audience
2. Build Your Content Pillars
3. Generate 30 Useful Content Ideas
4. Turn Ideas Into Captions + Reels
5. Build the Calendar + Repeat

Include:
- lesson video
- captions/transcript
- lesson action
- 30-Day Content Starter workbook
- editable Canva companion pack
- AI prompt library

### Show Up Simply™ Content System
Five modules:
1. Clarify — goal, audience, voice
2. Plan — funnel, pillars, channels
3. Create — copy, short video, Canva
4. Publish — workflow, native formats, email
5. Repeat — KPIs, repurpose, launches

Total: 15 lessons plus five implementation checkpoints and the complete Toolkit.

## Website integration
Do not enable a purchase button until the matching Payhip product has:
- a live checkout URL
- correct price and currency
- correct uploaded files/course access
- completed policies
- successful test order

Once those URLs exist, replace each disabled website button with the corresponding Payhip checkout link or embedded checkout.

## Customer delivery QA
For every paid SKU test:
- checkout price/currency
- tax display
- terms/refund acknowledgement
- receipt
- download/course access
- mobile experience
- expired/incorrect-link handling
- support contact
- licence visibility

## Analytics
Track at minimum:
- product page view
- checkout click
- completed purchase (via available Payhip/analytics integration)
- revenue by SKU
- funnel progression from free resource to paid offer

## Security rule
Paid files, course videos and source templates must not be committed to the public GitHub repository. GitHub contains the storefront and public marketing assets only.
