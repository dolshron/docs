# Source: https://docs.nadapay.io/docs/get-account-details

## 

Request

[Skip link to Request](https://docs.nadapay.io/docs/get-account-details#request)

Bash

```
curl --request GET \
  --url "$baseUrl/organizations/accounts/{accountId}" \
  --header 'x-api-key: YOUR_API_KEY'
```

| Path param | Required | Description |
| --- | --- | --- |
| `accountId` | Yes | The wallet ID |

## 

Response

[Skip link to Response](https://docs.nadapay.io/docs/get-account-details#response)

JSON

```
{
  "id": "acc-uuid-123",
  "name": "Main Wallet",
  "currency": "USD",
  "walletStatus": "ACTIVE"
}
```

## 

Call this next

[Skip link to Call this next](https://docs.nadapay.io/docs/get-account-details#call-this-next)

- [Fetch Account Ledger](https://docs.nadapay.io/docs/fetch-account-ledger) to see the transaction history behind this balance

Updated 2 months ago

---

Did this page help you?

Yes

No

Copy Page