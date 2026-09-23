# Source: https://docs.nadapay.io/docs/card-api-overview

## 

What's in this section

[Skip link to What's in this section](https://docs.nadapay.io/docs/card-api-overview#whats-in-this-section)

| Guide | Purpose |
| --- | --- |
| [Issue Card](https://docs.nadapay.io/docs/issue-card) | Create a new virtual card |
| [List Cards](https://docs.nadapay.io/docs/list-cards) | View all cards under your organization |
| [Get Card](https://docs.nadapay.io/docs/card-api-overview#get-card) | Fetch metadata for one card |
| [Get Secure Card Details](https://docs.nadapay.io/docs/get-secure-card-details) | Retrieve full PAN and CVV (server-only) |
| [Set Card PIN](https://docs.nadapay.io/docs/set-card-pin) | Set the PIN and activate a card |
| [Switch Card Account](https://docs.nadapay.io/docs/switch-card-account) | Reassign a card to a different wallet |

## 

Card lifecycle

[Skip link to Card lifecycle](https://docs.nadapay.io/docs/card-api-overview#card-lifecycle)

1. Issue the card — it starts `inactive`
2. Set a PIN — this activates the card
3. Use `Get Card` for safe display metadata; use `Get Secure Card Details` only when you need the full PAN/CVV
4. Optionally reassign the card to a different wallet later via Switch Card Account

## 

Security — read this first

[Skip link to Security — read this first](https://docs.nadapay.io/docs/card-api-overview#security--read-this-first)

- `Get Secure Card Details` returns the full PAN and CVV. **Call it only from a secure backend, and never log the response.**
- `Get Card` is the safe endpoint for anything customer- or dashboard-facing — it never exposes PAN or CVV.
- PINs must be a 4-digit numeric value and should be collected and transmitted only through a tightly scoped, PCI-aware flow on your frontend.

Updated 2 months ago

---

Did this page help you?

Yes

No

Copy Page