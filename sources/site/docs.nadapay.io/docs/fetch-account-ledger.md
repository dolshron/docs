# Source: https://docs.nadapay.io/docs/fetch-account-ledger

## 

Request

[Skip link to Request](https://docs.nadapay.io/docs/fetch-account-ledger#request)

Bash

```
curl --request GET \
  --url "$baseUrl/organizations/accounts/{accountId}/ledger?page=1&limit=10&sortBy=createdAt&sortOrder=desc" \
  --header 'x-api-key: YOUR_API_KEY'
```

| Query param | Default | Description |
| --- | --- | --- |
| `page` | `1` | Page number |
| `limit` | `10` | Results per page |
| `sortBy` | `createdAt` | Field to sort by |
| `sortOrder` | `desc` | `asc` or `desc` |

## 

Response

[Skip link to Response](https://docs.nadapay.io/docs/fetch-account-ledger#response)

Returns paginated ledger entries. Use this for reconciliation and dashboards — not for real-time settlement logic; rely on webhooks for that.

## 

Call this next

[Skip link to Call this next](https://docs.nadapay.io/docs/fetch-account-ledger#call-this-next)

- [Get Account Details](https://docs.nadapay.io/docs/get-account-details) to see the current balance this ledger rolls up to

Updated 2 months ago

---

Did this page help you?

Yes

No

Copy Page