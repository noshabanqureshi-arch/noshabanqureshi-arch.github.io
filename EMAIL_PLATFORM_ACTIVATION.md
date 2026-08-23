# Square Social Studio — Email Platform Activation

Purpose: turn the existing email-platform setup into a compliant, low-maintenance owned-audience system without blocking the current Payhip product funnel or confusing temporary customer support with marketing consent.

## Current verified state

- A **Mailchimp account already exists** for Square Social Studio.
- The account is currently on Mailchimp's free plan.
- The audience has been initialized, but there is not yet evidence that Square Social has a meaningful permission-based marketing list.
- Existing Square Social email drafts/automation copy already exist separately.
- No verified Square Social custom domain or authenticated branded-domain sender has been found yet.
- The brand-named Gmail address `squaresocialstudio@gmail.com` is now published on the Contact page as a **temporary launch support/inquiry inbox** so buyers have a business-controlled way to get help.
- That temporary support Gmail is **not** treated as the final Mailchimp sender identity or as proof that marketing automation is ready.
- Do not switch on ongoing marketing automation merely because the Mailchimp account and temporary support inbox exist.

No provider credentials, private IDs or customer data belong in the public repository.

## Email-role separation

### Transactional
Payhip handles order/download messages for the live Starter and later the free PDF if the $0 product is activated.

Transactional delivery does not equal marketing consent.

### Temporary launch support
Current public support/inquiry route:
`squaresocialstudio@gmail.com`

Use it for:
- order/access questions,
- simple business inquiries,
- launch-stage support.

Do not ask customers to email:
- passwords,
- full card details,
- customer lists,
- sensitive client records.

### Future marketing sender
Ongoing Mailchimp marketing should wait for the permanent domain/sender/contact setup and full consent/unsubscribe QA below.

---

# Activation sequence

## Gate 1 — permanent business sender identity
Before ongoing marketing email is activated, Square Social needs:
- a final business/domain decision;
- a branded-domain sender/support email address;
- a valid business mailing/contact address appropriate for required commercial-email footer information;
- a public contact/support method that matches the privacy notice;
- sender/domain authentication where the selected provider supports/requires it.

The temporary Gmail support route can remain available during migration, but it should not become the reason to skip the permanent sender setup.

## Gate 2 — Mailchimp audience hygiene
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

## Gate 3 — permission-based signup form
Create one permission-based signup form with:

**Headline:** Get practical content-planning ideas from Square Social Studio.

**Description:** Useful systems, examples and relevant product updates for service- and expertise-based small businesses.

**Consent:** clear affirmative opt-in. Do not pre-check the marketing box.

The free Payhip order/download can remain transactional. It does not need to be treated as blanket marketing consent.

## Gate 4 — welcome sequence
Once sender identity, consent and unsubscribe are tested, activate the existing nurture sequence:
1. orient + deliver/use the free resource;
2. Teach / Trust / Connect / Offer / Convert;
3. introduce the live $27 Starter;
4. teach Clarify → Plan → Create → Publish → Repeat;
5. show only the next offers that are actually live.

## Gate 5 — purchase suppression
When integration/tagging allows:
- stop promoting a product to someone who already owns it;
- keep transactional Payhip receipts/delivery separate;
- move customers into implementation/customer-success messages;
- promote only the next relevant live offer.

## Gate 6 — testing
Before sending the first automated sequence, verify:
- sender identity/authentication;
- mailing/contact address/footer;
- consent capture;
- unsubscribe;
- mobile rendering;
- accessibility/readability;
- link destinations and UTMs;
- purchase suppression/tags if available;
- privacy notice reflects the active data flow.

---

# First metrics
Track:
- valid consented subscribers;
- delivery/bounce;
- resource-to-product clicks;
- Starter sales associated with email traffic when attribution is technically reliable;
- unsubscribe/complaint signals;
- revenue per subscriber;
- repeat purchase;
- movement to course/Vault when those offers become live.

# Capacity rule
Email should reduce selling effort, not create daily newsletter pressure.

Default operating model:
- automated welcome/customer-success flows;
- a practical broadcast only when there is something useful to teach or announce;
- reuse existing resources, videos and product lessons before creating an email-only content stream.
