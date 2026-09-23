# Source: https://docs.nadapay.io/reference/checkoutcontroller_configure

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

[Skip link to name](https://docs.nadapay.io/reference/checkoutcontroller_configure#body-params-name)

Configuration name

settlementAccountId

string

required

[Skip link to settlementAccountId](https://docs.nadapay.io/reference/checkoutcontroller_configure#body-params-settlementAccountId)

The wallet ID where funds will settle

checkoutType

string

enum

required

Defaults to CUSTOM

[Skip link to checkoutType](https://docs.nadapay.io/reference/checkoutcontroller_configure#body-params-checkoutType)

PRODUCTCUSTOM

Allowed:

`PRODUCT``CUSTOM`

productIds

array of strings

[Skip link to productIds](https://docs.nadapay.io/reference/checkoutcontroller_configure#body-params-productIds)

Required if checkoutType is PRODUCT

productIds

ADD string

allowedDomains

array of strings

[Skip link to allowedDomains](https://docs.nadapay.io/reference/checkoutcontroller_configure#body-params-allowedDomains)

allowedDomains

ADD string

branding

object

[Skip link to branding](https://docs.nadapay.io/reference/checkoutcontroller_configure#body-params-branding)

branding object

returnUrl

string

[Skip link to returnUrl](https://docs.nadapay.io/reference/checkoutcontroller_configure#body-params-returnUrl)

successUrl

string

[Skip link to successUrl](https://docs.nadapay.io/reference/checkoutcontroller_configure#body-params-successUrl)

enabledFiatCurrencies

array of strings

[Skip link to enabledFiatCurrencies](https://docs.nadapay.io/reference/checkoutcontroller_configure#body-params-enabledFiatCurrencies)

enabledFiatCurrencies

ADD string

enabledCryptoCurrencies

array of strings

[Skip link to enabledCryptoCurrencies](https://docs.nadapay.io/reference/checkoutcontroller_configure#body-params-enabledCryptoCurrencies)

enabledCryptoCurrencies

ADD string

enabledPaymentMethods

array of strings

[Skip link to enabledPaymentMethods](https://docs.nadapay.io/reference/checkoutcontroller_configure#body-params-enabledPaymentMethods)

Allowed: crypto, nadapay\_wallet, card, bank\_transfer

enabledPaymentMethods

ADD string

# 

200

Checkout configured successfully.

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
     --url https://core.nadapay.io/api/v1/organization/checkout/configure \
3
     --header 'accept: application/json' \
4
     --header 'content-type: application/json' \
5
     --data '
6
{
7
  "checkoutType": "CUSTOM"
8
}
9
'
```

Click `Try It!` to start a request and see the response here! Or choose an example:

application/json

200

Updated 3 months ago

---

Did this page help you?

Yes

No