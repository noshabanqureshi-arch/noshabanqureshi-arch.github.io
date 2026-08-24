# Square Social Studio — Weekly CEO Report Automation

Purpose: replace daily dashboard checking with one short weekly decision report.

## Trigger
Run once weekly after the final scheduled post for the week has had enough time to collect an initial signal.

Default review window for the current campaign:
- weekly, not daily;
- exact run day/time can be chosen during Make setup.

## Inputs
Use only verified data available from connected providers.

### Content activity
- number of posts scheduled;
- number successfully published;
- failed/blocked posts;
- Post IDs and formats.

### Instagram diagnostics
Where the connected API returns them:
- reach/views;
- saves;
- shares;
- comments;
- other post insights.

### Website/funnel
Only after analytics is connected:
- sessions by source/content;
- landing-page visits;
- tracked link activity;
- Starter CTA clicks where implemented.

Before analytics exists, do not invent these numbers.

### Commerce
Source of truth for the live Starter:
- Payhip paid orders;
- gross Starter revenue;
- refunds;
- delivery/access issues.

### Owner effort
- estimated owner minutes/hours spent on campaign approval, posting exceptions and support.

## Derived calculations
Calculate only from real inputs:
- posts published / planned;
- gross revenue for the week;
- cumulative campaign revenue;
- sales count;
- average revenue per paid order when meaningful;
- qualified clicks per post when click data exists;
- orders per landing-page session only after session data exists;
- owner hours per week.

Do not calculate conversion rates with missing denominators.

## Claude analysis prompt

You are reviewing Square Social Studio's `first-1000` campaign.

Use the business manifest and the supplied verified weekly metrics.

Return:

### WEEK IN ONE LINE
One sentence explaining what actually happened.

### REVENUE
- paid Starter orders;
- gross revenue;
- cumulative progress toward the working test target;
- refunds/access issues.

### WHAT GOT USEFUL ATTENTION
Identify up to three posts/messages with the strongest relevant signal.
Distinguish high reach from high purchase/click intent.

### KEEP
One to three things worth continuing.

### STOP
One or two things that consumed effort without enough evidence of value.

### TEST
Choose exactly ONE meaningful variable for the next week.
Examples:
- hook;
- CTA wording;
- destination page;
- format;
- message angle.

Do not recommend changing price, offer, audience, landing page and format all at once.

### SCALE
Name anything with enough evidence to reuse across another format/channel.
If there is not enough evidence, say so.

### CUSTOMER SIGNALS
Summarize repeated questions, objections or support problems.
Do not expose customer-identifying information.

### OWNER TIME
State owner hours and whether the campaign is becoming too labor-intensive.

### NEXT THREE PRIORITIES
Maximum three.

## Decision rules

### High reach + weak clicks
Improve CTA/message-to-destination fit before increasing content volume.

### Strong clicks + weak sales
Inspect landing-page/product-fit friction before creating more top-of-funnel content.

### Sales associated with a message/theme
Reuse the underlying message with a new format or angle.

### No meaningful signal
After enough posts/time, change one variable only.
Do not react to a single low-performing post.

### Owner time exceeds target
Simplify production/publishing before adding volume.

## Delivery
Send one compact weekly report to the owner.

Preferred end state:
- owner does not need to open Instagram analytics daily;
- owner does not manually add up Payhip revenue;
- owner does not build a report from scratch;
- owner reads one decision-oriented summary and makes one or two choices.

## Guardrail
AI may summarize and recommend.
AI may not autonomously change:
- pricing;
- live offer scope;
- refund policy;
- campaign budget;
- client capacity;
- legal/privacy policy.

Those remain owner decisions.