# Source: https://docs.nadapay.io/docs/get-exchange-rate

## 

When to use this

[Skip link to When to use this](https://docs.nadapay.io/docs/get-exchange-rate#when-to-use-this)

Use this when you want to show a customer or operator an approximate conversion — for example, live-updating an amount field as they type. For anything you're about to execute, generate a formal [Quote](https://docs.nadapay.io/docs/get-exchange-rate#generate-quote) instead; rates here are indicative, not locked.

## 

Request

[Skip link to Request](https://docs.nadapay.io/docs/get-exchange-rate#request)

Bash

```
curl --request POST \
  --url $baseUrl/transactions/rate \
  --header 'x-api-key: YOUR_API_KEY' \
  --header 'Content-Type: application/json' \
  --data '{
    "currency": "KES"
  }'
```

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `currency` | string | Yes | Currency code to get the rate against USD |

## 

Response

[Skip link to Response](https://docs.nadapay.io/docs/get-exchange-rate#response)

Returns the current exchange rate for the requested currency against USD.

## 

Call this next

[Skip link to Call this next](https://docs.nadapay.io/docs/get-exchange-rate#call-this-next)

- [Generate Quote](https://docs.nadapay.io/docs/generate-quote) - to lock in a rate before executing
- [Check Transaction Limits](https://docs.nadapay.io/docs/check-transaction-limits)

Updated 2 months ago

---

Did this page help you?

Yes

No

Copy Page