# Source: https://docs.nadapay.io/docs/collection-overview

# 

Collection Overview

[Skip link to Collection Overview](https://docs.nadapay.io/docs/collection-overview#collection-overview)

Understand the inbound payment options NadaPay supports and when to use Checkout, payment links, or deposit instructions.

---

## 

Prerequisites

[Skip link to Prerequisites](https://docs.nadapay.io/docs/collection-overview#prerequisites)

> Decide whether the payer should complete a hosted checkout flow or send funds using account funding instructions.

---

## 

Overview

[Skip link to Overview](https://docs.nadapay.io/docs/collection-overview#overview)

Collection covers inbound money movement into NadaPay-powered flows. Use Checkout when a customer needs to pay from a product, invoice, donation, or booking page. Use deposit instructions when a payer or operations team needs funding details for a bank or wallet transfer.

Text

```
Checkout / Payment Link → Customer pays in hosted flow
Deposit Instructions → Payer sends funds using provided account details
```

---

## 

Collection methods

[Skip link to Collection methods](https://docs.nadapay.io/docs/collection-overview#collection-methods)

| Method | Use it when | Guide |
| --- | --- | --- |
| Checkout | You control a Pay button or embedded payment flow in your application. | [Accept Payments](https://docs.nadapay.io/docs/accept-payments) |
| Payment links | You want to send a hosted payment URL outside your app. | [Accept Payments](https://docs.nadapay.io/docs/accept-payments) |
| Deposit instructions | You need funding details for a bank or wallet transfer. | [Get Deposit Instructions](https://docs.nadapay.io/docs/get-deposit-instructions) |

---

## 

What success looks like

[Skip link to What success looks like](https://docs.nadapay.io/docs/collection-overview#what-success-looks-like)

- you know when to use Checkout instead of deposit instructions
- you know where payment verification happens
- you know which guide to follow for your collection flow

---

## 

Troubleshooting

[Skip link to Troubleshooting](https://docs.nadapay.io/docs/collection-overview#troubleshooting)

### 

You need a customer-facing payment flow

[Skip link to You need a customer-facing payment flow](https://docs.nadapay.io/docs/collection-overview#you-need-a-customer-facing-payment-flow)

Use Checkout through [Accept Payments](https://docs.nadapay.io/docs/accept-payments). Create the session on your backend when the customer clicks Pay.

### 

You need funding instructions for an account

[Skip link to You need funding instructions for an account](https://docs.nadapay.io/docs/collection-overview#you-need-funding-instructions-for-an-account)

Use [Get Deposit Instructions](https://docs.nadapay.io/docs/get-deposit-instructions) and share the returned instructions with the funding party.

---

## 

What's next

[Skip link to What's next](https://docs.nadapay.io/docs/collection-overview#whats-next)

| Next step | Why |
| --- | --- |
| [Accept Payments](https://docs.nadapay.io/docs/accept-payments) | Build a Checkout-based payment flow. |
| [Get Deposit Instructions](https://docs.nadapay.io/docs/get-deposit-instructions) | Retrieve funding details for inbound transfers. |
| [Handle Webhooks](https://docs.nadapay.io/docs/handle-webhooks) | Receive real-time updates after payment events. |

Updated 2 months ago

---

Did this page help you?

Yes

No

Copy Page