# Square Social Studio — Claude Content Production Handoff

Purpose: use Claude + Canva + ElevenLabs as the production layer while keeping the Square Social Studio website, funnel, offer status, links and measurement system synchronized with the current GitHub Pages business system.

## Division of work

### Claude production workspace
Use Claude for:
- adapting approved campaign copy into Reel scripts, carousels, captions and production directions;
- creating/editing Canva assets through the connected Canva AI connector;
- generating or coordinating voiceover audio through ElevenLabs only when the connected ElevenLabs tool actually exposes creative/TTS actions;
- batching multiple assets from one approved source idea;
- preserving Square Social voice and visual rules.

### Website / funnel control layer
The GitHub Pages system remains the source of truth for:
- live offer status and pricing;
- public product/resource pages;
- campaign landing pages;
- tracked destinations and UTMs;
- private launch dashboard and publishing calendar;
- privacy/terms/support language;
- SEO/internal links;
- measurement and campaign decisions.

Do not let Claude invent a new price, offer, product inclusion, URL, testimonial, deadline, discount or customer result.

## Current brand contract
Brand: Square Social Studio
Promise: Show Up Simply™
Positioning: Turn what you already know into useful content—without making social media your full-time job.

Voice:
- calm;
- helpful;
- practical;
- credible;
- human;
- clear over clever;
- useful over noisy.

Visual system:
- dark navy #0B1F3A;
- warm white #F8F6F0;
- soft gold #D9B66D;
- muted sage #8FAE9E;
- Georgia-style serif display treatment + clean sans-serif body treatment;
- simple diagrams, checklists and process visuals;
- avoid stock-photo-heavy agency imagery and fake client dashboards.

## Current commercial truth
Only live paid self-serve checkout:
- 30-Day Content Starter — CAD $27 — Payhip.

Do not describe as live:
- Show Up Simply™: Plan Your Content Month — planned $69;
- Show Up Simply™ Toolkit — planned $149;
- Show Up Simply™ Content System — planned $349;
- Square Social Vault — planned $99/month;
- other low-ticket product previews.

Done-for-You:
- from CAD $3,000/month;
- maximum 3 active clients;
- prequalification exists;
- secure application submission is not open yet.

## First $1K campaign
Campaign ID: first-1000
Schedule: August 24–September 27, 2026
Cadence: 4 primary Instagram posts/week for 5 weeks
Primary channel: Instagram
TikTok/Pinterest: reuse only when easy; do not create a second full calendar.

All 20 approved static campaign visuals already exist in Canva across four packs.

Operator pages:
- /launch-command-center/
- /launch-dashboard/
- /publishing-calendar/
- /reel-production/
- /instagram-launch/

## Current tracked destination rules
Instagram bio shortcut:
https://noshabanqureshi-arch.github.io/ig/

Education / free-idea destination:
https://noshabanqureshi-arch.github.io/resources/30-social-media-content-ideas-small-business/

Starter purchase-intent destination:
https://noshabanqureshi-arch.github.io/lp/30-day-content-starter/

Normal product-research destination:
https://noshabanqureshi-arch.github.io/products/30-day-content-starter/

Resources hub:
https://noshabanqureshi-arch.github.io/resources/

Do not send every post directly to checkout.

## Reel production rule
Current Reel slots: Posts 1, 6, 10, 12 and 16.

Preferred structure:
1. Hook
2. Useful value
3. Real example / process detail
4. One action

Production options:
- voiceover + simple B-roll;
- screen recording;
- text-led video;
- talking-head answer;
- carousel-to-video.

Video should still make sense with sound off:
- readable captions;
- strong contrast;
- no important text hidden under platform UI;
- accurate spelling;
- no invented facts/results.

If fresh video is not ready by the planned posting date, publish the approved static Canva cover with the approved caption. Do not delay the campaign.

## ElevenLabs rule
If the Claude-connected ElevenLabs tool exposes creative TTS/audio generation, use it for the approved Reel script and the existing Square Social voice where available.

If the connected tool only exposes ElevenAgents/agent-management actions, do not try to force it to generate marketing voiceover. Use the ElevenLabs web app or an ElevenLabs MCP/tool that explicitly supports text-to-speech.

Voiceover output convention:
SSS-FIRST1000-P<POSTNUMBER>-VO-v1.mp3

Keep the script under the matching post ID and do not alter factual product claims.

## Canva naming convention
Static pack examples already exist.
For new Reel/video production designs use:
SSS-FIRST1000-P01-REEL
SSS-FIRST1000-P06-REEL
SSS-FIRST1000-P10-REEL
SSS-FIRST1000-P12-REEL
SSS-FIRST1000-P16-REEL

Do not overwrite the approved static campaign packs. Create copies/new Reel production designs.

## Website synchronization rule
Claude does not need to edit the website to create campaign assets.
The website and social assets are linked by:
1. the same campaign/post IDs;
2. the approved destination URLs above;
3. the first-1000 UTM convention;
4. the same offer truth/brand contract.

When Claude creates a new asset or changes a campaign message, bring back only these fields for website/control-layer synchronization:
- Post ID;
- asset/design title;
- Canva design link;
- final caption;
- final voiceover script;
- final format/duration;
- destination URL;
- any new customer question or objection discovered.

Do not send credentials, API keys, customer data, payment details or private source files through public website URLs.

## UTM convention
Campaign: first-1000
Medium: organic-social
Source: instagram (or tiktok / pinterest when reused)
Content: use the approved post/content slug from the launch dashboard.

Example pattern:
?utm_source=instagram&utm_medium=organic-social&utm_campaign=first-1000&utm_content=<slug>

## Production QA checklist
Before calling an asset complete:
- correct Square Social colors/voice;
- matches approved post idea;
- one primary job (Teach / Trust / Connect / Offer / Convert);
- one primary CTA;
- correct live price: CAD $27 when Starter is mentioned;
- no fake urgency;
- no fake testimonial/result;
- no retired $850 Sprint / DM SYSTEM / Kitchener-Waterloo language;
- no retired mini-course title “30 Days of Content in 60 Minutes”;
- correct destination URL;
- caption readable and not overlong for the format;
- video captions checked for sound-off viewing;
- final design/audio clearly named.

## Exact production brief to give Claude
Use the current campaign and brand contract above as fixed constraints. Do not redesign the offer or funnel. Produce only the requested campaign asset. Reuse existing Square Social Canva styles. For Reels, create a simple low-production video that can be repeated by a busy small-business owner: voiceover/B-roll, screen recording, text-led video or simple talking head. Preserve the approved factual claims and CTA. If ElevenLabs creative TTS is available, generate the voiceover from the final approved script; if it is not available, return the script ready to paste into ElevenLabs. Return the Canva design link, final script/caption, duration, destination and Post ID so the website/control system can stay synchronized.

## Current strategic rule
Production is not the bottleneck after the 20-post campaign is complete.
The operating loop is:
Publish → verify → respond → record → review → improve one variable → repeat.

Do not create more campaign volume merely because the tools make it easy.