# Square Social Studio — AI-Lean Automation Blueprint

Purpose: reduce recurring owner hours by making Square Social Studio an approval-driven system rather than a manually operated social-media business.

## Core operating rule
AI and automations do the preparation, production, routing, logging and first-pass analysis. The owner keeps final control over claims, pricing, publishing, customer-sensitive work, refunds, client commitments and major strategy changes.

## Architecture

### 1. One source of truth
Use a single non-sensitive business manifest for:
- brand promise and voice;
- current live offers/prices;
- planned-but-not-live offers;
- approved URLs;
- CTA rules;
- campaign IDs and UTM conventions;
- visual brand tokens;
- legal/claim guardrails.

Do not let Claude, Canva, ElevenLabs, email or automation tools invent commercial facts independently.

### 2. Automation layer
Recommended first no-code orchestrator: Make.

Role:
- connect source data to Claude;
- send approved scripts to ElevenLabs;
- populate Canva brand templates;
- write output/status records;
- move approved assets into a publish queue;
- trigger customer-success/admin workflows;
- collect weekly metrics into one scorecard.

Alternative later: n8n for more technical/self-hosted/custom workflows.

## Human-approval levels

### Fully automatic
- generate draft captions from approved source material;
- transform one approved idea into multiple formats;
- generate UTM links;
- create file names and folders;
- create first-pass voiceover audio;
- populate approved Canva templates;
- log published content/metrics;
- send transactional onboarding/instructions after purchase when provider permissions allow;
- summarize support questions;
- prepare weekly KPI summaries;
- surface anomalies or broken links for review.

### One-click approval
- public social posts;
- newsletters/marketing broadcasts;
- new landing-page copy;
- changes to offer messaging;
- client-facing content;
- testimonial/case-study publication;
- campaign-scale changes.

### Always human
- price changes;
- new offers;
- refunds/disputes;
- promises/guarantees;
- legal/privacy decisions;
- client acceptance;
- sensitive customer data;
- final regulated/high-risk claims;
- hiring/vendor commitments.

## Automation 1 — Content engine

Trigger: approved campaign row or approved idea.

Flow:
1. Read business manifest + post ID + source material.
2. Claude generates platform-specific caption/script while preserving factual constraints.
3. If video: send final script to ElevenLabs for TTS.
4. Populate approved Canva template/design.
5. Create asset record with Post ID, campaign, CTA, destination and UTM slug.
6. Put item into `READY FOR APPROVAL` queue.
7. Owner reviews once.
8. After approval, publish/schedule through an available supported scheduler; otherwise present final asset and caption for manual posting.
9. Mark as published and record URL/date.

Target: owner should review content, not assemble it.

## Automation 2 — Repurposing engine

Trigger: a post/article performs well or is manually marked `REUSE`.

Claude creates:
- Reel script;
- carousel outline;
- Story/FAQ version;
- email version;
- Pinterest/title variation when appropriate.

Rule: reuse the same verified source idea rather than inventing unrelated content.

## Automation 3 — Customer purchase + success

Trigger: Payhip/checkout purchase event when supported.

Flow:
1. Delivery remains handled by the protected commerce platform.
2. Apply product/customer tag in the customer system.
3. Send quick-start/support information.
4. Suppress future acquisition messages for the product already owned when integrations allow.
5. After a reasonable usage period, ask for private feedback.
6. Never publish a testimonial without separate permission.

## Automation 4 — Free resource funnel

Trigger: free-resource request after $0 Payhip product is live.

Flow:
- deliver resource transactionally;
- do not auto-enrol in unrelated marketing;
- if explicit marketing consent exists, tag source and enter welcome sequence;
- route future emails to the live Starter only when relevant.

## Automation 5 — Support triage

Trigger: support email.

AI can:
- classify order/download/general inquiry;
- draft a reply from approved FAQ/support rules;
- surface missing order information;
- flag refund/payment/privacy issues for owner handling.

Owner should only touch exceptions.

## Automation 6 — Weekly CEO report

Run once weekly.

Input:
- posts published;
- reach/views where available;
- saves/shares/profile visits/link clicks;
- Payhip orders;
- gross revenue;
- refunds/support issues;
- owner hours.

Output:
- KEEP;
- STOP;
- TEST one variable;
- SCALE;
- anomalies;
- next three priorities.

No daily analytics checking.

## Automation 7 — Client delivery later

Only after secure client intake is active.

For each client keep a private client source-of-truth separate from the public Square Social manifest.

Suggested monthly flow:
1. ingest approved client source material;
2. extract real FAQs/offers/examples;
3. draft monthly strategy/content plan;
4. create assets from approved templates;
5. client approval queue;
6. publish/schedule;
7. monthly report generated automatically;
8. owner reviews exceptions and strategic changes.

Never mix one client's data with another client's workspace.

## Recommended owner workload

### Digital-product/content business without clients
Design target: roughly 3–6 recurring owner hours/week after workflows are stable.

Owner time goes to:
- one approval batch;
- one weekly KPI review;
- important support exceptions;
- product/strategy decisions.

This is a design target, not a guarantee; actual time depends on provider reliability and customer volume.

### With premium clients
Client work should replace general production blocks rather than be added on top. Maintain the existing maximum of three clients and automate preparation/reporting heavily.

## Build order

### Phase 1 — now
1. Establish machine-readable business manifest.
2. Use Make as orchestration layer.
3. Automate Claude → Canva draft generation.
4. Automate Claude → ElevenLabs voice generation for Reel posts.
5. Create a single approval queue.
6. Keep publishing approval human while the system learns.

### Phase 2 — after the first campaign produces data
7. Automate weekly KPI summary.
8. Activate $0 Payhip freebie workflow.
9. Connect compliant email marketing.
10. Add support triage.

### Phase 3 — after repeatable demand
11. Build customer-facing Square Social AI assistant using the same approved knowledge/manifest.
12. Add secure client workspaces and client delivery workflows.
13. Consider n8n/custom MCP architecture only when Make becomes a real constraint.

## Anti-overengineering rule
Do not build an autonomous AI company before there is real demand.

Automate a repeated task only when:
- it happens often;
- the input/output can be standardized;
- errors can be detected;
- human approval can be placed at the right risk point;
- automation saves more owner time than it creates in maintenance.

The goal is not maximum automation. The goal is minimum necessary owner attention.