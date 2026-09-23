# Source: https://docs.nadapay.io/docs/get-supported-networks

> **Note:** this endpoint is primarily used just before creating a beneficiary account — you may see it referenced in Payout API guides as well.

## 

Request

[Skip link to Request](https://docs.nadapay.io/docs/get-supported-networks#request)

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

## 

Response

[Skip link to Response](https://docs.nadapay.io/docs/get-supported-networks#response)

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

Use the returned network `code` in the `details` object when adding a beneficiary account.

> **Network availability varies by corridor.** Always fetch this dynamically rather than hardcoding network options in your UI.

## 

Call this next

[Skip link to Call this next](https://docs.nadapay.io/docs/get-supported-networks#call-this-next)

- Add a beneficiary account _(Payout API)_
- [Resolve a Bank Account](https://docs.nadapay.io/docs/resolve-a-bank-account) _(Payout API)_

Updated 2 months ago

---

Did this page help you?

Yes

No

Copy Page