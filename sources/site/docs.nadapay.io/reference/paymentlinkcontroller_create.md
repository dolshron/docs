# Source: https://docs.nadapay.io/reference/paymentlinkcontroller_create

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

[Skip link to name](https://docs.nadapay.io/reference/paymentlinkcontroller_create#body-params-name)

checkoutType

string

enum

required

Defaults to CUSTOM

[Skip link to checkoutType](https://docs.nadapay.io/reference/paymentlinkcontroller_create#body-params-checkoutType)

PRODUCTCUSTOM

Allowed:

`PRODUCT``CUSTOM`

productId

string

[Skip link to productId](https://docs.nadapay.io/reference/paymentlinkcontroller_create#body-params-productId)

Required if checkoutType is PRODUCT

description

string

[Skip link to description](https://docs.nadapay.io/reference/paymentlinkcontroller_create#body-params-description)

image

string

[Skip link to image](https://docs.nadapay.io/reference/paymentlinkcontroller_create#body-params-image)

amount

number

[Skip link to amount](https://docs.nadapay.io/reference/paymentlinkcontroller_create#body-params-amount)

Leave empty for variable amount

currency

string

[Skip link to currency](https://docs.nadapay.io/reference/paymentlinkcontroller_create#body-params-currency)

isVariableAmount

boolean

required

[Skip link to isVariableAmount](https://docs.nadapay.io/reference/paymentlinkcontroller_create#body-params-isVariableAmount)

Allows customer to enter the amount

truefalse

settlementAccountId

string

required

[Skip link to settlementAccountId](https://docs.nadapay.io/reference/paymentlinkcontroller_create#body-params-settlementAccountId)

The wallet ID where funds will land

collectAddress

boolean

[Skip link to collectAddress](https://docs.nadapay.io/reference/paymentlinkcontroller_create#body-params-collectAddress)

truefalse

collectPhoneNumber

boolean

[Skip link to collectPhoneNumber](https://docs.nadapay.io/reference/paymentlinkcontroller_create#body-params-collectPhoneNumber)

truefalse

customFieldLabel

string

[Skip link to customFieldLabel](https://docs.nadapay.io/reference/paymentlinkcontroller_create#body-params-customFieldLabel)

redirectUrl

string

[Skip link to redirectUrl](https://docs.nadapay.io/reference/paymentlinkcontroller_create#body-params-redirectUrl)

successMessage

string

[Skip link to successMessage](https://docs.nadapay.io/reference/paymentlinkcontroller_create#body-params-successMessage)

expiresAt

string

[Skip link to expiresAt](https://docs.nadapay.io/reference/paymentlinkcontroller_create#body-params-expiresAt)

# 

201

Payment link created successfully.

Updated 3 months ago

---

Did this page help you?

Yes

No

ShellNodeRubyPHPPython

```
xxxxxxxxxx10
1
curl --request POST \
2
     --url https://core.nadapay.io/api/v1/organization/payment-links \
3
     --header 'accept: application/json' \
4
     --header 'content-type: application/json' \
5
     --data '
6
{
7
  "checkoutType": "CUSTOM",
8
  "isVariableAmount": true
9
}
10
'
```

Click `Try It!` to start a request and see the response here! Or choose an example:

application/json

201

Updated 3 months ago

---

Did this page help you?

Yes

No