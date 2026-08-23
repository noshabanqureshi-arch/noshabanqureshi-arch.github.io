# Square Social Studio — Search Visibility Activation

Purpose: move the public Square Social Studio site from technically crawlable to intentionally monitored in search.

## Current verified site-side state
- public GitHub Pages site exists;
- `robots.txt` allows crawling;
- `sitemap.xml` exists and includes the current public resources and commercial pages;
- canonical URLs are present on the main pages;
- the live $27 Starter has Product/Offer structured data;
- the About page has Organization structured data;
- six evergreen educational resources are published;
- the focused campaign landing page is intentionally `noindex,follow` and canonicalized to the normal product page;
- planned offers are clearly labeled rather than pretending to be live.

A current external web search did not surface the GitHub Pages domain or the live Starter by exact brand/product queries. This is not proof of an indexing defect, but it means indexing should be actively checked rather than assumed.

## External activation steps
These require owner/provider access and cannot be completed from the static repository alone.

### 1. Google Search Console
Create/verify the current website property for:
`https://noshabanqureshi-arch.github.io/`

Use a verification method supported for GitHub Pages.

### 2. Submit the sitemap
Submit:
`https://noshabanqureshi-arch.github.io/sitemap.xml`

### 3. Inspect priority URLs
Start with:
- homepage;
- `/resources/`;
- `/resources/turn-customer-questions-into-content/`;
- `/resources/how-to-choose-content-pillars-small-business/`;
- `/resources/use-ai-social-media-without-sounding-generic/`;
- `/products/30-day-content-starter/`.

Request indexing only when useful; do not repeatedly spam indexing requests.

### 4. Validate structured data
Use Google's Rich Results Test / Search Console enhancement reporting for:
- live Starter Product/Offer markup;
- Organization markup.

Do not add ratings/reviews until genuine customer review data exists and the markup matches visible content.

### 5. Establish the baseline
Once data appears, record:
- indexed pages;
- impressions;
- clicks;
- queries;
- pages receiving impressions;
- crawl/indexing errors;
- structured-data warnings/errors.

## Search content strategy
Do not create articles merely to increase page count.

Priority topic sources:
1. real small-business questions;
2. questions already covered in Square Social products/courses;
3. recurring objections;
4. content that demonstrates the Show Up Simply method;
5. topics where a useful free answer naturally leads to a real product or course.

Current evergreen cluster:
- turning customer questions into content;
- choosing content pillars;
- realistic posting frequency;
- AI without generic/invented content;
- simple short-form video;
- meaningful social-media measurement.

Build internal links between related resources as the library grows.

## Custom-domain migration rule
When a final branded domain is acquired:
- do not simply publish both domains as independent copies;
- configure GitHub Pages/custom-domain settings correctly;
- update canonical URLs, sitemap, Organization/Product markup and email links;
- verify the new property in Search Console;
- preserve redirects/canonical signals where the platform supports them;
- review every campaign/UTM link and provider callback URL.

Do not acquire or migrate a domain without checking brand/name conflict, renewal cost, DNS control and the email setup that will use it.
