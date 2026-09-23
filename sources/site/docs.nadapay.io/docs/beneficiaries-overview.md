# Source: https://docs.nadapay.io/docs/beneficiaries-overview

# 

Beneficiaries Overview

[Skip link to Beneficiaries Overview](https://docs.nadapay.io/docs/beneficiaries-overview#beneficiaries-overview)

Understand beneficiaries, beneficiary accounts, supported destination types, and why bank accounts should be resolved before use.

---

## 

Prerequisites

[Skip link to Prerequisites](https://docs.nadapay.io/docs/beneficiaries-overview#prerequisites)

> Choose the payout country and rail before you create or attach a beneficiary account.

---

## 

Overview

[Skip link to Overview](https://docs.nadapay.io/docs/beneficiaries-overview#overview)

A beneficiary is a reusable recipient profile. A beneficiary account is the specific destination attached to that profile, such as a bank account, mobile money wallet, or crypto address.

Text

```
Beneficiary
└── Beneficiary Account
```

Create the beneficiary once, then attach one or more destination accounts that can be reused in future payout flows.

---

## 

Supported destination types

[Skip link to Supported destination types](https://docs.nadapay.io/docs/beneficiaries-overview#supported-destination-types)

| Type | Use it for | Common fields |
| --- | --- | --- |
| Bank | Bank transfers and ACH-style rails | `accountNumber`, `accountName`, `networkId`, `country` |
| Mobile money | Mobile wallet payouts | `phoneNumber`, `provider`, `country`, `networkId` |
| Crypto | Wallet-address payouts | `chain`, `address` |

---

## 

Resolve before you create

[Skip link to Resolve before you create](https://docs.nadapay.io/docs/beneficiaries-overview#resolve-before-you-create)

For bank-based payouts, resolve the bank account before you attach it to a beneficiary. Resolution confirms the account holder name and reduces the risk of misdirected payouts.

Text

```
Get networks → Resolve bank account → Create beneficiary → Add beneficiary account
```

---

## 

What success looks like

[Skip link to What success looks like](https://docs.nadapay.io/docs/beneficiaries-overview#what-success-looks-like)

- you know the difference between a beneficiary and a beneficiary account
- you know which destination fields apply to each payout type
- you resolve bank accounts before attaching them to a beneficiary

---

## 

Troubleshooting

[Skip link to Troubleshooting](https://docs.nadapay.io/docs/beneficiaries-overview#troubleshooting)

### 

The network ID is invalid

[Skip link to The network ID is invalid](https://docs.nadapay.io/docs/beneficiaries-overview#the-network-id-is-invalid)

Fetch provider networks for the destination country and use the returned `networkId` instead of hardcoding bank or provider identifiers.

### 

The resolved name does not match the recipient

[Skip link to The resolved name does not match the recipient](https://docs.nadapay.io/docs/beneficiaries-overview#the-resolved-name-does-not-match-the-recipient)

Do not continue. Ask the customer or operations team to confirm the account details before creating the beneficiary account.

---

## 

What's next

[Skip link to What's next](https://docs.nadapay.io/docs/beneficiaries-overview#whats-next)

| Next step | Why |
| --- | --- |
| [Get Provider Networks](https://docs.nadapay.io/docs/get-provider-networks) | Select the correct payout network for the country. |
| [Resolve a Bank Account](https://docs.nadapay.io/docs/resolve-bank-account) | Validate bank account details before attaching them. |
| [Create a Beneficiary](https://docs.nadapay.io/docs/create-beneficiary) | Create the recipient and attach a payout destination. |

Updated 2 months ago

---

Did this page help you?

Yes

No

Copy Page