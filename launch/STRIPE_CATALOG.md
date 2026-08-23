# Square Social Studio — Stripe Catalogue / Payment Architecture

Live Stripe account: Square Social Studio
Currency: CAD
Payment model: one-time purchases at launch

## Current public architecture

For **SSS-P01 — 30-Day Content Starter**, the public path is now:

GitHub Pages sales page
→ Payhip checkout/delivery
→ connected Stripe payment processing
→ Payhip protected download

Public Payhip product:
`https://payhip.com/b/1gEcw`

Older standalone Stripe products/prices remain useful internal catalogue/fallback infrastructure but are not the primary public SSS-P01 checkout.

## Existing Stripe catalogue

| SKU | Offer | CAD | Stripe Price ID | Lookup Key | Public state |
|---|---|---:|---|---|---|
| SSS-P02 | Brand Voice Clarity Workbook | 18 | `price_1U7UhkJZF520sfDczSz25jVW` | `sss_brand_voice_clarity_18` | Not public |
| SSS-P03 | Caption Vault: 120 Prompts | 22 | `price_1U7UhtJZF520sfDc6SAa4D0o` | `sss_caption_vault_22` | Not public |
| SSS-P01 | 30-Day Content Starter | 27 | `price_1U7Ui2JZF520sfDcEy2h8GtW` | `sss_30_day_starter_27` | Public through Payhip |
| SSS-P05 | Monthly Content Dashboard | 28 | `price_1U7Ui7JZF520sfDc2eKNoWxa` | `sss_monthly_dashboard_28` | Not public |
| SSS-P04 | Reels Made Simple | 34 | `price_1U7UiEJZF520sfDc3lar7SfY` | `sss_reels_made_simple_34` | Not public |
| SSS-P06 | Local Business Launch Pack | 42 | `price_1U7UiKJZF520sfDcNHbBaidr` | `sss_local_business_launch_pack_42` | Not public |
| SSS-C01 | 30 Days of Content in 60 Minutes | 69 | `price_1U7UiYJZF520sfDcdOkOSVyk` | `sss_mini_course_69` | Course access pending |
| SSS-B01 | Show Up Simply™ Toolkit | 149 | `price_1U7UiQJZF520sfDcC8gbZQ18` | `sss_toolkit_149` | Bundle QA pending |
| SSS-C02 | Show Up Simply™ Content System | 349 | `price_1U7UifJZF520sfDc73Iwh8Vz` | `sss_flagship_349` | Course access pending |

## SSS-P01 QA state
- final 24-page + 11-page PDF package complete;
- final ZIP uploaded to Payhip;
- Payhip/Stripe connection completed;
- mobile zero-dollar checkout/download test succeeded;
- website Buy button points to Payhip.

## Safety rule
Do not publish checkout for another SKU simply because a Stripe price exists. A public checkout only opens after the matching customer package/course access is accurate, protected and tested.

## Security
GitHub Pages never receives raw payment-card information. Do not commit payment secrets, banking data, customer order data or private identity information to the public repository.
