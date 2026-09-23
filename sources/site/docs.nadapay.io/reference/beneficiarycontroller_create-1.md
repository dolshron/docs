# Source: https://docs.nadapay.io/reference/beneficiarycontroller_create-1

| Time | Status | User Agent | |
| :-- | :-- | :-- | :-- |
| 
Retrieving recent requests…

 |

Loading…

#### URL Expired

The URL for this request expired after 30 days.

name

string

required

[Skip link to name](https://docs.nadapay.io/reference/beneficiarycontroller_create-1#body-params-name)

Beneficiary name

email

string

[Skip link to email](https://docs.nadapay.io/reference/beneficiarycontroller_create-1#body-params-email)

Beneficiary email

phone

string

[Skip link to phone](https://docs.nadapay.io/reference/beneficiarycontroller_create-1#body-params-phone)

Beneficiary phone number

currency

string

required

[Skip link to currency](https://docs.nadapay.io/reference/beneficiarycontroller_create-1#body-params-currency)

Currency code

type

string

enum

required

[Skip link to type](https://docs.nadapay.io/reference/beneficiarycontroller_create-1#body-params-type)

Beneficiary type

INTERNALEXTERNAL\_BANKEXTERNAL\_WALLET

Allowed:

`INTERNAL``EXTERNAL_BANK``EXTERNAL_WALLET`

details

object

required

[Skip link to details](https://docs.nadapay.io/reference/beneficiarycontroller_create-1#body-params-details)

details object

x-idempotency-key

string

[Skip link to x-idempotency-key](https://docs.nadapay.io/reference/beneficiarycontroller_create-1#header-params-x-idempotency-key)

Unique key to prevent duplicate processing.

201

Beneficiary successfully registered.

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
     --url https://core.nadapay.io/api/v1/beneficiaries \
3
     --header 'content-type: application/json' \
4
     --data '{"type":"INTERNAL"}'
```

Click `Try It!` to start a request and see the response here!

Updated 3 months ago

---

Did this page help you?

Yes

No