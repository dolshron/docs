# Source: https://docs.nadapay.io/docs/configure-checkout-widget

## 

Request

[Skip link to Request](https://docs.nadapay.io/docs/configure-checkout-widget#request)

Bash

```
curl --request POST \
  --url $baseUrl/organization/checkout/configure \
  --header 'x-api-key: YOUR_API_KEY' \
  --header 'Content-Type: application/json' \
  --data '{
    "name": "Web Checkout Widget",
    "settlementAccountId": "wallet-uuid",
    "checkoutType": "CUSTOM",
    "allowedDomains": ["https://yourapp.com"],
    "branding": {},
    "returnUrl": "https://example.com/checkout/return",
    "successUrl": "https://example.com/checkout/success",
    "enabledFiatCurrencies": ["USD", "NGN"],
    "enabledCryptoCurrencies": ["USDC", "SOL"],
    "enabledPaymentMethods": ["crypto", "bank_transfer"]
  }'
```

| Field | Required | Description |
| --- | --- | --- |
| `name` | Yes | Configuration name |
| `settlementAccountId` | Yes | Wallet where funds settle |
| `checkoutType` | Yes | `PRODUCT` or `CUSTOM` |
| `productIds` | If `checkoutType` is `PRODUCT` | Products this checkout sells |
| `allowedDomains` | No | Domains permitted to embed this checkout — validated against the `Origin` header |
| `branding` | No | Logo, colors, etc. |
| `returnUrl` / `successUrl` | No | Where to send the customer after payment |
| `enabledFiatCurrencies` | No | e.g. `["USD", "NGN"]` |
| `enabledCryptoCurrencies` | No | e.g. `["USDC", "SOL"]` |
| `enabledPaymentMethods` | No | Any of `crypto`, `nadapay_wallet`, `card`, `bank_transfer` |

## 

Response

[Skip link to Response](https://docs.nadapay.io/docs/configure-checkout-widget#response)

JSON

```
{
  "success": true,
  "statusCode": 200,
  "message": "Checkout configured successfully",
  "data": {
    "id": "chk_01hw3x7k2r4p5q6m8n9v",
    "brandColor": "#7C3AED",
    "logoUrl": "https://cdn.example.com/logo.png",
    "redirectUrl": "https://app.example.com/payment/success",
    "allowedChannels": ["card", "bank_transfer"],
    "environment": "live",
    "updatedAt": "2024-07-01T10:00:00.000Z"
  }
}
```

## 

Frontend integration notes

[Skip link to Frontend integration notes](https://docs.nadapay.io/docs/configure-checkout-widget#frontend-integration-notes)

- Read `enabledPaymentMethods` from this configuration at render time — don't hardcode payment options in your UI
- Send a valid `Origin` header on any browser-facing request against this config so `allowedDomains` validation succeeds

## 

Call this next

[Skip link to Call this next](https://docs.nadapay.io/docs/configure-checkout-widget#call-this-next)

- [List Checkout Configurations](https://docs.nadapay.io/docs/list-checkout-configurations)

Updated 2 months ago

---

Did this page help you?

Yes

No

Copy Page