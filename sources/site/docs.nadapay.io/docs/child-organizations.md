# Source: https://docs.nadapay.io/docs/child-organizations

## 

Register a child organization

[Skip link to Register a child organization](https://docs.nadapay.io/docs/child-organizations#register-a-child-organization)

Bash

```
curl --request POST \
  --url $baseUrl/organizations/children \
  --header 'x-api-key: YOUR_API_KEY' \
  --header 'Content-Type: application/json' \
  --header 'x-idempotency-key: YOUR_UNIQUE_UUID' \
  --data '{
    "businessName": "Acme Corp",
    "businessType": "Technology",
    "businessEmail": "info@acmecorp.com",
    "phoneNumber": "+1234567890",
    "address": "123 Main St",
    "country": "USA",
    "city": "New York",
    "state": "NY",
    "firstname": "Jane",
    "lastname": "Doe",
    "website": "https://www.acmecorp.com"
  }'
```

| Field | Required | Description |
| --- | --- | --- |
| `businessName` | Yes | Legal or trading name |
| `businessType` | Yes | e.g. `Technology` |
| `businessEmail` | Yes | Primary business email |
| `phoneNumber` | Yes | Business phone number |
| `address`, `country`, `city`, `state` | Yes | Business location |
| `firstname`, `lastname` | Yes | Primary contact person |
| `website` | No | Business website |

This creates both the child organization and its associated owner user account.

**Response:**

JSON

```
{
  "userId": "user-uuid-123",
  "organizationId": "org-uuid-456"
}
```

## 

List child organizations

[Skip link to List child organizations](https://docs.nadapay.io/docs/child-organizations#list-child-organizations)

Bash

```
curl --request GET \
  --url $baseUrl/organizations/children \
  --header 'x-api-key: YOUR_API_KEY'
```

Returns all sub-businesses managed under the authenticated partner organization.

## 

Call this next

[Skip link to Call this next](https://docs.nadapay.io/docs/child-organizations#call-this-next)

- [Verification Status](https://docs.nadapay.io/docs/verification-status) — each child organization goes through its own KYB

Updated 2 months ago

---

Did this page help you?

Yes

No

Copy Page