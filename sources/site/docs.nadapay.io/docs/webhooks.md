# Source: https://docs.nadapay.io/docs/webhooks

## 

Endpoints

[Skip link to Endpoints](https://docs.nadapay.io/docs/webhooks#endpoints)

| Method | Path | Purpose |
| --- | --- | --- |
| `POST` | `/organization/webhooks` | Register a webhook endpoint |
| `GET` | `/organization/webhooks` | List webhooks |
| `GET` | `/organization/webhooks/:id` | Get webhook details |
| `PATCH` | `/organization/webhooks/:id` | Update a webhook |
| `DELETE` | `/organization/webhooks/:id` | Delete a webhook |
| `GET` | `/organization/webhooks/deliveries/history` | View delivery history |
| `POST` | `/organization/webhooks/deliveries/:id/retry` | Retry a failed delivery |

## 

Register a webhook

[Skip link to Register a webhook](https://docs.nadapay.io/docs/webhooks#register-a-webhook)

Bash

```
curl --request POST \
  --url $baseUrl/organization/webhooks \
  --header 'x-api-key: YOUR_API_KEY' \
  --header 'Content-Type: application/json'
```

> Webhook environment is determined by the API key used — `np_test_...` keys register sandbox webhooks, `np_live_...` keys register live webhooks.

## 

Verify the signature

[Skip link to Verify the signature](https://docs.nadapay.io/docs/webhooks#verify-the-signature)

Every webhook includes an `X-Nadapay-Signature` header (HMAC-SHA256). Verify it before processing:

JavaScript

```
const crypto = require('crypto');

function verifyWebhook({ rawBody, signature, timestamp, secret }) {
  const signedPayload = `${timestamp}.${rawBody}`;

  const expectedSignature = crypto
    .createHmac('sha256', secret)
    .update(signedPayload)
    .digest('hex');

  return crypto.timingSafeEqual(
    Buffer.from(signature, 'hex'),
    Buffer.from(expectedSignature, 'hex')
  );
}
```

> **Verify the raw request body exactly as received.** Parsing and re-stringifying the JSON before verification can change whitespace or key ordering and break the signature check.

## 

Supported events

[Skip link to Supported events](https://docs.nadapay.io/docs/webhooks#supported-events)

| Event | Description |
| --- | --- |
| `TRANSACTION.CREATED` | A new transaction was initialized |
| `TRANSACTION.AWAITING_FUNDS` | Deposit flow waiting for funds |
| `TRANSACTION.PROCESSING` | Funds detected, being processed |
| `TRANSACTION.EXECUTING` | Sent to external banking/crypto rails |
| `TRANSACTION.COMPLETED` | Settled successfully |
| `TRANSACTION.FAILED` | Failed — check `failureReason` in payload |
| `TRANSACTION.QUEUED` | Awaiting liquidity resolution |
| `VERIFICATION.COMPLETED` | KYC/KYB process finished |

## 

Payload format

[Skip link to Payload format](https://docs.nadapay.io/docs/webhooks#payload-format)

JSON

```
{
  "id": "delivery-uuid",
  "event": "TRANSACTION.COMPLETED",
  "environment": "LIVE",
  "timestamp": 1713289200000,
  "data": {
    "reference": "NP-ABCD-1234",
    "internalReference": "PAY-XYZ-999",
    "status": "COMPLETED",
    "sourceAmount": "1000.00",
    "sourceCurrency": "USD",
    "targetAmount": "1000.00",
    "targetCurrency": "USD",
    "totalFee": "5.00",
    "rail": "BRIDGE",
    "metadata": {}
  }
}
```

Amounts are dollar-style decimal strings, e.g. `"1000.00"`.

## 

Respond quickly

[Skip link to Respond quickly](https://docs.nadapay.io/docs/webhooks#respond-quickly)

Return a `2xx` as soon as you've received and validated the event — do the heavy processing in a background job.

HTTP

```
HTTP/1.1 202 Accepted
```

## 

Retry schedule

[Skip link to Retry schedule](https://docs.nadapay.io/docs/webhooks#retry-schedule)

If your endpoint doesn't return `2xx`, NadaPay retries with exponential backoff:

| Attempt | Delay |
| --- | --- |
| 1 | 2 minutes |
| 2 | 4 minutes |
| 3 | 8 minutes |
| 4 | 16 minutes |
| 5 | 32 minutes |

## 

Best practices

[Skip link to Best practices](https://docs.nadapay.io/docs/webhooks#best-practices)

- Return `200`/`202` quickly; verify signature before processing
- Deduplicate using the webhook `id` — deliveries can arrive more than once
- Store secrets in a server-side secret manager
- Use HTTPS on every endpoint
- Log `id`, `event`, `timestamp`, and `data.reference` for reconciliation

## 

Troubleshooting

[Skip link to Troubleshooting](https://docs.nadapay.io/docs/webhooks#troubleshooting)

- **Signature fails** — confirm you're verifying the raw body, the secret matches, and you're reading from `X-Nadapay-Signature`
- **Repeated retries** — your endpoint isn't returning `2xx`
- **Duplicate events** — use the webhook `id` as your dedup key

Updated 2 months ago

---

Did this page help you?

Yes

No

Copy Page