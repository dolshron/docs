# Source: https://docs.nadapay.io/docs/get-currency-balance

## 

Request

[Skip link to Request](https://docs.nadapay.io/docs/get-currency-balance#request)

Bash

```
curl --request GET \
  --url "$baseUrl/organizations/balance/{currency}" \
  --header 'x-api-key: YOUR_API_KEY'
```

| Path param | Required | Description |
| --- | --- | --- |
| `currency` | Yes | Currency code, e.g. `USD`, `NGN`, `USDC` |

## 

Response

[Skip link to Response](https://docs.nadapay.io/docs/get-currency-balance#response)

Returns the balance details for the requested currency.

## 

When to use this vs. List Financial Accounts

[Skip link to When to use this vs. List Financial Accounts](https://docs.nadapay.io/docs/get-currency-balance#when-to-use-this-vs-list-financial-accounts)

Use this when you already know which currency you care about and just need the number — e.g., checking sufficient balance before generating a quote. Use [List Financial Accounts](https://docs.nadapay.io/docs/list-financial-accounts) when you need to see everything at once, like rendering a dashboard.

Updated 2 months ago

---

Did this page help you?

Yes

No

Copy Page