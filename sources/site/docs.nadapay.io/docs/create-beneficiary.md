# Source: https://docs.nadapay.io/docs/create-beneficiary

Create a beneficiary and attach a payout account so you can reuse the destination in future transactions.

**Time to complete:** 5 minutes

## 

When to use this page

[Skip link to When to use this page](https://docs.nadapay.io/docs/create-beneficiary#when-to-use-this-page)

Use this page when you need to register a reusable payout destination before you generate a quote or execute a transaction.

## 

Prerequisites

[Skip link to Prerequisites](https://docs.nadapay.io/docs/create-beneficiary#prerequisites)

1. Set your NadaPay API base URL in `$baseUrl`.
2. Export your NadaPay API key as `YOUR_API_KEY`.
3. Generate a unique idempotency key for each create request.

## 

Before you continue

[Skip link to Before you continue](https://docs.nadapay.io/docs/create-beneficiary#before-you-continue)

- decide the payout rail you want to use
- resolve the destination bank account first if the rail is bank-based
- confirm the organization is ready to move beyond onboarding for the intended mode

## 

Step 1 - Create the beneficiary

[Skip link to Step 1 - Create the beneficiary](https://docs.nadapay.io/docs/create-beneficiary#step-1---create-the-beneficiary)

Bash

```
curl --request POST \
  --url $baseUrl/beneficiaries \
  --header 'x-api-key: YOUR_API_KEY' \
  --header 'Content-Type: application/json' \
  --header 'x-idempotency-key: YOUR_UNIQUE_UUID' \
  --data '{
    "name": "string",
    "email": "string",
    "phone": "string",
    "currency": "USD",
    "type": "INTERNAL",
    "details": {
      "nadapayCode": "string",
      "accountNumber": "string",
      "accountName": "string",
      "networkId": "string",
      "rail": "ACH",
      "bankCode": "string",
      "country": "NG",
      "iban": "string",
      "swiftCode": "string",
      "sortCode": "string",
      "routingNumber": "string",
      "clabe": "string",
      "pixKey": "string",
      "cpf": "string",
      "chain": "ETHEREUM",
      "address": "string",
      "legalName": "string",
      "accountType": "personal",
      "phoneNumber": "string",
      "provider": "string",
      "streetLine1": "string",
      "city": "string",
      "state": "string",
      "postalCode": "string"
    }
  }'
```

Use the fields inside `details` that apply to the rail you are registering.

## 

Start with these values for the recommended bank-transfer flow

[Skip link to Start with these values for the recommended bank-transfer flow](https://docs.nadapay.io/docs/create-beneficiary#start-with-these-values-for-the-recommended-bank-transfer-flow)

For the fastest first integration, set these values in the example below before you customize anything else:

- `name`
- `currency`
- `type`
- `details.rail`
- `details.accountNumber`
- `details.accountName`
- `details.networkId`
- `details.country`

### 

`details` by rail

[Skip link to \[object Object\], by rail](https://docs.nadapay.io/docs/create-beneficiary#details-by-rail)

#### 

ACH

[Skip link to ACH](https://docs.nadapay.io/docs/create-beneficiary#ach)

| Field | Required | Notes |
| --- | --- | --- |
| `accountNumber` | Yes | Recipient bank account number |
| `accountName` | Yes | Recipient account name |
| `routingNumber` | Yes | ACH routing number |
| `country` | Yes | Country for the destination bank account |

#### 

Bank Transfer

[Skip link to Bank Transfer](https://docs.nadapay.io/docs/create-beneficiary#bank-transfer)

| Field | Required | Notes |
| --- | --- | --- |
| `accountNumber` | Yes | Recipient bank account number |
| `accountName` | Yes | Recipient account name |
| `networkId` | Yes | Provider or banking network identifier |
| `country` | Yes | Destination country |
| `bankCode` | Conditional | Use when required for the destination banking scheme |
| `iban` | Conditional | Use for IBAN-based corridors |
| `swiftCode` | Conditional | Use for international wire routing |
| `sortCode` | Conditional | Use for UK bank routing |
| `routingNumber` | Conditional | Use for US bank routing when applicable |
| `clabe` | Conditional | Use for Mexico corridors |
| `pixKey` | Conditional | Use for Brazil PIX flows |
| `cpf` | Conditional | Use when the corridor requires recipient CPF |

#### 

Mobile Money

[Skip link to Mobile Money](https://docs.nadapay.io/docs/create-beneficiary#mobile-money)

| Field | Required | Notes |
| --- | --- | --- |
| `phoneNumber` | Yes | Recipient mobile money number |
| `provider` | Yes | Mobile money provider |
| `country` | Yes | Destination country |
| `networkId` | Conditional | Use when provider routing depends on a network identifier |

#### 

Crypto

[Skip link to Crypto](https://docs.nadapay.io/docs/create-beneficiary#crypto)

| Field | Required | Notes |
| --- | --- | --- |
| `chain` | Yes | Blockchain network |
| `address` | Yes | Recipient wallet address |

For crypto rails, do not send `accountName`, `provider`, or `country`.

**Response:**

JSON

```
{
  "data": {
    "id": "ben_01HXXXXXXXXXXXXXXXXXX",
    "name": "John Doe",
    "type": "individual",
    "status": "active",
    "created_at": "2025-01-01T00:00:00Z"
  }
}
```

Save the `id` - you will use it to attach a payout account in the next step.

**Response - error:**

JSON

```
{
  "statusCode": 500,
  "message": "Internal server error"
}
```

## 

What success looks like

[Skip link to What success looks like](https://docs.nadapay.io/docs/create-beneficiary#what-success-looks-like)

- the beneficiary is created successfully
- you save the returned beneficiary ID
- the beneficiary account is attached successfully when you complete Step 2

## 

Do not continue if

[Skip link to Do not continue if](https://docs.nadapay.io/docs/create-beneficiary#do-not-continue-if)

- beneficiary creation returns an error
- the selected rail does not match the `details` fields you sent
- a bank-based rail has not been resolved and confirmed first

## 

Step 2 - Add a beneficiary account

[Skip link to Step 2 - Add a beneficiary account](https://docs.nadapay.io/docs/create-beneficiary#step-2---add-a-beneficiary-account)

If you are adding a bank account, resolve it first with [Resolve a Bank Account](https://docs.nadapay.io/docs/resolve-bank-account).

Bash

```
curl --request POST \
  --url $baseUrl/beneficiaries/ben_01HXXXXXXXXXXXXXXXXXX/accounts \
  --header 'x-api-key: YOUR_API_KEY' \
  --header 'Content-Type: application/json' \
  --header 'x-idempotency-key: YOUR_UNIQUE_UUID' \
  --data '{
    "currency": "USD",
    "type": "INTERNAL",
    "details": {
      "nadapayCode": "string",
      "accountNumber": "string",
      "accountName": "string",
      "networkId": "string",
      "rail": "ACH",
      "bankCode": "string",
      "country": "NG",
      "iban": "string",
      "swiftCode": "string",
      "sortCode": "string",
      "routingNumber": "string",
      "clabe": "string",
      "pixKey": "string",
      "cpf": "string",
      "chain": "ETHEREUM",
      "address": "string",
      "legalName": "string",
      "accountType": "personal",
      "phoneNumber": "string",
      "provider": "string",
      "streetLine1": "string",
      "city": "string",
      "state": "string",
      "postalCode": "string"
    }
  }'
```

Use the same rail-based `details` rules above when you add the beneficiary account.

**Response - error:**

JSON

```
{
  "statusCode": 500,
  "message": "Internal server error"
}
```

## 

What this step returns

[Skip link to What this step returns](https://docs.nadapay.io/docs/create-beneficiary#what-this-step-returns)

- beneficiary ID from Step 1
- beneficiary account details from Step 2

Save the beneficiary ID after creation and the beneficiary account details after the account is attached.

## 

Common reasons this step fails

[Skip link to Common reasons this step fails](https://docs.nadapay.io/docs/create-beneficiary#common-reasons-this-step-fails)

- the selected rail does not match the `details` fields you sent
- required fields for the rail are missing
- the destination configuration is invalid for the selected rail

## 

Call this next

[Skip link to Call this next](https://docs.nadapay.io/docs/create-beneficiary#call-this-next)

- [Resolve a Bank Account](https://docs.nadapay.io/docs/resolve-bank-account)
- [Fetch Transaction Limits](https://docs.nadapay.io/docs/fetch-transaction-limits)
- [Authenticate with x-api-key](https://docs.nadapay.io/docs/how-to)

Updated about 2 months ago

---

Did this page help you?

Yes

No

Copy Page