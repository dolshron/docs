# Source: https://docs.nadapay.io/docs/list-cards

## 

Request

[Skip link to Request](https://docs.nadapay.io/docs/list-cards#request)

Bash

```
curl --request GET \
  --url "$baseUrl/organization/cards?page=1&limit=10&sortBy=createdAt&sortOrder=desc" \
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

[Skip link to Response](https://docs.nadapay.io/docs/list-cards#response)

JSON

```
{
  "success": true,
  "statusCode": 200,
  "message": "Cards retrieved",
  "data": {
    "items": [
      {
        "id": "card_01hw3x7k2r4p5q6m8n9v",
        "last4": "4242",
        "status": "active",
        "nadapayCode": "NP-0001",
        "environment": "live",
        "createdAt": "2024-07-01T10:00:00.000Z"
      }
    ],
    "total": 1,
    "page": 1,
    "limit": 20
  }
}
```

This endpoint returns metadata only — no PAN or CVV. Use [Get Secure Card Details](https://docs.nadapay.io/docs/get-secure-card-details) if you need full card numbers.

Updated 2 months ago

---

Did this page help you?

Yes

No

Copy Page