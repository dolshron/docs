# Source: https://docs.nadapay.io/docs/archive-checkout-configuration

> **This cannot be undone.** Archiving disables any active hosted checkout sessions currently using this configuration.

## 

Request

[Skip link to Request](https://docs.nadapay.io/docs/archive-checkout-configuration#request)

Bash

```
curl --request DELETE \
  --url "$baseUrl/organization/checkout/{id}" \
  --header 'x-api-key: YOUR_API_KEY'
```

## 

Response

[Skip link to Response](https://docs.nadapay.io/docs/archive-checkout-configuration#response)

JSON

```
{
  "success": true,
  "statusCode": 200,
  "message": "Configuration archived successfully",
  "data": null
}
```

## 

Before you archive

[Skip link to Before you archive](https://docs.nadapay.io/docs/archive-checkout-configuration#before-you-archive)

Confirm no live integrations are still referencing this configuration's `id` — any in-progress checkout session tied to it will stop working immediately.

Updated 2 months ago

---

Did this page help you?

Yes

No

Copy Page