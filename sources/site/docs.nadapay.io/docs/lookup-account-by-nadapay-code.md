# Source: https://docs.nadapay.io/docs/lookup-account-by-nadapay-code

## 

Request

[Skip link to Request](https://docs.nadapay.io/docs/lookup-account-by-nadapay-code#request)

Bash

```
curl --request GET \
  --url "$baseUrl/organizations/nadapay-code/{code}" \
  --header 'x-api-key: YOUR_API_KEY'
```

| Path param | Required | Description |
| --- | --- | --- |
| `code` | Yes | The Nadapay Code, e.g. `WAL-123` |

## 

Response

[Skip link to Response](https://docs.nadapay.io/docs/lookup-account-by-nadapay-code#response)

Returns the account information tied to that code.

## 

When to use this

[Skip link to When to use this](https://docs.nadapay.io/docs/lookup-account-by-nadapay-code#when-to-use-this)

Use this before executing a wallet-to-wallet transaction (see [Execute Transaction](https://docs.nadapay.io/docs/execute-transaction) in the Payments API) to confirm you're sending to the correct destination before you commit.

Updated 2 months ago

---

Did this page help you?

Yes

No

Copy Page