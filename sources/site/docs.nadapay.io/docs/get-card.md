# Source: https://docs.nadapay.io/docs/get-card

## 

Request

[Skip link to Request](https://docs.nadapay.io/docs/get-card#request)

Bash

```
curl --request GET \
  --url "$baseUrl/organization/cards/{id}" \
  --header 'x-api-key: YOUR_API_KEY'
```

## 

Response

[Skip link to Response](https://docs.nadapay.io/docs/get-card#response)

JSON

```
{
  "success": true,
  "statusCode": 200,
  "message": "Card metadata retrieved",
  "data": {
    "id": "card_01hw3x7k2r4p5q6m8n9v",
    "last4": "4242",
    "status": "active",
    "nadapayCode": "NP-0001"
  }
}
```

Use this endpoint for anything customer-facing or displayed on a dashboard — it's safe to log and render directly.

Updated 2 months ago

---

Did this page help you?

Yes

No

Copy Page