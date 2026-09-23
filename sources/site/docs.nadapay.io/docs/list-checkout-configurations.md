# Source: https://docs.nadapay.io/docs/list-checkout-configurations

Request

Bash

```
curl --request GET \
  --url "$baseUrl/organization/checkout?page=1&limit=10&sortBy=createdAt&sortOrder=desc" \
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

[Skip link to Response](https://docs.nadapay.io/docs/list-checkout-configurations#response)

JSON

```
{
  "success": true,
  "statusCode": 200,
  "message": "Configurations retrieved successfully",
  "data": {
    "items": [
      {
        "id": "chk_01hw3x7k2r4p5q6m8n9v",
        "brandColor": "#7C3AED",
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

Use this to find the `id` of a configuration you want to reference elsewhere or pass to [Archive Checkout Configuration](https://docs.nadapay.io/docs/archive-checkout-configuration).

Updated 2 months ago

---

Did this page help you?

Yes

No

Copy Page