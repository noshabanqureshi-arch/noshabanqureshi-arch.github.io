# Square Social Studio — Make Instagram Publishing + Insights Spec

Purpose: remove repetitive manual Instagram publishing and first-pass metric collection while keeping owner approval before anything goes public.

## Provider requirement

Use Make's Instagram for Business connection only after the Square Social Instagram account is configured as a supported Business/Creator account and linked through the required Facebook/Meta connection.

Do not change account type or Meta settings blindly; verify the account configuration during setup.

## Publishing rule

No generated creative goes directly from Claude/Canva to Instagram.

Required state:
`ready_for_approval` → owner APPROVES → `approved` → Make may publish/schedule.

## Scenario: `SSS — Approved Instagram Publisher v1`

### Trigger
Runtime record changes to:
`approval_status=approved`

and contains:
- post_id;
- campaign_id;
- final caption;
- approved media file/export;
- target publication date/time;
- tracked destination/CTA record.

### Router by format

#### Reel
Use Instagram for Business action:
- Create a Reel post.

#### Static image
Use:
- Create a photo post.

#### Carousel
Use:
- Create a carousel post.

If a format is unsupported or required media is missing, stop and mark `blocked` rather than substituting another format.

## Scheduling

For v1, the Make scenario itself can run at the assigned publication time and then call the Instagram publishing action.

Use the dated Square Social campaign calendar as the source schedule.

Do not double-post to compensate for a missed run. If a scheduled run fails, keep the job blocked and surface the failure.

## Caption rule

Publish the exact owner-approved caption.

Do not regenerate caption copy at the publishing stage.

If Instagram rejects the caption because of a technical constraint, return the job to `needs_revision` rather than silently rewriting it.

## Link rule

Instagram feed/Reel captions may not make URLs directly clickable in every placement. The campaign's primary profile route remains:
`https://noshabanqureshi-arch.github.io/ig/`

Store the tracked destination with the post record for measurement and for any supported link placement.

## After publish

Store privately in Make Data Store:
- post_id;
- Instagram media/post ID;
- published timestamp;
- public post URL when returned/available;
- creative version;
- caption version;
- campaign ID.

Status → `published`.

## Metric collection

Use Instagram for Business post-insight/search modules where available.

Suggested collection windows:
- first snapshot: approximately 24 hours after publish;
- campaign review snapshot: approximately 7 days after publish.

Collect only metrics that the API actually returns for the content/account type.

Potential fields:
- reach/views;
- saves;
- shares;
- comments;
- profile/activity signals where available.

Do not fabricate unavailable metrics and do not compare incompatible metric definitions across formats without noting the difference.

## Weekly roll-up

Once per week, combine:
- posts published;
- verified Instagram insight fields;
- website/link data when analytics is active;
- Payhip paid orders and gross revenue;
- support/refund/access issues;
- owner hours.

Send the combined record to the weekly CEO-analysis workflow.

## Comment automation rule

Make can technically connect to Instagram comments/replies, but Square Social should NOT start with autonomous comment replies.

Phase 1:
- collect comments;
- classify useful customer questions;
- draft suggested replies;
- owner handles or approves replies where needed.

Only automate factual low-risk replies after real comment patterns exist.

Never automate:
- disputes;
- refunds;
- complaints;
- legal/privacy questions;
- personalized strategy consultations;
- sensitive customer situations.

## Success condition

After stabilization, the owner should be able to:
1. approve the weekly creative batch once;
2. have Make publish approved assets at the assigned times;
3. receive metrics without opening Instagram analytics for every post.

That is the target—not fully autonomous public communication.