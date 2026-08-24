# Square Social Studio — Support Triage Automation

Purpose: reduce owner inbox time by letting AI classify and draft routine support responses while escalating payment, refund, privacy, complaint and unusual cases.

## Scope for v1

Support categories:
- download/access problem;
- lost receipt/download link;
- product-use question;
- general product question;
- refund/payment issue;
- privacy/data question;
- complaint;
- business/service inquiry;
- spam/irrelevant.

## Trigger
New message in the designated Square Social support inbox.

Do not use the owner's unrelated personal inbox as the automation source.

## Privacy rule

Only send the minimum email content needed for classification/drafting to the AI provider.

Do not expose:
- payment-card information;
- passwords;
- API keys;
- private client files;
- unrelated inbox history.

If a customer sends sensitive payment/card data, flag for owner handling and avoid copying it into other systems.

## Scenario: `SSS — Support Triage v1`

### Step 1 — Read new support email
Collect:
- sender email;
- subject;
- message body;
- message/thread ID;
- attachment metadata only if needed.

### Step 2 — Claude classification
Return JSON:

```json
{
  "category": "download_access",
  "risk": "low",
  "needs_owner": false,
  "needs_order_lookup": true,
  "draft_reply": "...",
  "reason": "Customer cannot find the Payhip download link."
}
```

Allowed `risk` values:
- low;
- medium;
- high.

### Step 3 — Routing

#### Low risk
Examples:
- where to find Payhip receipt/download;
- how to unzip/open the files;
- where the quick-start instructions are;
- factual question already answered in approved product FAQ.

AI may prepare a complete reply from approved support rules.

During the first phase, save as draft or place in `READY_TO_SEND`; do not fully auto-send until several weeks of drafts have proven reliable.

#### Medium risk
Examples:
- customer says product does not match expectations;
- unusual file/access failure;
- ambiguous billing issue;
- service/client inquiry.

Draft a reply but require owner review.

#### High risk
Always owner-handled:
- refund request;
- payment dispute;
- chargeback threat;
- privacy/data request;
- legal complaint;
- harassment/threat;
- customer alleges harm or material misrepresentation;
- request to delete/export customer data;
- anything involving credentials or sensitive information.

Do not generate a final decision for these cases.

## Approved low-risk response principles

### Download/access
- direct customer back to the Payhip receipt/download email first;
- confirm the product name;
- explain that Payhip handles protected delivery;
- provide the Square Social quick-start/support route when relevant;
- do not attach a paid ZIP from an unsecured email unless a verified support process explicitly requires it.

### Product-use question
- answer using verified Starter content and the public quick-start page;
- do not invent missing worksheets/features;
- if the question exceeds the product scope, say so clearly.

### General product question
- use current manifest for price/status;
- current live Starter = CAD $27;
- planned products must not be described as available.

## Owner notification rule

Do not notify the owner for every routine message.

Notify when:
- risk = high;
- confidence is low;
- the same support failure repeats across customers;
- a product file/link may actually be broken;
- the message contains a new objection/question worth business attention.

## Knowledge feedback loop

Once weekly, summarize non-identifying repeated support themes:
- recurring access issue;
- recurring confusion;
- repeated pre-purchase question;
- recurring objection;
- possible FAQ/product improvement.

Feed useful patterns into the weekly CEO report.

Do not publish customer wording or identity without permission.

## Success target

Owner should not spend time manually composing the same download/access answer repeatedly.

The system should:
- classify routine issues;
- draft accurate responses;
- surface exceptions;
- turn repeated support patterns into product improvements.

The goal is fewer inbox decisions, not an unsupervised customer-service bot.