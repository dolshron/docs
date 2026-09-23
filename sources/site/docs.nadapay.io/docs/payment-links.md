# Source: https://docs.nadapay.io/docs/payment-links

## 

Endpoints

[Skip link to Endpoints](https://docs.nadapay.io/docs/payment-links#endpoints)

| Method | Path | Purpose |
| --- | --- | --- |
| `POST` | `/organization/payment-links` | Create a payment link |
| `GET` | `/organization/payment-links` | List payment links |
| `GET` | `/organization/payment-links/:id` | Get payment link details |
| `PATCH` | `/organization/payment-links/:id` | Update a payment link |
| `DELETE` | `/organization/payment-links/:id` | Archive a payment link |
| `POST` | `/organization/payment-links/:id/share` | Share a link via email |
| `GET` | `/organization/payment-links/shares/history` | View share history |

## 

Create a payment link

[Skip link to Create a payment link](https://docs.nadapay.io/docs/payment-links#create-a-payment-link)

Bash

```
curl --request POST \
  --url $baseUrl/organization/payment-links \
  --header 'x-api-key: YOUR_API_KEY' \
  --header 'Content-Type: application/json' \
  --data '{
    "name": "Consultation Fee",
    "checkoutType": "CUSTOM",
    "amount": 5000,
    "currency": "USD",
    "isVariableAmount": false,
    "settlementAccountId": "string",
    "collectAddress": false,
    "collectPhoneNumber": false,
    "redirectUrl": "https://yoursite.com/thank-you",
    "successMessage": "Thanks for your payment!"
  }'
```

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | Yes | Internal/display name for the link |
| `checkoutType` | `PRODUCT` | `CUSTOM` | Yes | Whether the link is tied to a product or a custom amount |
| `productId` | string | If `checkoutType` is `PRODUCT` | Product to bill against |
| `amount` | number | No | Fixed amount — leave empty for variable amount |
| `currency` | string | Yes | e.g. `USD` |
| `isVariableAmount` | boolean | Yes | Let the customer enter their own amount |
| `settlementAccountId` | string | Yes | Wallet the funds land in |
| `collectAddress` | boolean | No | Collect a shipping/billing address |
| `collectPhoneNumber` | boolean | No | Collect a phone number |
| `customFieldLabel` | string | No | Add a custom field, e.g. "Invoice Number" |
| `redirectUrl` | string | No | Where to send the customer after payment |
| `successMessage` | string | No | Message shown on the success screen |
| `expiresAt` | string | No | Expiry timestamp |

## 

Response

[Skip link to Response](https://docs.nadapay.io/docs/payment-links#response)

JSON

```
{
  "success": true,
  "statusCode": 201,
  "message": "Payment link created successfully",
  "data": {
    "id": "pl_abc123",
    "slug": "monthly-subscription",
    "url": "https://pay.nadapay.io/monthly-subscription",
    "amount": 5000,
    "currency": "USD",
    "isActive": true,
    "createdAt": "2026-01-01T00:00:00Z"
  }
}
```

The `url` field is the shareable link — hand this directly to your customer.

## 

Best practices

[Skip link to Best practices](https://docs.nadapay.io/docs/payment-links#best-practices)

- Keep the link stable once shared; avoid recreating links for the same purpose
- Use `share` and the share history endpoint for audit and customer-support visibility
- Archive rather than delete once a link is no longer needed — archived links stop accepting payments but preserve history

## 

Call this next

[Skip link to Call this next](https://docs.nadapay.io/docs/payment-links#call-this-next)

- Share the link via email using the share endpoint
- Track completed payments through your webhook handler

Updated 2 months ago

---

Did this page help you?

Yes

No

Copy Page