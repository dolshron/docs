# Source: https://docs.nadapay.io/docs/set-card-pin

## 

Request

[Skip link to Request](https://docs.nadapay.io/docs/set-card-pin#request)

Bash

```
curl --request POST \
  --url "$baseUrl/organization/cards/{id}/pin" \
  --header 'x-api-key: YOUR_API_KEY' \
  --header 'Content-Type: application/json' \
  --data '{
    "pin": "1234"
  }'
```

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `pin` | string | Yes | 4-digit numeric PIN |

## 

Response

[Skip link to Response](https://docs.nadapay.io/docs/set-card-pin#response)

JSON

```
{
  "success": true,
  "statusCode": 200,
  "message": "Card PIN set and activated",
  "data": {
    "id": "card_01hw3x7k2r4p5q6m8n9v",
    "status": "active"
  }
}
```

A card cannot be used for transactions until its PIN is set — this call moves the card's status from `inactive` to `active`.

## 

Security note

[Skip link to Security note](https://docs.nadapay.io/docs/set-card-pin#security-note)

Collect the PIN through a tightly scoped input on your frontend and send it straight to this endpoint — don't store it, log it, or pass it through any intermediate service that doesn't need it.

Updated 2 months ago

---

Did this page help you?

Yes

No

Copy Page