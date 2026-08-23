# Square Social Studio — Email Platform Activation

Purpose: turn the existing email-platform setup into a compliant, low-maintenance owned-audience system without blocking the current Payhip product funnel.

## Current verified state

- A **Mailchimp account already exists** for Square Social Studio.
- The account is currently on Mailchimp's free plan.
- The audience has been initialized, but there is not yet evidence that Square Social has a meaningful marketing list.
- Existing Square Social email drafts/automation copy already exist separately.
- No evidence was found that a Square Social custom domain or branded sending address has been registered/authenticated yet.
- Do not switch on ongoing marketing automation merely because the Mailchimp account exists.

No account credentials, personal email addresses or provider IDs belong in the public repository.

## Activation sequence

### Gate 1 — business sender identity
Before ongoing marketing email is activated, Square Social needs:
- a final business/domain decision;
- a branded sender/support email address;
- a valid business mailing address appropriate for the commercial-email footer;
- a public contact/support method that matches the privacy notice.

### Gate 2 — Mailchimp audience hygiene
Configure the audience so Square Social can distinguish:
- free-resource leads with explicit marketing consent;
- purchasers;
- course students;
- Vault members;
- premium clients.

Minimum fields/tags where supported:
- email;
- first name optional;
- consent source;
- consent timestamp or provider record;
- lead magnet/source;
- purchase/product tag when available.

Do not upload scraped/public email addresses as marketing subscribers.

### Gate 3 — signup form
Create one permission-based signup form with:

**Headline:** Get practical content-planning ideas from Square Social Studio.

**Description:** Useful systems, examples and relevant product updates for service- and expertise-based small businesses.

**Consent:** clear affirmative opt-in. Do not pre-check the marketing box.

The free Payhip order/download can remain transactional. It does not need to be treated as blanket marketing consent.

### Gate 4 — welcome sequence
Once sender identity, consent and unsubscribe are tested, activate the existing nurture sequence:
1. orient + deliver/use the free resource;
2. Teach / Trust / Connect / Offer / Convert;
3. introduce the live $27 Starter;
4. teach Clarify → Plan → Create → Publish → Repeat;
5. show only the next offers that are actually live.

### Gate 5 — purchase suppression
When integration/tagging allows:
- stop promoting a product to someone who already owns it;
- keep transactional Payhip receipts/delivery separate;
- move customers into implementation/customer-success messages;
- promote only the next relevant live offer.

### Gate 6 — testing
Before sending the first automated sequence, verify:
- sender identity;
- mailing address/footer;
- consent capture;
- unsubscribe;
- mobile rendering;
- link destinations;
- purchase suppression/tags if available;
- privacy notice reflects the active data flow.

## First metrics
Track:
- valid consented subscribers;
- delivery/bounce;
- resource-to-product clicks;
- Starter sales associated with email traffic;
- unsubscribe/complaint signals;
- revenue per subscriber;
- repeat purchase;
- movement to course/Vault when those offers become live.

## Capacity rule
Email should reduce selling effort, not create daily newsletter pressure.

Default operating model:
- automated welcome/customer-success flows;
- a practical broadcast only when there is something useful to teach or announce;
- reuse existing resources, videos and product lessons before creating an email-only content stream.
