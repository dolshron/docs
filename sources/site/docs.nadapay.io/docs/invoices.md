# Source: https://docs.nadapay.io/docs/invoices

## 

Endpoints

[Skip link to Endpoints](https://docs.nadapay.io/docs/invoices#endpoints)

| Method | Path | Purpose |
| --- | --- | --- |
| `POST` | `/organization/invoices` | Create an invoice |
| `GET` | `/organization/invoices` | List invoices |
| `GET` | `/organization/invoices/:id` | Get invoice details |
| `PATCH` | `/organization/invoices/:id` | Update a draft invoice |
| `POST` | `/organization/invoices/:id/send` | Send an invoice to the customer |
| `DELETE` | `/organization/invoices/:id` | Delete a draft invoice |
| `GET` | `/public/invoices/:number` | Resolve invoice details publicly |
| `POST` | `/public/invoices/:number/session` | Create a checkout session for the invoice |

## 

Create an invoice

[Skip link to Create an invoice](https://docs.nadapay.io/docs/invoices#create-an-invoice)

Bash

```
curl --request POST \
  --url $baseUrl/organization/invoices \
  --header 'x-api-key: YOUR_API_KEY' \
  --header 'Content-Type: application/json' \
  --data '{
    "customerId": "customer-uuid",
    "number": "INV-001",
    "issueDate": "2026-04-24T00:00:00.000Z",
    "dueDate": "2026-05-24T00:00:00.000Z",
    "currency": "USD",
    "items": [
      { "description": "Web Design", "quantity": 2, "unitPrice": 500 }
    ],
    "taxRate": 8.25,
    "taxName": "Sales Tax",
    "settlementAccountId": "wallet-uuid",
    "paymentMethods": ["bank_transfer", "crypto"],
    "sendNow": false
  }'
```

| Field | Required | Description |
| --- | --- | --- |
| `customerId` | Yes | Must reference an existing [customer](https://docs.nadapay.io/docs/customers) |
| `number` | Yes | Invoice number |
| `issueDate`, `dueDate` | Yes | |
| `currency` | Yes | |
| `items` | Yes | Array of `{ description, quantity, unitPrice }` |
| `settlementAccountId` | Yes | Wallet the payment lands in |
| `paymentMethods` | Yes | e.g. `["bank_transfer", "crypto"]` |
| `taxRate`, `taxName` | No | |
| `discountValue`, `discountType` | No | `discountType`: `PERCENTAGE` or fixed |
| `allowPartialPayment` | No | |
| `sendNow` | No | If `true`, transitions to `SENT` immediately and emails the customer |
| `scheduledAt` | No | Schedule the send for later instead |

**Response:**

JSON

```
{
  "success": true,
  "statusCode": 201,
  "message": "Invoice created successfully",
  "data": {
    "id": "inv_abc123",
    "invoiceNumber": "INV-0001",
    "customerId": "cus_abc123",
    "total": 150000,
    "currency": "NGN",
    "status": "DRAFT",
    "dueDate": "2026-02-01T00:00:00Z",
    "createdAt": "2026-01-01T00:00:00Z"
  }
}
```

## 

Best practices

[Skip link to Best practices](https://docs.nadapay.io/docs/invoices#best-practices)

- Create the invoice first as a `DRAFT`, then send it once ready
- Only `DRAFT` invoices can be updated or deleted
- Use the invoice number as your customer-facing reference
- Only create a checkout session when the customer is actually ready to pay

## 

Call this next

[Skip link to Call this next](https://docs.nadapay.io/docs/invoices#call-this-next)

- Send the invoice via the `send` endpoint
- Customer opens `/public/invoices/:number` and creates a session to pay

Updated 2 months ago

---

Did this page help you?

Yes

No

Copy Page