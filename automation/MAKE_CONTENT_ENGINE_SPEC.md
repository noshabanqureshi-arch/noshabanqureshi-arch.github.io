# Square Social Studio — Make Content Engine Specification

Purpose: convert an approved Square Social content job into a production-ready creative package with as little owner handling as possible.

This is an implementation specification. It does not contain API keys, customer data or private credentials.

## Source files

Business truth:
`https://noshabanqureshi-arch.github.io/automation/public-business-manifest.json`

Content job schema:
`https://noshabanqureshi-arch.github.io/automation/content-job-schema.json`

Current Reel jobs:
`https://noshabanqureshi-arch.github.io/automation/first-1000-reel-jobs.json`

## Runtime principle

The public GitHub files are the non-sensitive source of truth.

Do not use the public repository as a customer database or credential store.

Use Make's own Data Store, a private approved database, or another private operational store for mutable runtime state such as:
- current processing status;
- private provider IDs;
- generated asset IDs;
- approval timestamps;
- support/customer records;
- API tokens.

## Scenario 1 — Reel production

### Trigger
Start with one of these low-complexity options:
1. Manual run with `post_id`, or
2. Scheduled run that selects the next `queued` Reel job from the private runtime queue.

Do not automatically process all five at once until one complete job has passed QA.

### Step A — Load source of truth
HTTP GET:
- public business manifest;
- current Reel job list.

Select the requested `post_id`.

Reject the job if:
- campaign does not match `first-1000`;
- destination is not an approved Square Social URL;
- live product price conflicts with the manifest;
- the job is already published;
- required fields are missing.

### Step B — Generate the creative package with Claude
Claude receives:
- business manifest;
- one content job only;
- the production prompt in `CLAUDE_CONTENT_PRODUCTION_HANDOFF.md`;
- any approved source article text needed for factual grounding.

Require structured output:

```json
{
  "post_id": "P01",
  "final_hook": "...",
  "voiceover_script": "...",
  "on_screen_text": ["..."],
  "b_roll_plan": ["..."],
  "caption": "...",
  "cta": "...",
  "destination": "...",
  "utm_content": "...",
  "estimated_seconds": 25,
  "claims_check": {
    "invented_statistics": false,
    "invented_testimonial": false,
    "invented_results": false,
    "price_matches_manifest": true,
    "planned_offer_presented_as_live": false
  }
}
```

If any claims-check field fails, stop the workflow and mark `needs_revision`.

### Step C — Generate tracked URL
Create:

`destination + ?utm_source=instagram&utm_medium=organic-social&utm_campaign=first-1000&utm_content=<utm_content>`

If the destination already contains a query string, append with `&` instead of `?`.

Store the final tracked URL with the asset record.

### Step D — Voiceover
If ElevenLabs text-to-speech is available in the connected Make/Claude workflow:
- send only the final approved script text;
- use the designated Square Social voice;
- save the output using the job's `voiceover_filename`;
- store the private provider asset/file ID in the runtime store.

If ElevenLabs TTS is not available:
- do not block the whole content job;
- create a `VOICEOVER_READY_FOR_MANUAL_TTS` task containing the exact final script and filename.

Never store the ElevenLabs API key in GitHub.

### Step E — Canva production
Preferred implementation:
- create a new design or copy from an approved Square Social Reel template;
- never overwrite the approved campaign static posts;
- title it with `canva_name` from the content job;
- insert approved hook/on-screen text;
- add captions;
- add the voiceover if available;
- use simple reusable B-roll or screen footage;
- preserve navy / warm white / gold / sage visual system.

If direct Make → Canva generation is limited, use Claude + Canva as the production action and let Make remain the state/routing layer.

### Step F — Automated QA
Before approval, verify:
- correct Post ID;
- correct campaign ID;
- correct product price if mentioned;
- approved destination;
- correct UTM campaign/source/content;
- no retired `$850`, `DM SYSTEM`, `Seven-Day Sprint`, or Kitchener-Waterloo positioning;
- no invented proof/testimonials/statistics;
- no planned product described as live;
- captions/on-screen text are readable;
- one primary CTA only;
- Canva design is a copy/new design, not the master/static source overwritten.

Any failure → `needs_revision`.

### Step G — One human approval
Create one approval packet containing:
- Post ID;
- Canva preview/design link;
- final voiceover script;
- final caption;
- final CTA;
- tracked destination;
- duration;
- QA status.

Owner choices:
- APPROVE;
- REVISE;
- HOLD.

No second approval should be required unless a revision materially changes claims, pricing, CTA, destination or offer scope.

### Step H — After approval
If a supported scheduler is connected:
- schedule the asset for the assigned campaign date;
- store scheduled timestamp and scheduler ID.

If no supported scheduler is connected:
- put the asset into `READY_TO_POST`;
- send the owner one compact package containing the final asset/design link, caption and tracked destination.

Do not invent a scheduler integration.

### Step I — Publication logging
Once published, record:
- Post ID;
- publication date/time;
- platform;
- published URL if available;
- tracked destination;
- final creative version;
- owner time spent if tracked.

Status → `published`.

---

## Scenario 2 — Weekly metrics later

Trigger: once weekly after the first campaign begins.

Inputs where available:
- post-level reach/views;
- saves;
- shares;
- profile visits;
- link clicks;
- Payhip Starter orders;
- gross revenue;
- refunds;
- support/access issues;
- owner hours.

Claude output:
- KEEP;
- STOP;
- TEST exactly one meaningful variable;
- SCALE;
- anomalies;
- next three priorities.

Do not call a high-reach post a business success unless qualified traffic or commercial evidence supports it.

---

## Scenario 3 — Purchase/customer-success later

Do not activate until provider hooks are verified.

Purchase event →
- protected provider delivers product;
- tag purchase privately;
- send quick-start/support instructions;
- suppress acquisition messages for the same owned product where technically possible;
- request private feedback after a reasonable use period;
- never publish feedback without separate permission.

---

## Error handling

Every scenario should fail safely.

If Claude, Canva, ElevenLabs or another provider fails:
- preserve the job;
- mark the exact failed stage;
- retry only the failed stage where safe;
- do not create duplicate published content;
- do not silently substitute another price/offer/CTA;
- alert the owner only when the failure cannot be automatically retried or resolved.

## Cost/time guardrail

The automation is successful only if it reduces owner attention.

Target for normal content production after stabilization:
- one batch approval session per week;
- no repeated manual copying among Claude, ElevenLabs and Canva;
- no daily analytics checking;
- no manual recreation of UTM links;
- no rebuilding content from blank prompts.

If maintenance starts taking more time than manual production, simplify the automation.