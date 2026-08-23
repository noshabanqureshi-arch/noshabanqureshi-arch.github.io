# Square Social Studio — Funnel Analytics Event Map

Use this event naming consistently when analytics is connected.

## Core events
- `view_freebie_page`
- `freebie_opt_in`
- `freebie_download`
- `view_starter_page`
- `starter_checkout_click`
- `starter_checkout_start`
- `starter_purchase`
- `starter_delivery_access`
- `support_request`

## Purchase properties
Attach when supported:
- `sku`: SSS-P01
- `product_name`: 30-Day Content Starter
- `currency`: CAD
- `value`: 27
- `traffic_source`
- `campaign`
- `content_id`

## Primary formulas
- Freebie opt-in rate = freebie opt-ins / freebie page sessions
- Product purchase rate = Starter purchases / Starter page sessions
- Checkout completion rate = purchases / checkout starts
- Revenue per product-page session = gross Starter revenue / Starter page sessions
- Lead-to-buyer rate = buyers who previously opted in / qualified leads

## First $1,000 dashboard
Show these five numbers first:
1. Qualified Starter page sessions
2. Purchases
3. Product page purchase rate
4. Gross revenue
5. Revenue per session

Secondary diagnostics:
- freebie opt-ins
- checkout starts
- checkout abandonment
- top traffic source
- top converting content
- refund/access issues

## UTM convention
Use lowercase and hyphens.

Example:
`utm_source=instagram&utm_medium=organic-social&utm_campaign=first-1000&utm_content=content-pillars-reel`

Suggested sources:
- instagram
- tiktok
- linkedin
- pinterest
- email
- direct
- referral

Suggested campaign:
- `first-1000`

Each post should receive a short descriptive `utm_content` value so content can be evaluated by business outcome rather than likes alone.
