# Source: https://docs.nadapay.io/docs/products

## 

Endpoints

[Skip link to Endpoints](https://docs.nadapay.io/docs/products#endpoints)

| Method | Path | Purpose |
| --- | --- | --- |
| `POST` | `/organization/products` | Create a product |
| `GET` | `/organization/products` | List products |
| `GET` | `/organization/products/:id` | Fetch a product |
| `PATCH` | `/organization/products/:id` | Update a product |
| `DELETE` | `/organization/products/:id` | Archive a product |

## 

Create a product

[Skip link to Create a product](https://docs.nadapay.io/docs/products#create-a-product)

Bash

```
curl --request POST \
  --url $baseUrl/organization/products \
  --header 'x-api-key: YOUR_API_KEY' \
  --header 'Content-Type: application/json' \
  --data '{
    "name": "Premium Plan",
    "description": "string",
    "sku": "string",
    "type": "RECURRING",
    "price": 120,
    "currency": "USD",
    "billingPeriod": "monthly",
    "status": "ACTIVE"
  }'
```

| Field | Required | Description |
| --- | --- | --- |
| `name` | Yes | Product name |
| `type` | Yes | `RECURRING` or `ONE_TIME` |
| `price` | Yes | Price in whole units (converted internally) |
| `currency` | Yes | e.g. `USD` |
| `billingPeriod` | If `RECURRING` | e.g. `monthly` |
| `sku`, `description`, `image` | No | |
| `status` | No | `ACTIVE`, `ARCHIVED`, or `DRAFT` — defaults to `ACTIVE` |

**Response:**

JSON

```
{
  "success": true,
  "statusCode": 201,
  "message": "Product created successfully",
  "data": {
    "id": "prod_01hw3x7k2r4p5q6m8n9v",
    "name": "Annual Subscription",
    "description": "Access to all premium features for 12 months.",
    "currency": "NGN",
    "price": 120000,
    "isActive": true,
    "environment": "live",
    "createdAt": "2024-07-01T10:00:00.000Z"
  }
}
```

## 

Best practices

[Skip link to Best practices](https://docs.nadapay.io/docs/products#best-practices)

- Keep product identifiers stable once referenced by invoices or payment links
- **Archive, don't delete**, once a product has historical usage — this preserves past transaction records
- Use products as the source of truth for recurring billing metadata

## 

Call this next

[Skip link to Call this next](https://docs.nadapay.io/docs/products#call-this-next)

- [Payment Links](https://docs.nadapay.io/docs/payment-links) _(Payments API)_ — attach a product via `checkoutType: PRODUCT`
- [Invoices](https://docs.nadapay.io/docs/invoices)

Updated 2 months ago

---

Did this page help you?

Yes

No

Copy Page