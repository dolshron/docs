# Source: https://docs.nadapay.io/docs/get-secure-card-details

> **Security-critical endpoint.** Call this only from a secure server environment. Never log the response, never return it to a browser or mobile client directly, and never persist the PAN/CVV in your own systems.

## 

Request

[Skip link to Request](https://docs.nadapay.io/docs/get-secure-card-details#request)

Bash

```
curl --request GET \
  --url "$baseUrl/organization/cards/{id}/details" \
  --header 'x-api-key: YOUR_API_KEY'
```

## 

Response

[Skip link to Response](https://docs.nadapay.io/docs/get-secure-card-details#response)

JSON

```
{
  "success": true,
  "statusCode": 200,
  "message": "Secure details retrieved",
  "data": {
    "pan": "4000000000004242",
    "cvv": "123"
  }
}
```

## 

When to use this

[Skip link to When to use this](https://docs.nadapay.io/docs/get-secure-card-details#when-to-use-this)

Only when you have a specific, secure need for the full card number — e.g., displaying it once inside a PCI-compliant iframe for the cardholder to view. For everything else (listing, status checks, dashboards), use [Get Card](https://docs.nadapay.io/docs/get-card) instead.

Updated 2 months ago

---

Did this page help you?

Yes

No

Copy Page