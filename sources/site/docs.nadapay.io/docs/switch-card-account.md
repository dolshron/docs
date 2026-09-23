# Source: https://docs.nadapay.io/docs/switch-card-account

## 

Request

[Skip link to Request](https://docs.nadapay.io/docs/switch-card-account#request)

Bash

```
curl --request PATCH \
  --url "$baseUrl/organization/cards/{id}/account" \
  --header 'x-api-key: YOUR_API_KEY' \
  --header 'Content-Type: application/json' \
  --data '{
    "nadapayCode": "NP-0002"
  }'
```

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `nadapayCode` | string | Yes | The new wallet to tie the card to |

## 

Response

[Skip link to Response](https://docs.nadapay.io/docs/switch-card-account#response)

JSON

```
{
  "success": true,
  "statusCode": 200,
  "message": "Card account switched successfully",
  "data": {
    "id": "card_01hw3x7k2r4p5q6m8n9v",
    "nadapayCode": "NP-0002"
  }
}
```

## 

When to use this

[Skip link to When to use this](https://docs.nadapay.io/docs/switch-card-account#when-to-use-this)

Use this when a card needs to draw from a different wallet going forward — for example, moving a card from one sub-organization's account to another. The card itself (number, PIN, status) doesn't change; only which wallet it debits.

Updated 2 months ago

---

Did this page help you?

Yes

No

Copy Page