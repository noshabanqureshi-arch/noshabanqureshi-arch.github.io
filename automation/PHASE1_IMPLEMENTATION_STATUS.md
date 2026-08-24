# Square Social Studio — AI Automation Phase 1 Status

Status date: 2026-08-23

Purpose: separate architecture already completed from provider-account setup that still has to be activated.

## COMPLETED — architecture/source of truth

- `AI_LEAN_AUTOMATION_BLUEPRINT.md`
- `automation/public-business-manifest.json`
- `automation/content-job-schema.json`
- `automation/first-1000-reel-jobs.json`
- `automation/CLAUDE_REEL_RUNNER_PROMPT.md`
- `automation/MAKE_CONTENT_ENGINE_SPEC.md`
- `automation/MAKE_SETUP_CHECKLIST.md`
- `automation/MAKE_INSTAGRAM_PUBLISHING_SPEC.md`
- `automation/WEEKLY_CEO_REPORT_SPEC.md`
- `automation/PAYHIP_CUSTOMER_SUCCESS_AUTOMATION.md`
- `automation/SUPPORT_TRIAGE_AUTOMATION.md`
- `/automation-control/` private operator page

## COMPLETED — campaign inputs

- 20 campaign posts defined;
- 20 static Canva campaign visuals built;
- five Reel jobs identified: P01, P06, P10, P12, P16;
- approved live offer/price/destinations centralized;
- UTM convention defined;
- dated campaign calendar defined;
- Reel static fallback defined so launch does not wait for video;
- privacy/claim guardrails defined.

## REQUIRES PROVIDER LOGIN / CONNECTION

### Make
Needs owner/provider setup:
- create/sign in to Make account;
- connect Anthropic Claude;
- connect ElevenLabs;
- connect Canva;
- create `sss_content_runtime` Data Store;
- build one `SSS — Reel Production v1` scenario from the checklist.

### Canva
For best automation:
- create or select one reusable Square Social Reel Brand Template;
- expose simple autofill fields such as HOOK, BODY_1, BODY_2 and CTA where the Canva plan/template supports it;
- preserve the existing static/master designs.

If Brand Template autofill is unavailable, keep Canva assembly through the current Claude + Canva workflow while Make handles routing/state.

### ElevenLabs
- choose the approved Square Social voice;
- connect ElevenLabs in Make;
- keep API credential inside the provider/Make connection only.

### Instagram / Meta
To automate publishing/insights:
- verify `square.social.studio` ownership;
- configure it as a supported Business/Creator account if appropriate;
- link the required Facebook/Meta connection;
- connect Instagram for Business inside Make;
- test a non-critical draft/publish flow before unattended scheduling.

### Payhip
- create Make custom webhook endpoint;
- add endpoint under Payhip Settings → Developer;
- subscribe first to `paid` and `refunded`;
- verify webhook signature before processing;
- test with a controlled transaction/event before relying on it.

### Support inbox
- use the designated Square Social support inbox only;
- connect it to Make after privacy/triage rules are ready;
- start with AI drafting, not automatic sending.

## FIRST LIVE AUTOMATION TO BUILD

Build only:
`P01 → Claude → ElevenLabs → Canva → owner approval packet`

Do not automate all five Reels until P01 passes.

P01 definition of done:
- one Post ID starts the workflow;
- manifest/job data are loaded automatically;
- Claude returns valid structured creative;
- guardrails pass;
- ElevenLabs produces the named voice file;
- Canva creates a new Reel design/draft;
- tracked URL is generated;
- owner receives one approval packet;
- no retired offer language appears;
- no manual copy/paste is required between Claude and ElevenLabs.

## SECOND LIVE AUTOMATION

After P01 passes:
- add approval → Instagram publishing;
- collect post ID/URL;
- schedule first post insight snapshot;
- feed result into weekly CEO report.

## THIRD LIVE AUTOMATION

Payhip `paid` webhook → verified event → private purchase record → one transactional quick-start/support message.

## WHAT NOT TO BUILD YET

- autonomous price changes;
- autonomous refunds;
- autonomous comment handling;
- customer-facing Square Social AI assistant;
- complex multi-client agent system;
- custom app merely to replace Make;
- multiple automation platforms for the same workflow.

## Phase 1 success test

Phase 1 is successful when the owner can run the content side of Square Social with:
- one weekly approval batch;
- automated publishing where supported;
- one weekly CEO report;
- exception-only support handling;
- purchase customer-success automation;
- no repeated transfer of the same information among ChatGPT, Claude, ElevenLabs and Canva.

That is the point at which Square Social becomes meaningfully AI-lean rather than simply AI-assisted.