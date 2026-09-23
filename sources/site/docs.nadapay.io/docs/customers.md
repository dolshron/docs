# Source: https://docs.nadapay.io/docs/customers

## 

Endpoints

[Skip link to Endpoints](https://docs.nadapay.io/docs/customers#endpoints)

| Method | Path | Purpose |
| --- | --- | --- |
| `POST` | `/organization/customers` | Create a customer |
| `GET` | `/organization/customers` | List customers |
| `GET` | `/organization/customers/:id` | Fetch a customer |
| `PATCH` | `/organization/customers/:id` | Update a customer |
| `DELETE` | `/organization/customers/:id` | Delete a customer |

## 

Create a customer

[Skip link to Create a customer](https://docs.nadapay.io/docs/customers#create-a-customer)

Bash

```
curl --request POST \
  --url $baseUrl/organization/customers \
  --header 'x-api-key: YOUR_API_KEY' \
  --header 'Content-Type: application/json' \
  --data '{
    "name": "Biffco Enterprise",
    "email": "biffco@enterprise.com",
    "phoneNumber": "+2348000000000",
    "address": "string",
    "metadata": {}
  }'
```

| Field | Required | Description |
| --- | --- | --- |
| `name` | Yes | Customer name |
| `email` | Yes | Must be unique per organization |
| `phoneNumber` | No | |
| `address` | No | |
| `metadata` | No | Arbitrary key-value data |

**Response:**

JSON

```
{
  "success": true,
  "statusCode": 201,
  "message": "Customer created successfully",
  "data": {
    "id": "cus_abc123",
    "name": "Acme Corp",
    "email": "billing@acme.com",
    "phone": "+2348000000000",
    "createdAt": "2026-01-01T00:00:00Z"
  }
}
```

> A `409` response means a customer with that email already exists — look them up instead of creating a duplicate.

## 

Best practices

[Skip link to Best practices](https://docs.nadapay.io/docs/customers#best-practices)

- Deduplicate by email where your business rules allow it
- Keep customer profile data current
- Don't store payment credentials in the customer record

## 

Call this next

[Skip link to Call this next](https://docs.nadapay.io/docs/customers#call-this-next)

- [Invoices](https://docs.nadapay.io/docs/invoices) — attach a customer to a receivable

Updated 2 months ago

---

Did this page help you?

Yes

No

Copy Page