# Source: https://docs.nadapay.io/docs/get-deposit-instructions

Get deposit instructions so your team or clients know exactly how to fund a NadaPay account.

## 

When to use this page

[Skip link to When to use this page](https://docs.nadapay.io/docs/get-deposit-instructions#when-to-use-this-page)

Use this page when you need the exact funding instructions for a NadaPay account before money is sent into the platform.

## 

Prerequisites

[Skip link to Prerequisites](https://docs.nadapay.io/docs/get-deposit-instructions#prerequisites)

1. Set your NadaPay API base URL in `$baseUrl`.
2. Export your NadaPay API key as `YOUR_API_KEY`.
3. Generate a unique idempotency key for the request.

## 

Before you continue

[Skip link to Before you continue](https://docs.nadapay.io/docs/get-deposit-instructions#before-you-continue)

- confirm the destination `nadapayCode` for the account you want to fund
- confirm the source currency, country, and amount for the funding flow
- gather any additional values required inside `source.details` for the rail you are using

## 

Step 1 - Fetch deposit instructions

[Skip link to Step 1 - Fetch deposit instructions](https://docs.nadapay.io/docs/get-deposit-instructions#step-1---fetch-deposit-instructions)

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

**Response:**

A successful response returns the deposit instructions for the requested source and destination. Use the response shape shown in the API Reference for this endpoint.

**Response - error:**

JSON

```
{
  "statusCode": 500,
  "message": "Internal server error"
}
```

## 

What success looks like

[Skip link to What success looks like](https://docs.nadapay.io/docs/get-deposit-instructions#what-success-looks-like)

- you receive a full set of funding instructions
- the returned `reference` is saved and shared with the funding party
- the destination account details match the account you intend to fund

## 

Do not continue if

[Skip link to Do not continue if](https://docs.nadapay.io/docs/get-deposit-instructions#do-not-continue-if)

- the destination `nadapayCode` is incorrect
- the returned funding instructions do not match the account you intend to fund
- the required funding details for the selected rail are incomplete

## 

Step 2 - Share the instructions with the funding party

[Skip link to Step 2 - Share the instructions with the funding party](https://docs.nadapay.io/docs/get-deposit-instructions#step-2---share-the-instructions-with-the-funding-party)

Provide the full instruction set, including the `reference`, to whoever is initiating the inbound transfer. The `reference` is how NadaPay matches the inbound payment to your wallet.

> ⚠️
> 
> ### 
> 
> Deposit instructions are unique per wallet and must include the exact `reference` provided. Missing or incorrect references will delay crediting.
> 
> [Skip link to Deposit instructions are unique per wallet and must include the exact ,\[object Object\], provided. Missing or incorrect references will delay crediting.](https://docs.nadapay.io/docs/get-deposit-instructions#deposit-instructions-are-unique-per-wallet-and-must-include-the-exact-reference-provided-missing-or-incorrect-references-will-delay-crediting)

## 

What this step returns

[Skip link to What this step returns](https://docs.nadapay.io/docs/get-deposit-instructions#what-this-step-returns)

- funding instructions for the destination account
- the reference to include with the inbound payment

Save the returned instruction set exactly as provided and share the `reference` with the funding party.

## 

Common reasons this step fails

[Skip link to Common reasons this step fails](https://docs.nadapay.io/docs/get-deposit-instructions#common-reasons-this-step-fails)

- the destination `nadapayCode` is incorrect
- the source funding details are incomplete for the selected rail
- the requested funding configuration is not supported

## 

Call this next

[Skip link to Call this next](https://docs.nadapay.io/docs/get-deposit-instructions#call-this-next)

- [Collection Overview](https://docs.nadapay.io/docs/collection-overview)
- [Fetch Transaction Limits](https://docs.nadapay.io/docs/fetch-transaction-limits)
- [Authenticate with x-api-key](https://docs.nadapay.io/docs/how-to)

Updated 2 months ago

---

Did this page help you?

Yes

No

Copy Page