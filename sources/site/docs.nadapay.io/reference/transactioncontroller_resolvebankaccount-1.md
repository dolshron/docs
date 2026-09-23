# Source: https://docs.nadapay.io/reference/transactioncontroller_resolvebankaccount-1

| Time | Status | User Agent | |
| :-- | :-- | :-- | :-- |
| 
Retrieving recent requests…

 |

Loading…

#### URL Expired

The URL for this request expired after 30 days.

accountNumber

string

required

[Skip link to accountNumber](https://docs.nadapay.io/reference/transactioncontroller_resolvebankaccount-1#body-params-accountNumber)

Bank account number

networkId

string

required

[Skip link to networkId](https://docs.nadapay.io/reference/transactioncontroller_resolvebankaccount-1#body-params-networkId)

Network ID

x-idempotency-key

string

[Skip link to x-idempotency-key](https://docs.nadapay.io/reference/transactioncontroller_resolvebankaccount-1#header-params-x-idempotency-key)

Unique key to prevent duplicate processing.

200

Resolved account holder name and verification status.

Updated 3 months ago

---

Did this page help you?

Yes

No

ShellNodeRubyPHPPython

```
xxxxxxxxxx
1
curl --request POST \
2
     --url https://core.nadapay.io/api/v1/transactions/resolve-bank-account \
3
     --header 'content-type: application/json'
```

Click `Try It!` to start a request and see the response here!

Updated 3 months ago

---

Did this page help you?

Yes

No