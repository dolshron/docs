# Source: https://docs.nadapay.io/docs/generate-quote-1

## 

When to use this

[Skip link to When to use this](https://docs.nadapay.io/docs/generate-quote-1#when-to-use-this)

Use this once you know your source account, destination details, amount, and rail — and before calling Execute Transaction.

## 

Prerequisites

[Skip link to Prerequisites](https://docs.nadapay.io/docs/generate-quote-1#prerequisites)

- A valid `x-api-key`
- A unique `x-idempotency-key` for this request
- Source account confirmed (the account you intend to debit)
- Destination/beneficiary account confirmed and complete
- Amount validated against corridor limits (see [Check Transaction Limits](https://docs.nadapay.io/docs/check-transaction-limits))

## 

Request

[Skip link to Request](https://docs.nadapay.io/docs/generate-quote-1#request)

Bash

```
curl --request POST \
  --url $baseUrl/transactions/quote \
  --header 'x-api-key: YOUR_API_KEY' \
  --header 'Content-Type: application/json' \
  --header 'x-idempotency-key: YOUR_UNIQUE_UUID' \
  --data '{
    "source": {
      "accountId": "string",
      "currency": "USD",
      "amount": 1000000,
      "rail": "ACH",
      "chain": "Ethereum",
      "address": "string",
      "type": "CRYPTO"
    },
    "destination": {
      "beneficiaryAccountId": "string",
      "accountId": "string",
      "currency": "USD",
      "type": "BANK",
      "accountNumber": "string",
      "bankCode": "string",
      "country": "Nigeria",
      "chain": "Base",
      "address": "string",
      "name": "string",
      "paymentMethod": "Bank Transfer"
    },
    "metadata": {}
  }'
```

The `source` object describes where funds come from. The `destination` object describes which beneficiary account or address will receive the funds.

## 

Response

[Skip link to Response](https://docs.nadapay.io/docs/generate-quote-1#response)

Returns the priced `quoteId` along with the finalized source and destination terms. **Save the** `quoteId` - you'll need it immediately for execution.

## 

Common failure reasons

[Skip link to Common failure reasons](https://docs.nadapay.io/docs/generate-quote-1#common-failure-reasons)

- Amount falls outside the supported limit range
- Source/destination configuration isn't supported together
- Destination details don't match the selected rail

## 

Do not continue if

[Skip link to Do not continue if](https://docs.nadapay.io/docs/generate-quote-1#do-not-continue-if)

- The amount is outside supported limits
- Source or destination details don't match the rail
- You didn't receive a valid `quoteId`

## 

Call this next

[Skip link to Call this next](https://docs.nadapay.io/docs/generate-quote-1#call-this-next)

- [Execute Transaction](https://docs.nadapay.io/docs/execute-transaction)
- [Check Transaction Limits](https://docs.nadapay.io/docs/check-transaction-limits)

Updated 2 months ago

---

Did this page help you?

Yes

No

Copy Page