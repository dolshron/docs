# Source: https://docs.nadapay.io/docs/upgrade-to-virtual-account

## 

Request

[Skip link to Request](https://docs.nadapay.io/docs/upgrade-to-virtual-account#request)

Bash

```
curl --request POST \
  --url $baseUrl/organizations/upgrade-virtual-account \
  --header 'x-api-key: YOUR_API_KEY' \
  --header 'Content-Type: application/json' \
  --header 'x-idempotency-key: YOUR_UNIQUE_UUID' \
  --data '{
    "currency": "USD"
  }'
```

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `currency` | string | Yes | Currency of the fiat wallet to upgrade |

## 

Response

[Skip link to Response](https://docs.nadapay.io/docs/upgrade-to-virtual-account#response)

Returns the provisioned virtual account details — account number and bank name.

## 

When to use this

[Skip link to When to use this](https://docs.nadapay.io/docs/upgrade-to-virtual-account#when-to-use-this)

Use this once, per currency, when you want that wallet to be able to receive direct bank transfers instead of relying only on [Get Deposit Instructions](https://docs.nadapay.io/docs/get-deposit-instructions) for one-off funding.

## 

Call this next

[Skip link to Call this next](https://docs.nadapay.io/docs/upgrade-to-virtual-account#call-this-next)

- [Get Deposit Instructions](https://docs.nadapay.io/docs/get-deposit-instructions)

Updated 2 months ago

---

Did this page help you?

Yes

No

Copy Page