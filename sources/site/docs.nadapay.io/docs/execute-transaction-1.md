# Source: https://docs.nadapay.io/docs/execute-transaction-1

## 

When to use this

[Skip link to When to use this](https://docs.nadapay.io/docs/execute-transaction-1#when-to-use-this)

Only after you have a valid `quoteId` and the source/destination values still match what you priced.

## 

Prerequisites

[Skip link to Prerequisites](https://docs.nadapay.io/docs/execute-transaction-1#prerequisites)

- A valid `x-api-key`
- A unique `x-idempotency-key` for this request
- A `quoteId` from [Generate Quote](https://docs.nadapay.io/docs/generate-quote)
- Confirmed source account has sufficient balance

## 

Request

[Skip link to Request](https://docs.nadapay.io/docs/execute-transaction-1#request)

Bash

```
curl --request POST \
  --url $baseUrl/transactions/execute \
  --header 'x-api-key: YOUR_API_KEY' \
  --header 'Content-Type: application/json' \
  --header 'x-idempotency-key: YOUR_UNIQUE_UUID' \
  --data '{
    "quoteId": "string",
    "reason": "gift",
    "reasonDescription": "string",
    "metadata": {},
    "source": {
      "accountId": "string",
      "nadapayCode": "WAL-123",
      "amount": 1000000
    },
    "destination": {
      "beneficiaryAccountId": "string",
      "accountId": "string",
      "nadapayCode": "WAL-456"
    }
  }'
```

The `quoteId` must come from the quote step, and the source/destination values here must match what you priced.

## 

Response

[Skip link to Response](https://docs.nadapay.io/docs/execute-transaction-1#response)

Returns the transaction created from the quote. Save the returned transaction identifiers for monitoring and reconciliation.

## 

Common failure reasons

[Skip link to Common failure reasons](https://docs.nadapay.io/docs/execute-transaction-1#common-failure-reasons)

- The quote is expired or invalid
- The source account doesn't have enough balance
- Source/destination values don't match the priced quote
- The transaction is blocked by corridor or compliance conditions

## 

Do not continue if

[Skip link to Do not continue if](https://docs.nadapay.io/docs/execute-transaction-1#do-not-continue-if)

- The quote is expired or invalid
- The source account has insufficient balance
- Destination values don't match the quote

## 

Call this next

[Skip link to Call this next](https://docs.nadapay.io/docs/execute-transaction-1#call-this-next)

- [Get Deposit Instructions](https://docs.nadapay.io/docs/get-deposit-instructions) _(Wallet API)_
- Monitor via webhook or session status polling

Updated 2 months ago

---

Did this page help you?

Yes

No

Copy Page