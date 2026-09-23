# Source: https://docs.nadapay.io/reference/beneficiarycontroller_updateaccount-1

| Time | Status | User Agent | |
| :-- | :-- | :-- | :-- |
| 
Retrieving recent requests…

 |

Loading…

#### URL Expired

The URL for this request expired after 30 days.

accountId

string

required

[Skip link to accountId](https://docs.nadapay.io/reference/beneficiarycontroller_updateaccount-1#path-params-accountId)

currency

string

[Skip link to currency](https://docs.nadapay.io/reference/beneficiarycontroller_updateaccount-1#body-params-currency)

Currency code

type

string

enum

[Skip link to type](https://docs.nadapay.io/reference/beneficiarycontroller_updateaccount-1#body-params-type)

Beneficiary type

INTERNALEXTERNAL\_BANKEXTERNAL\_WALLET

Allowed:

`INTERNAL``EXTERNAL_BANK``EXTERNAL_WALLET`

details

object

[Skip link to details](https://docs.nadapay.io/reference/beneficiarycontroller_updateaccount-1#body-params-details)

details object

status

string

[Skip link to status](https://docs.nadapay.io/reference/beneficiarycontroller_updateaccount-1#body-params-status)

Status

x-idempotency-key

string

[Skip link to x-idempotency-key](https://docs.nadapay.io/reference/beneficiarycontroller_updateaccount-1#header-params-x-idempotency-key)

Unique key to prevent duplicate processing.

200

Account details updated.

Updated 3 months ago

---

Did this page help you?

Yes

No

ShellNodeRubyPHPPython

```
xxxxxxxxxx
1
curl --request PATCH \
2
     --url https://core.nadapay.io/api/v1/beneficiaries/accounts/accountId \
3
     --header 'content-type: application/json'
```

Click `Try It!` to start a request and see the response here!

Updated 3 months ago

---

Did this page help you?

Yes

No