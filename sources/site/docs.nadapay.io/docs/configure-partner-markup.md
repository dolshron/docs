# Source: https://docs.nadapay.io/docs/configure-partner-markup

> **Restricted:** only available to organizations with `PARTNER` class.

## 

Request

[Skip link to Request](https://docs.nadapay.io/docs/configure-partner-markup#request)

Bash

```
curl --request POST \
  --url $baseUrl/organizations/fees \
  --header 'x-api-key: YOUR_API_KEY' \
  --header 'Content-Type: application/json' \
  --header 'x-idempotency-key: YOUR_UNIQUE_UUID' \
  --data '{
    "txType": "PAYOUT",
    "markupBps": 50,
    "reason": "Strategic adjustment"
  }'
```

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `txType` | `PAYOUT` | `DEPOSIT` | `FX_SWAP` | Yes | Which transaction type this markup applies to |
| `markupBps` | number | Yes | Markup in basis points (50 = 0.5%) |
| `reason` | string | No | Internal note for the adjustment |

## 

Response

[Skip link to Response](https://docs.nadapay.io/docs/configure-partner-markup#response)

Confirms the updated fee markup configuration.

## 

When to use this

[Skip link to When to use this](https://docs.nadapay.io/docs/configure-partner-markup#when-to-use-this)

Use this if you're a partner platform earning revenue on top of NadaPay's base rates for transactions your child organizations process.

Updated 2 months ago

---

Did this page help you?

Yes

No

Copy Page