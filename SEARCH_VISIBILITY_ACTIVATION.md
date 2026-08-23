# Square Social Studio — Search Visibility Activation

Purpose: move the public Square Social Studio site from technically crawlable to intentionally monitored in search without accidentally indexing private operator or campaign-control pages.

## Current verified site-side state
- public GitHub Pages site exists;
- `robots.txt` allows crawling;
- `sitemap.xml` exists and includes the current public evergreen/commercial pages;
- canonical URLs are present on the main pages;
- the live $27 Starter has Product/Offer structured data;
- the About page has Organization structured data;
- **ten evergreen educational resources** are published;
- the full 30 Social Media Content Ideas guide is indexable and immediately usable without an email gate;
- the focused Starter campaign landing page is intentionally `noindex,follow` and canonicalized to the normal product page;
- private operator pages such as Start Here, the launch dashboard, command center, publishing calendar and Reel board are intentionally `noindex` and excluded from the sitemap;
- planned offers are clearly labeled rather than pretending to be live;
- the main campaign/product/resource entry pages have Open Graph/social-share metadata using the existing `og.png` asset.

A previous external web search did not surface the GitHub Pages domain or live Starter by exact brand/product queries. That is not proof of an indexing defect; it means indexing should be checked deliberately rather than assumed.

## External activation steps
These require owner/provider access and cannot be completed from the static repository alone.

### 1. Google Search Console
Create/verify the current website property for:
`https://noshabanqureshi-arch.github.io/`

Use a verification method supported for GitHub Pages.

### 2. Submit the sitemap
Submit:
`https://noshabanqureshi-arch.github.io/sitemap.xml`

### 3. Inspect priority public URLs
Start with:
- homepage;
- `/resources/`;
- `/resources/30-social-media-content-ideas-small-business/`;
- `/resources/turn-customer-questions-into-content/`;
- `/resources/monthly-content-planning-workflow/`;
- `/resources/how-to-choose-content-pillars-small-business/`;
- `/resources/use-ai-social-media-without-sounding-generic/`;
- `/products/30-day-content-starter/`.

Request indexing only when useful; do not repeatedly submit indexing requests.

### 4. Do not request indexing for intentional noindex pages
Examples:
- `/start-here/`;
- `/launch-dashboard/`;
- `/launch-command-center/`;
- `/publishing-calendar/`;
- `/reel-production/`;
- focused campaign/thank-you/operator pages that intentionally use `noindex`.

These pages can remain usable through direct links while staying out of search results.

### 5. Validate structured data and share metadata
Use Google's Rich Results Test / Search Console enhancement reporting for:
- live Starter Product/Offer markup;
- Organization markup.

When practical, use a social-share/debugger tool to confirm that the campaign/product/resource URLs resolve the intended title, description and `og.png` share image.

Do not add ratings/reviews until genuine customer review data exists and the markup matches visible content.

### 6. Establish the baseline
Once data appears, record:
- indexed pages;
- impressions;
- clicks;
- queries;
- pages receiving impressions;
- crawl/indexing errors;
- structured-data warnings/errors.

Use these as a baseline, not as a reason to create content volume for its own sake.

## Current ten-resource cluster
1. 30 Social Media Content Ideas for Small Businesses
2. Turn Customer Questions Into Social Media Content
3. Five Jobs Your Small-Business Content Can Do
4. Turn One Customer Question Into Four Content Pieces
5. A Simple Monthly Content Planning Workflow
6. How to Choose Content Pillars for a Small Business
7. Do Small Businesses Need to Post Every Day?
8. Use AI for Social Media Without Sounding Generic
9. Short-Form Video Without the Performance
10. What Should a Small Business Actually Measure?

## Search content strategy
Do not create articles merely to increase page count.

Priority topic sources:
1. real small-business questions;
2. recurring customer questions from the First $1K campaign;
3. questions already covered in Square Social products/courses;
4. recurring objections;
5. content that demonstrates the Show Up Simply method;
6. topics where a useful free answer naturally leads to a real product or course.

Use internal links to reinforce a small number of useful topic clusters instead of producing overlapping articles that compete with one another.

## Custom-domain migration rule
When a final branded domain is acquired:
- do not simply publish both domains as independent copies;
- configure GitHub Pages/custom-domain settings correctly;
- update canonical URLs, Open Graph URLs, sitemap, Organization/Product markup and email links;
- verify the new property in Search Console;
- preserve redirects/canonical signals where the platform supports them;
- review every campaign/UTM link and provider callback URL;
- re-test Payhip links and Mailchimp sender/domain settings.

Do not acquire or migrate a domain without checking brand/name conflict, renewal cost, DNS control and the email setup that will use it.
