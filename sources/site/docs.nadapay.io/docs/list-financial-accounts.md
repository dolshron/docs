# Source: https://docs.nadapay.io/docs/list-financial-accounts

## 

Request

[Skip link to Request](https://docs.nadapay.io/docs/list-financial-accounts#request)

Bash

```
curl --request GET \
  --url "$baseUrl/organizations/accounts?status=ACTIVE&currency=USD" \
  --header 'x-api-key: YOUR_API_KEY'
```

| Query param | Required | Description |
| --- | --- | --- |
| `status` | No | Filter by account status, e.g. `ACTIVE` |
| `currency` | No | Filter by currency, e.g. `USD` |

## 

Response

[Skip link to Response](https://docs.nadapay.io/docs/list-financial-accounts#response)

JSON

```
[
  {
    "id": "acc-uuid-123",
    "name": "Main Wallet",
    "currency": "USD",
    "walletStatus": "ACTIVE"
  }
]
```

## 

Call this next

[Skip link to Call this next](https://docs.nadapay.io/docs/list-financial-accounts#call-this-next)

- [Get Account Details](https://docs.nadapay.io/docs/get-account-details) for full details on one wallet
- [Get Currency Balance](https://docs.nadapay.io/docs/get-currency-balance) for a quick balance check

Updated 2 months ago

---

Did this page help you?

Yes

No

Copy Page