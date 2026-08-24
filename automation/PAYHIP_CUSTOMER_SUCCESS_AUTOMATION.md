# Square Social Studio — Payhip Customer Success Automation

Purpose: automate post-purchase logging, quick-start support and refund-state updates without turning a purchase into automatic marketing consent.

## Official event source
Use Payhip's Developer webhooks.

For the current $27 Starter, listen to:
- `paid`;
- `refunded`.

Future subscription products may also use:
- `subscription.created`;
- `subscription.deleted`.

## Security requirement

Payhip webhook payloads include a `signature` field.

Verify the incoming signature before processing the event.
Payhip documents the expected signature as the SHA-256 hash of the account API key.

Keep the Payhip API key only in a protected Make connection/secret variable.
Never put the API key, signature secret or customer payload into GitHub.

If signature verification fails:
- return/handle safely according to the webhook implementation;
- do not create/update customer records;
- record a private security/error event;
- alert owner only if repeated.

## Privacy/minimization rule

Payhip may send fields such as customer email, transaction ID, price, item details, payment type and IP address.

For Square Social v1, retain only what is operationally necessary.

Recommended private fields:
- transaction_id;
- customer_email;
- product_name/product identifier;
- amount/currency;
- purchase timestamp;
- event type;
- refund amount/status;
- support status;
- quick-start sent timestamp.

Do NOT retain the customer's IP address in the Square Social runtime store unless there is a documented security/legal reason to do so.

Do not put any customer fields into the public repository.

## Scenario: `SSS — Payhip Purchase Success v1`

### Module 1 — Make Custom Webhook
Create a private Make webhook endpoint.

Add that endpoint in Payhip:
Settings → Developer → Webhooks.

Subscribe to `paid` and `refunded` for the first version.

### Module 2 — Verify event signature
Before processing:
- hash the protected Payhip API key using SHA-256;
- compare it with the payload `signature`;
- stop on mismatch.

### Module 3 — Route by event type

#### `paid`
Continue to purchase-success flow.

#### `refunded`
Continue to refund-state flow.

Ignore unsupported event types in v1.

## Paid event flow

### Step A — Validate product
Confirm the event includes the live:
`30-Day Content Starter`.

Do not apply Starter-specific messaging to unrelated future products.

### Step B — Record purchase privately
Store:
- transaction ID;
- email;
- product;
- amount/currency;
- purchase time;
- status `paid`.

Use transaction ID as an idempotency key so a retried webhook does not create a duplicate customer-success sequence.

### Step C — Do not interfere with Payhip delivery
Payhip remains responsible for the protected product delivery/receipt flow.

Square Social automation should not duplicate the paid ZIP as an unsecured attachment.

### Step D — Transactional quick-start
Send or prepare a short post-purchase message that helps the buyer use the product.

Suggested content:
- thank them for purchasing the 30-Day Content Starter;
- remind them to use their Payhip receipt/download link for file access;
- point to the public noindex customer quick-start page where appropriate;
- provide the temporary Square Social support route for download/access problems;
- tell them not to send payment-card details by email.

This message is customer service/transactional, not a marketing newsletter.

### Step E — Marketing-consent separation
A purchase does not automatically place the customer into ongoing promotional email.

Only add the buyer to marketing automation when a separate valid consent record exists.

When marketing automation becomes active, customers may be tagged privately as `starter_customer` to suppress irrelevant acquisition messages for the product they already own.

### Step F — Optional implementation check-in later
After a reasonable usage period, Square Social may send a customer-success check-in such as:
- Were you able to open the files?
- Which planning step did you use first?
- Was anything confusing?

Do not pressure for a public review.

If asking for feedback:
- collect feedback privately first;
- obtain separate permission before publishing any testimonial/name/business detail.

## Refund event flow

### Step A — Match transaction
Find the private record by Payhip transaction ID.

### Step B — Record refund status
Store:
- refund amount;
- refund timestamp;
- full vs partial status where determinable;
- current order state.

### Step C — Suppression/flags
Stop future customer-success/promotional sequences that would be inappropriate after a full refund.

Do not automatically argue, refuse or reverse a refund.
Refund decisions remain human/provider controlled.

### Step D — CEO metrics
Include refunded amount/count in weekly reporting.

## Error handling

Payhip retries webhook POSTs when the configured endpoint does not return a successful response.

Therefore:
- make purchase processing idempotent using transaction ID;
- never send duplicate quick-start emails because the webhook was retried;
- log failed stages privately;
- alert only after automatic retries cannot resolve the problem.

## Definition of done

After a real/test Starter purchase:
1. Payhip delivers the product normally;
2. webhook is verified;
3. purchase is recorded once;
4. transactional quick-start/support message is generated/sent once;
5. marketing consent remains separate;
6. a refund later updates the same transaction record rather than creating a duplicate.

That removes routine customer-success admin without weakening privacy or consent boundaries.