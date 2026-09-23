# Source: https://docs.nadapay.io/docs/check-transaction-limits

## 

When to use this

[Skip link to When to use this](https://docs.nadapay.io/docs/check-transaction-limits#when-to-use-this)

Use this once you know the corridor and amount, before quoting or executing.

## 

Request

[Skip link to Request](https://docs.nadapay.io/docs/check-transaction-limits#request)

Bash

```
curl --request POST \
  --url $baseUrl/transactions/limits \
  --header 'x-api-key: YOUR_API_KEY' \
  --header 'Content-Type: application/json' \
  --header 'x-idempotency-key: YOUR_UNIQUE_UUID' \
  --data '{
    "currency": "USD",
    "country": "NG",
    "rail": "bank_transfer"
  }'
```

## 

Response

[Skip link to Response](https://docs.nadapay.io/docs/check-transaction-limits#response)

Returns the minimum amount, maximum amount, and any daily limit for the requested corridor.

## 

Validate before executing

[Skip link to Validate before executing](https://docs.nadapay.io/docs/check-transaction-limits#validate-before-executing)

```
transaction_amount >= minimum_amount
transaction_amount <= maximum_amount
daily_volume + transaction_amount <= daily_limit
```

Surface a clear error to the user if the amount falls outside these bounds — don't let it fail at execution time instead.

> **Limits can change.** Fetch them fresh per session rather than hardcoding them in your application.

## 

Common failure reasons

[Skip link to Common failure reasons](https://docs.nadapay.io/docs/check-transaction-limits#common-failure-reasons)

- The corridor isn't supported for the currency/country pair
- The rail value is invalid for the transaction
- No matching limit configuration exists

## 

Call this next

[Skip link to Call this next](https://docs.nadapay.io/docs/check-transaction-limits#call-this-next)

- [Get Supported Networks](https://docs.nadapay.io/docs/get-supported-networks)
- [Generate Quote](https://docs.nadapay.io/docs/generate-quote)

Updated 2 months ago

---

Did this page help you?

Yes

No

Copy Page