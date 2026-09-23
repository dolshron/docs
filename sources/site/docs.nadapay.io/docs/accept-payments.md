# Source: https://docs.nadapay.io/docs/accept-payments

# 

Accept Payments

[Skip link to Accept Payments](https://docs.nadapay.io/docs/accept-payments#accept-payments)

Create a checkout session when the customer clicks Pay, open NadaPay Checkout, and verify the payment before fulfilment.

**Time to complete:** 15 minutes

---

## 

Prerequisites

[Skip link to Prerequisites](https://docs.nadapay.io/docs/accept-payments#prerequisites)

> Create a backend endpoint that can create checkout sessions with your NadaPay secret key, and load the Checkout JavaScript SDK on your payment page.

---

## 

How it works

[Skip link to How it works](https://docs.nadapay.io/docs/accept-payments#how-it-works)

Your frontend never creates a checkout session directly. When the customer clicks Pay, your frontend asks your backend to create a session, then opens Checkout with the returned `np_reference_id`.

Text

```
Customer clicks Pay
  ↓
Frontend calls your backend
  ↓
Backend calls POST /checkout/sessions
  ↓
Frontend opens NadaPay Checkout
  ↓
Customer pays
  ↓
Backend verifies the session
  ↓
Order is fulfilled
```

---

## 

Step 1 - Load and initialize Checkout

[Skip link to Step 1 - Load and initialize Checkout](https://docs.nadapay.io/docs/accept-payments#step-1---load-and-initialize-checkout)

Load the Checkout SDK and call `NadaPay.init()` once when the page loads.

HTML

```
<script src="https://js.nadapay.io/v1/inline.js" async></script>
<script>
  window.addEventListener('load', function () {
    NadaPay.init({
      key: 'npk_test_xxxxxxxxxxxx',
      environment: 'sandbox',
      checkoutType: 'CUSTOM',
      currency: 'USD',

      onSuccess: function (result) {
        fetch('/api/orders/verify', {
          method: 'POST',
          headers: { 'Content-Type': 'application/json' },
          body: JSON.stringify({ reference: result.reference })
        });
      },

      onFailure: function (result) {
        console.log('Payment failed:', result.reason, result.message);
      },

      onClose: function () {
        console.log('Checkout closed');
      }
    });
  });
</script>
```

Use `npk_test_` public keys in sandbox and `npk_live_` public keys in production. Public keys are safe in browser code; secret keys are not.

---

## 

Step 2 - Create the session on Pay click

[Skip link to Step 2 - Create the session on Pay click](https://docs.nadapay.io/docs/accept-payments#step-2---create-the-session-on-pay-click)

Call your backend from the button click handler. Wait for the backend to return `np_reference_id`, then call `NadaPay.open()`.

HTML

```
<button id="pay-button">Pay $245.00</button>
<p id="status"></p>

<script>
  document.getElementById('pay-button').addEventListener('click', async function () {
    const response = await fetch('/api/checkout/session', {
      method: 'POST',
      headers: { 'Content-Type': 'application/json' },
      body: JSON.stringify({ orderId: 'ORD-4821' })
    });

    if (!response.ok) {
      document.getElementById('status').textContent = 'Could not start checkout.';
      return;
    }

    const session = await response.json();

    NadaPay.open({
      amount: session.amount,
      ref: session.np_reference_id,
      metadata: {
        order_id: 'ORD-4821'
      }
    });
  });
</script>
```

Save `np_reference_id`. You will verify it after the customer completes payment.

---

## 

Step 3 - Create the NadaPay checkout session on your backend

[Skip link to Step 3 - Create the NadaPay checkout session on your backend](https://docs.nadapay.io/docs/accept-payments#step-3---create-the-nadapay-checkout-session-on-your-backend)

Your backend calls NadaPay with your secret key. The authoritative amount comes from this backend session, not the frontend display amount.

JavaScript

```
app.post('/api/checkout/session', async function (req, res) {
  const { orderId } = req.body;
  const order = await getOrder(orderId);

  const response = await fetch('https://core.nadapay.io/v1/checkout/sessions', {
    method: 'POST',
    headers: {
      'Content-Type': 'application/json',
      'X-NadaPay-Secret-Key': process.env.NADAPAY_SECRET_KEY
    },
    body: JSON.stringify({
      merchant_id: 'your_merchant_id',
      amount_cents: order.amountCents,
      currency: 'USD',
      metadata: {
        order_id: order.id,
        customer_email: order.customerEmail
      }
    })
  });

  if (!response.ok) {
    return res.status(502).json({ message: 'Unable to create checkout session' });
  }

  const session = await response.json();

  res.json({
    np_reference_id: session.np_reference_id,
    amount: order.amount
  });
});
```

JSON

```
{
  "np_reference_id": "NP-P-CHECKOUT-4821-K9XZ",
  "amount": 245.00
}
```

Save `np_reference_id`; pass it to `NadaPay.open()` as `ref`.

---

## 

Step 4 - Verify the payment before fulfilment

[Skip link to Step 4 - Verify the payment before fulfilment](https://docs.nadapay.io/docs/accept-payments#step-4---verify-the-payment-before-fulfilment)

When `onSuccess` fires, verify the reference on your backend before shipping goods, unlocking content, or provisioning access.

JavaScript

```
app.post('/api/orders/verify', async function (req, res) {
  const { reference } = req.body;

  const response = await fetch(
    `https://core.nadapay.io/v1/checkout/sessions/${reference}`,
    {
      headers: {
        'X-NadaPay-Secret-Key': process.env.NADAPAY_SECRET_KEY
      }
    }
  );

  if (!response.ok) {
    return res.status(502).json({ message: 'Unable to verify payment' });
  }

  const session = await response.json();

  if (session.status !== 'PAID') {
    return res.status(400).json({ message: 'Payment is not complete' });
  }

  await fulfillOrder(session.metadata.order_id);

  res.json({ status: 'fulfilled' });
});
```

JSON

```
{
  "status": "fulfilled"
}
```

Fulfil the order only after your backend confirms the session status is `PAID`.

---

## 

What success looks like

[Skip link to What success looks like](https://docs.nadapay.io/docs/accept-payments#what-success-looks-like)

- Checkout opens only after your backend creates a session
- your frontend passes `np_reference_id` to `NadaPay.open()`
- your backend verifies the reference before fulfilment
- your production frontend uses an `npk_live_` public key
- your secret key never appears in browser code

---

## 

Troubleshooting

[Skip link to Troubleshooting](https://docs.nadapay.io/docs/accept-payments#troubleshooting)

### 

Checkout does not open

[Skip link to Checkout does not open](https://docs.nadapay.io/docs/accept-payments#checkout-does-not-open)

Confirm `NadaPay.init()` ran before `NadaPay.open()` and that `NadaPay.open()` is called from a direct user interaction, such as a button click.

### 

The amount looks wrong

[Skip link to The amount looks wrong](https://docs.nadapay.io/docs/accept-payments#the-amount-looks-wrong)

Use USD consistently. Send `$245.00` to the session API as `24500` cents and pass `245.00` to the frontend display amount.

### 

Payment succeeds in the browser but the order is not fulfilled

[Skip link to Payment succeeds in the browser but the order is not fulfilled](https://docs.nadapay.io/docs/accept-payments#payment-succeeds-in-the-browser-but-the-order-is-not-fulfilled)

Check your backend verification endpoint. The order should only be fulfilled after `GET /checkout/sessions/{reference}` confirms the session status is `PAID`.

---

## 

What's next

[Skip link to What's next](https://docs.nadapay.io/docs/accept-payments#whats-next)

| Next step | Why |
| --- | --- |
| [Collection Overview](https://docs.nadapay.io/docs/collection-overview) | Understand when to use Checkout versus deposit instructions. |
| [Get Deposit Instructions](https://docs.nadapay.io/docs/get-deposit-instructions) | Retrieve inbound funding instructions for account transfers. |
| [Handle Webhooks](https://docs.nadapay.io/docs/handle-webhooks) | Receive payment and transaction updates asynchronously. |

Updated 2 months ago

---

Did this page help you?

Yes

No

Copy Page