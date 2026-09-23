# Source: https://docs.nadapay.io/docs

Get the available provider networks for a country so you can choose the right payout rail before you add a beneficiary account.

## 

Prerequisites

[Skip link to Prerequisites](https://docs.nadapay.io/docs/get-provider-networks#prerequisites)

1. Set your NadaPay API base URL in `$baseUrl`.
2. Export your NadaPay API key as `YOUR_API_KEY`.
3. Generate a unique idempotency key for the request.

## 

Step 1 - Fetch provider networks for a country

[Skip link to Step 1 - Fetch provider networks for a country](https://docs.nadapay.io/docs/get-provider-networks#step-1---fetch-provider-networks-for-a-country)

Bash

```
curl --request POST \
  --url $baseUrl/transactions/networks \
  --header 'x-api-key: YOUR_API_KEY' \
  --header 'Content-Type: application/json' \
  --header 'x-idempotency-key: YOUR_UNIQUE_UUID' \
  --data '{
    "country": "GH"
  }'
```

**Response:**

JSON

```
{
  "data": {
    "country": "GH",
    "networks": [
      {
        "code": "bank_transfer",
        "name": "Local Bank Transfer",
        "currency": "GHS",
        "type": "bank_account"
      },
      {
        "code": "mtn_momo",
        "name": "MTN Mobile Money",
        "currency": "GHS",
        "type": "mobile_money"
      },
      {
        "code": "vodafone_cash",
        "name": "Vodafone Cash",
        "currency": "GHS",
        "type": "mobile_money"
      }
    ]
  }
}
```

## 

Step 2 - Use the network result when you add a beneficiary account

[Skip link to Step 2 - Use the network result when you add a beneficiary account](https://docs.nadapay.io/docs/get-provider-networks#step-2---use-the-network-result-when-you-add-a-beneficiary-account)

Use the returned network identifier in the `details` object required by the [Add Beneficiary Account](https://docs.nadapay.io/reference/beneficiarycontroller_addaccount) API reference for your selected account type.

> 📘
> 
> ### 
> 
> Network availability varies by corridor. Always fetch provider networks dynamically rather than hardcoding them.
> 
> [Skip link to Network availability varies by corridor. Always fetch provider networks dynamically rather than hardcoding them.](https://docs.nadapay.io/docs/get-provider-networks#network-availability-varies-by-corridor-always-fetch-provider-networks-dynamically-rather-than-hardcoding-them)

## 

What's next

[Skip link to What's next](https://docs.nadapay.io/docs/get-provider-networks#whats-next)

- [Resolve a Bank Account](https://docs.nadapay.io/docs/resolve-bank-account)
- [Create a Beneficiary](https://docs.nadapay.io/docs/create-beneficiary)
- [Authenticate with x-api-key](https://docs.nadapay.io/docs/how-to)

Updated about 2 months ago

---

Did this page help you?

Yes

No

Copy Page