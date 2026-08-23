# Square Social Studio — Stripe Catalogue

Live Stripe account: Square Social Studio
Currency: CAD
Payment model: one-time purchases only at launch
Checkout architecture: hosted Stripe Payment Links; GitHub Pages never handles card data.

## Live catalogue

| SKU | Offer | CAD | Stripe Price ID | Lookup Key | Launch state |
|---|---|---:|---|---|---|
| SSS-P02 | Brand Voice Clarity Workbook | 18 | `price_1U7UhkJZF520sfDczSz25jVW` | `sss_brand_voice_clarity_18` | Package ready; checkout not published |
| SSS-P03 | Caption Vault: 120 Prompts | 22 | `price_1U7UhtJZF520sfDc6SAa4D0o` | `sss_caption_vault_22` | Package ready; checkout not published |
| SSS-P01 | 30-Day Content Starter | 27 | `price_1U7Ui2JZF520sfDcEy2h8GtW` | `sss_30_day_starter_27` | Final branded export pending |
| SSS-P05 | Monthly Content Dashboard | 28 | `price_1U7Ui7JZF520sfDc2eKNoWxa` | `sss_monthly_dashboard_28` | PDF package ready; customer Notion duplicate link pending |
| SSS-P04 | Reels Made Simple | 34 | `price_1U7UiEJZF520sfDc3lar7SfY` | `sss_reels_made_simple_34` | Package ready; checkout not published |
| SSS-P06 | Local Business Launch Pack | 42 | `price_1U7UiKJZF520sfDcNHbBaidr` | `sss_local_business_launch_pack_42` | Package ready; checkout not published |
| SSS-C01 | 30 Days of Content in 60 Minutes | 69 | `price_1U7UiYJZF520sfDcdOkOSVyk` | `sss_mini_course_69` | Course media pending; do not publish checkout |
| SSS-B01 | Show Up Simply™ Toolkit | 149 | `price_1U7UiQJZF520sfDcC8gbZQ18` | `sss_toolkit_149` | Pre-launch bundle; final Starter file pending |
| SSS-C02 | Show Up Simply™ Content System | 349 | `price_1U7UifJZF520sfDc73Iwh8Vz` | `sss_flagship_349` | Course media pending; do not publish checkout |

## Safety rule

Do not create or publish website purchase buttons until the corresponding protected delivery path has been tested. Creating a Stripe product/price does not make the website publicly purchasable by itself.

## Next payment step

Create hosted Payment Links only for launch-ready downloadable products after:
1. final customer ZIP exists;
2. support email exists;
3. public terms/privacy/refund information is finalized;
4. delivery automation is connected;
5. end-to-end test succeeds.
