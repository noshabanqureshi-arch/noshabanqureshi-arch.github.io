# Square Social Studio — First $1,000 Campaign Routing

Purpose: keep the first revenue experiment focused on the live $27 30-Day Content Starter while routing education-first traffic to the full live 30-ideas guide rather than to an unfinished download flow.

## Campaign
`first-1000`

## Primary revenue goal
Test whether qualified small-business traffic can convert into purchases of the live **$27 CAD 30-Day Content Starter**.

This is an experiment, not a revenue guarantee.

---

# Destination hierarchy

## 1. Educational / free-intent campaign traffic
Primary destination:
`https://noshabanqureshi-arch.github.io/resources/30-social-media-content-ideas-small-business/`

Why:
- all 30 ideas are available immediately,
- no email address is required,
- the page is indexable,
- it contains a natural next step into monthly planning,
- it does not depend on the unfinished $0 Payhip setup.

The printable PDF status page remains:
`https://noshabanqureshi-arch.github.io/free/30-content-ideas/`

Use that page only when specifically discussing the printable/downloadable version until the $0 Payhip product is created and tested.

Broader education browsing:
`https://noshabanqureshi-arch.github.io/resources/`

## 2. Starter purchase-intent campaign traffic
Use the focused landing page:
`https://noshabanqureshi-arch.github.io/lp/30-day-content-starter/`

This page intentionally removes the full site navigation and keeps one primary action: buy the Starter through Payhip.

## 3. Normal product research / website browsing
Use the full product page:
`https://noshabanqureshi-arch.github.io/products/30-day-content-starter/`

## 4. General social-profile visitors
Use the short tracked entry points:
- Instagram: `https://noshabanqureshi-arch.github.io/ig/`
- TikTok: `https://noshabanqureshi-arch.github.io/tt/`
- Pinterest: `https://noshabanqureshi-arch.github.io/pin/`

Those shortcuts preserve the source and route into the shared `/go/` bio page.

## Why the routes differ
- 30 free ideas / Resources = **Discover / Learn**.
- Full product page = **Trust / product research**.
- Focused landing page = **Act / campaign conversion**.
- Social bio page = **self-selection / routing**.

Do not send every visitor to checkout simply for convenience.

---

# UTM pattern

Use lowercase parameters.

Campaign:
`utm_campaign=first-1000`

Organic social medium:
`utm_medium=organic-social`

Source:
`utm_source=<platform>`

Creative/message identifier:
`utm_content=<post-slug>`

The private `/launch-dashboard/` generates the current tracked destination URLs automatically. Prefer using that page rather than manually rebuilding UTM strings.

Example Instagram Starter link:
`https://noshabanqureshi-arch.github.io/lp/30-day-content-starter/?utm_source=instagram&utm_medium=organic-social&utm_campaign=first-1000&utm_content=monthly-workflow-process`

Example Instagram free-ideas link:
`https://noshabanqureshi-arch.github.io/resources/30-social-media-content-ideas-small-business/?utm_source=instagram&utm_medium=organic-social&utm_campaign=first-1000&utm_content=idea-problem-reel`

Email campaign links should not be used until the permission-based email system is activated.

---

# Current 20-post routing

## Free / education destination
1. Post 1 — problem may not be ideas — `idea-problem-reel`
2. Post 2 — five content jobs — `five-content-jobs-carousel`
3. Post 4 — not a full-time creator — `not-full-time-creator`
4. Post 6 — one question → four pieces — `one-question-four-posts`
5. Post 9 — clear over clever — `clear-over-clever`
6. Post 12 — AI without invented expertise — `ai-without-inventing`
7. Post 14 — calm system vs content sprint — `calm-system-vs-sprint`
8. Post 18 — Hook → Value → Example → Action — `hook-value-example-action`

All eight default to:
`/resources/30-social-media-content-ideas-small-business/`

A later campaign iteration may route an individual post to a more specific evergreen guide when analytics shows that doing so is worth testing. Do not change destinations mid-test without documenting the variable.

## Focused Starter landing page
3. Post 3 — monthly workflow/process — `monthly-workflow-process`
5. Post 5 — what is inside the Starter — `starter-inside-offer`
7. Post 7 — four content pillars — `four-content-pillars`
8. Post 8 — planning-session process — `planning-session-process`
10. Post 10 — plan next month Reel — `plan-next-month-reel`
11. Post 11 — do I need to post every day? — `not-post-every-day`
13. Post 13 — who the Starter is for — `starter-who-its-for`
15. Post 15 — actual PDF walkthrough — `starter-24-plus-11`
16. Post 16 — four questions before posting — `four-questions-before-posting`
17. Post 17 — blank → planned workflow — `blank-to-planned-workflow`
19. Post 19 — what $27 gets you — `starter-what-you-get`
20. Post 20 — direct plan-before-random-post — `plan-before-random-post`

All twelve default to:
`/lp/30-day-content-starter/`

---

# Reel fallback

Five campaign slots are planned as Reels: Posts 1, 6, 10, 12 and 16.

If fresh video is not ready:
- publish the approved Canva cover as a static text-led Instagram post,
- use the same approved caption,
- keep the same UTM content slug and destination,
- record the actual format used,
- test the video version later as a separate format variable.

Do **not** publish the retired $850-sprint R01–R06 audio/video merely to fill a Reel slot.

---

# Testing rule

Do not change several variables at once.

For the first useful sample:
- keep the live product and $27 price stable,
- keep campaign naming consistent,
- vary message/source/format through the planned posts,
- use the browser-local scorecard until site analytics exists,
- use Payhip order data as the source of truth for completed purchases.

## Interpretation
- reach but weak clicks → inspect hook/CTA/destination clarity,
- clicks but weak sales → inspect offer fit or landing-page friction,
- repeated useful question → prioritize it in later content,
- sales associated with a message → reuse the message in another format before creating a new offer.

---

# Paid-media gate

Do not buy traffic until:
- organic publishing has produced useful click/purchase evidence,
- site analytics/event tracking is active,
- the focused landing page and Payhip checkout are QA-tested,
- a daily/total test budget and stop rule are defined.

---

# Dropbox sync note

The older Dropbox `UTM-LINK-LIBRARY.md` and any older First-$1K funnel notes may still reference the normal product page or pre-five-week routing.

Do not silently edit the user's Dropbox from this GitHub runbook. When Dropbox file mutation is explicitly approved, synchronize those originals to:
- free campaign traffic → full 30-ideas web guide,
- purchase-intent traffic → focused Starter landing page,
- profile traffic → short `/ig/`, `/tt/`, `/pin/` routes,
- campaign duration → five weeks / 20 posts.
