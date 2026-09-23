# Source: https://docs.nadapay.io/docs/resolve-bank-account

Resolve a bank account so you can confirm the account holder name before you attach it to a beneficiary.

## 

When to use this page

[Skip link to When to use this page](https://docs.nadapay.io/docs/resolve-bank-account#when-to-use-this-page)

Use this page before you add a bank-based beneficiary account so you can verify the destination details first.

## 

Prerequisites

[Skip link to Prerequisites](https://docs.nadapay.io/docs/resolve-bank-account#prerequisites)

1. Set your NadaPay API base URL in `$baseUrl`.
2. Export your NadaPay API key as `YOUR_API_KEY`.
3. Generate a unique idempotency key for the request.

## 

Before you continue

[Skip link to Before you continue](https://docs.nadapay.io/docs/resolve-bank-account#before-you-continue)

- confirm you are using a bank-based rail
- fetch the correct provider network when the corridor depends on network selection
- collect the account number and network identifier you want to validate

## 

Step 1 - Resolve the bank account

[Skip link to Step 1 - Resolve the bank account](https://docs.nadapay.io/docs/resolve-bank-account#step-1---resolve-the-bank-account)

Bash

```
curl --request POST \
  --url $baseUrl/transactions/resolve-bank-account \
  --header 'x-api-key: YOUR_API_KEY' \
  --header 'Content-Type: application/json' \
  --header 'x-idempotency-key: YOUR_UNIQUE_UUID' \
  --data '{
    "accountNumber": "0123456789",
    "networkId": "ntwk_01HXXXXXXXXXXXXXXXXXX"
  }'
```

## 

Step 2 - Review the response

[Skip link to Step 2 - Review the response](https://docs.nadapay.io/docs/resolve-bank-account#step-2---review-the-response)

**Response - resolved:**

A successful response returns the resolved account holder name and verification status for the submitted account details. Use the response shape shown in the API Reference for this endpoint.

**Response - not found:**

JSON

```
{
  "statusCode": 500,
  "message": "Internal server error"
}
```

## 

What success looks like

[Skip link to What success looks like](https://docs.nadapay.io/docs/resolve-bank-account#what-success-looks-like)

- the account resolves successfully
- the returned account name matches the intended recipient
- the validation result is acceptable for the bank-based rail you selected

## 

Do not continue if

[Skip link to Do not continue if](https://docs.nadapay.io/docs/resolve-bank-account#do-not-continue-if)

- the account cannot be resolved
- the resolved account name does not match the intended recipient
- the network ID does not match the bank account details you are validating

## 

Step 3 - Confirm the account name before you continue

[Skip link to Step 3 - Confirm the account name before you continue](https://docs.nadapay.io/docs/resolve-bank-account#step-3---confirm-the-account-name-before-you-continue)

Show the resolved `account_name` to the user or operations team and ask them to confirm it matches the intended recipient. This is a critical step to prevent misdirected transfers.

Once confirmed, add it using [Add Beneficiary Account](https://docs.nadapay.io/reference/beneficiarycontroller_addaccount).

> ✅
> 
> ### 
> 
> Always resolve before adding. Never skip this step for bank account payouts.
> 
> [Skip link to Always resolve before adding. Never skip this step for bank account payouts.](https://docs.nadapay.io/docs/resolve-bank-account#always-resolve-before-adding-never-skip-this-step-for-bank-account-payouts)

## 

What this step returns

[Skip link to What this step returns](https://docs.nadapay.io/docs/resolve-bank-account#what-this-step-returns)

- resolved account name
- validation result for the account details you submitted

Save the resolved account information and use it to confirm the destination before you attach the beneficiary account.

## 

Common reasons this step fails

[Skip link to Common reasons this step fails](https://docs.nadapay.io/docs/resolve-bank-account#common-reasons-this-step-fails)

- account number and network ID do not match
- destination account details are invalid
- the selected network does not support the account you are resolving

## 

Call this next

[Skip link to Call this next](https://docs.nadapay.io/docs/resolve-bank-account#call-this-next)

- [Create a Beneficiary](https://docs.nadapay.io/docs/create-beneficiary)
- [Get Provider Networks for a Country](https://docs.nadapay.io/docs/get-provider-networks)
- [Authenticate with x-api-key](https://docs.nadapay.io/docs/how-to)

Updated about 2 months ago

---

Did this page help you?

Yes

No

Copy Page