# Source: https://docs.nadapay.io/docs/issue-card

Issue a new corporate virtual card linked to a NadaPay wallet.

## 

Request

[Skip link to Request](https://docs.nadapay.io/docs/issue-card#request)

Bash

```
curl --request POST \
  --url $baseUrl/organization/cards \
  --header 'x-api-key: YOUR_API_KEY' \
  --header 'Content-Type: application/json' \
  --data '{
    "nadapayCode": "NP-0001",
    "limit": 500000
  }'
```

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `nadapayCode` | string | Yes | The wallet this card is tied to |
| `limit` | number | No | Spending limit, in cents |

## 

Response

[Skip link to Response](https://docs.nadapay.io/docs/issue-card#response)

JSON

```
{
  "success": true,
  "statusCode": 201,
  "message": "Card issued successfully",
  "data": {
    "id": "card_01hw3x7k2r4p5q6m8n9v",
    "last4": "4242",
    "status": "inactive",
    "nadapayCode": "NP-0001",
    "environment": "live",
    "createdAt": "2024-07-01T10:00:00.000Z"
  }
}
```

A newly issued card starts in `inactive` status.

## 

Call this next

[Skip link to Call this next](https://docs.nadapay.io/docs/issue-card#call-this-next)

- [Set Card PIN](https://docs.nadapay.io/docs/set-card-pin) — required to activate the card before it can be used

Updated 2 months ago

---

Did this page help you?

Yes

No

Copy Page