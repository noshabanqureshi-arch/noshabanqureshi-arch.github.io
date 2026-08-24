# Square Social Studio — Make Setup Checklist

Purpose: build the first production automation with the smallest possible setup and one owner approval.

Current Make capability check: Make has current integrations for Anthropic Claude, Canva and ElevenLabs. Use native modules where available and keep credentials only inside provider/Make connections.

## Before building the scenario

Create/connect inside Make:
- Anthropic Claude connection;
- Canva connection;
- ElevenLabs connection;
- HTTP module access for reading the public Square Social manifest/job JSON;
- Make Data Store for private mutable workflow state.

Do not put API keys or private IDs into GitHub.

## Create Make Data Store: `sss_content_runtime`

Recommended fields:
- `post_id` — text, unique key;
- `campaign_id` — text;
- `status` — text;
- `creative_json` — long text/JSON;
- `voiceover_asset_id` — text;
- `canva_design_id` — text;
- `canva_design_url` — text;
- `approval_status` — text;
- `approved_at` — date/time;
- `scheduled_at` — date/time;
- `published_url` — text;
- `last_error_stage` — text;
- `last_error_message` — long text;
- `updated_at` — date/time.

Keep customer/client information out of this store for the first campaign.

## Scenario: `SSS — Reel Production v1`

Build only P01 first. After P01 passes end-to-end QA, reuse the same scenario for P06, P10, P12 and P16.

### Module 1 — Manual trigger or custom webhook
Input:
- `post_id` such as `P01`.

For the first test, manual execution is safer than an unattended schedule.

### Module 2 — HTTP: Get business manifest
GET:
`https://noshabanqureshi-arch.github.io/automation/public-business-manifest.json`

### Module 3 — HTTP: Get Reel job list
GET:
`https://noshabanqureshi-arch.github.io/automation/first-1000-reel-jobs.json`

### Module 4 — Select requested job
Find the job matching `post_id`.

Stop if no job matches.

### Module 5 — Guardrail check
Before Claude, verify:
- campaign = `first-1000`;
- channel = `instagram`;
- approval_required = true;
- destination begins with the approved Square Social domain;
- if the job names the Starter, price = CAD $27;
- job is not already marked published in the runtime store.

### Module 6 — Anthropic Claude: Create a Prompt
Send:
- business manifest;
- selected job;
- the rules from `CLAUDE_REEL_RUNNER_PROMPT.md`.

Require JSON-only creative output matching the shape described in `MAKE_CONTENT_ENGINE_SPEC.md`.

Recommended model behavior:
- concise;
- no web research unless specifically required;
- no invented claims;
- one CTA;
- script stays inside target duration.

### Module 7 — Parse Claude JSON
Reject the output if:
- it is not valid JSON;
- any QA claim-check field fails;
- CTA/destination changed without permission;
- product price/status conflicts with manifest.

If rejected:
- write `needs_revision` to Data Store;
- stop before ElevenLabs/Canva so failed drafts do not consume production credits.

### Module 8 — Build tracked URL
Append:
- `utm_source=instagram`
- `utm_medium=organic-social`
- `utm_campaign=first-1000`
- `utm_content=<job utm_content>`

### Module 9 — ElevenLabs: Create a speech synthesis
Input:
- final Claude `voiceover_script`;
- selected approved Square Social voice.

Output filename:
use the job's `voiceover_filename`.

Store provider/file ID privately in Make Data Store.

### Module 10 — Canva
Preferred setup: create one reusable Square Social **Brand Template** for Reels with autofill fields such as:
- `HOOK`;
- `BODY_1`;
- `BODY_2`;
- `CTA`;
- optional `POST_ID`.

Then use Canva's **Autofill a Design from a Brand Template** action where available.

Design title:
use `canva_name` from the job.

If the current Canva plan/template setup does not support autofill:
- use Canva Create Design as a partial automation;
- or temporarily keep the Canva assembly step inside the existing Claude + Canva workflow;
- do not block the rest of the automation.

### Module 11 — Optional Canva export
After the design is approved/final, Canva's Make integration can export a design to the chosen format.

Do not auto-export/publish before owner approval in v1.

### Module 12 — Save approval packet
Write to Make Data Store:
- creative JSON;
- voiceover reference;
- Canva design link/ID;
- tracked URL;
- status = `ready_for_approval`.

### Module 13 — Owner approval
V1 can be simple:
- send one email/message containing Canva link + caption + voiceover script + tracked URL;
- owner replies/acts with APPROVE / REVISE / HOLD;
- or use a small Make approval webhook/form later.

Do not build a complex approval app before the first five Reels prove the workflow.

### Module 14 — After approval
Set:
- `approval_status=approved`;
- `approved_at=timestamp`;
- status = `ready_to_post`.

Until a reliable social scheduler is connected, manual Instagram publishing is acceptable.

## P01 success criteria

The first scenario is successful only if one P01 run produces:
- correct final script;
- correct CTA;
- correct free-ideas destination;
- correct tracked URL;
- ElevenLabs voiceover;
- Canva Reel draft/design;
- one approval packet;
- no retired offer language;
- no manual copy/paste between Claude and ElevenLabs;
- no price or product-status drift.

## Then clone/reuse for remaining Reel jobs

After P01 passes:
- P06;
- P10;
- P12;
- P16.

Do not create five different scenarios. One scenario should accept different Post IDs.

## Phase-1 definition of done

Square Social can produce a Reel by entering a Post ID and then reviewing one final approval packet.

That is enough automation for the first production milestone.