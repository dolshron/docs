# Source: https://docs.nadapay.io/docs/payment-api

Everything needed to send money out to a beneficiary — from registering the destination through executing single or batch payouts.

## 

What's in this section

[Skip link to What's in this section](https://docs.nadapay.io/docs/payment-api#whats-in-this-section)

| Guide | Purpose |
| --- | --- |
| [Get Available Markets](https://docs.nadapay.io/docs/get-available-markets) | Check which currency corridors are currently active, across all providers |
| [Create a Beneficiary](https://docs.nadapay.io/docs/create-beneficiary) | Register a payout destination and attach an account |
| [Resolve a Bank Account](https://docs.nadapay.io/docs/resolve-bank-account) | Verify the account holder name before adding a bank-based beneficiary |
| [Batch Payout Execution](https://docs.nadapay.io/docs/batch-payout-execution) | Execute multiple payouts from one source in a single request |

## 

The payout flow

[Skip link to The payout flow](https://docs.nadapay.io/docs/payment-api#the-payout-flow)

```
Get Available Markets   ← confirm the corridor is active
        ↓
Get Supported Networks (Payments API)
        ↓
Resolve a Bank Account   ← required for bank-based rails
        ↓
Create a Beneficiary
        ↓
Add a Beneficiary Account
        ↓
Check Transaction Limits (Payments API)
        ↓
Generate Quote (Payments API)
        ↓
Execute Transaction — or Batch Payout Execution for multiple payouts
        ↓
Webhook confirms final state
```

> **Always resolve before adding.** Never skip [Resolve a Bank Account](https://docs.nadapay.io/docs/resolve-a-bank-account) for bank-based payouts — it's the step that catches misdirected transfers before money moves.

Updated 2 months ago

---

Did this page help you?

Yes

No

Copy Page