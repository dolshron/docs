# Source: https://docs.nadapay.io/docs/get-deposit-instructions-1

## 

Prerequisites

[Skip link to Prerequisites](https://docs.nadapay.io/docs/get-deposit-instructions-1#prerequisites)

- The destination `nadapayCode` for the wallet you want to fund
- Source currency, country, and amount for the funding flow
- Any additional `source.details` required for the rail you're using

## 

Request

[Skip link to Request](https://docs.nadapay.io/docs/get-deposit-instructions-1#request)

Bash

```
curl --request POST \
  --url $baseUrl/transactions/deposit-instructions \
  --header 'x-api-key: YOUR_API_KEY' \
  --header 'Content-Type: application/json' \
  --header 'x-idempotency-key: YOUR_UNIQUE_UUID' \
  --data '{
    "source": {
      "currency": "USD",
      "country": "NG",
      "amount": 100,
      "details": {}
    },
    "destination": {
      "nadapayCode": "WAL-123"
    }
  }'
```

## 

Response

[Skip link to Response](https://docs.nadapay.io/docs/get-deposit-instructions-1#response)

Returns the full funding instruction set, including a `reference`.

> **The** `reference` **is critical.** NadaPay uses it to match the inbound payment to the correct wallet. Share it exactly as returned with whoever is initiating the transfer — missing or incorrect references delay crediting.

## 

What success looks like

[Skip link to What success looks like](https://docs.nadapay.io/docs/get-deposit-instructions-1#what-success-looks-like)

- You receive a full set of funding instructions
- The `reference` is saved and shared with the funding party
- The destination details match the wallet you intend to fund

## 

Do not continue if

[Skip link to Do not continue if](https://docs.nadapay.io/docs/get-deposit-instructions-1#do-not-continue-if)

- The destination `nadapayCode` is incorrect
- The returned instructions don't match the intended wallet
- Required funding details for the selected rail are incomplete

## 

Call this next

[Skip link to Call this next](https://docs.nadapay.io/docs/get-deposit-instructions-1#call-this-next)

- Wait for a webhook confirming the deposit landed — don't assume success from this call alone

Updated 2 months ago

---

Did this page help you?

Yes

No

Copy Page