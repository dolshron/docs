# Source: https://docs.nadapay.io/reference/productcontroller_update

| Time | Status | User Agent | |
| :-- | :-- | :-- | :-- |
| 
Retrieving recent requests…

 |

Loading…

#### URL Expired

The URL for this request expired after 30 days.

id

string

required

[Skip link to id](https://docs.nadapay.io/reference/productcontroller_update#path-params-id)

The unique identifier

name

string

[Skip link to name](https://docs.nadapay.io/reference/productcontroller_update#body-params-name)

description

string

[Skip link to description](https://docs.nadapay.io/reference/productcontroller_update#body-params-description)

image

string

[Skip link to image](https://docs.nadapay.io/reference/productcontroller_update#body-params-image)

type

string

[Skip link to type](https://docs.nadapay.io/reference/productcontroller_update#body-params-type)

price

number

[Skip link to price](https://docs.nadapay.io/reference/productcontroller_update#body-params-price)

currency

string

[Skip link to currency](https://docs.nadapay.io/reference/productcontroller_update#body-params-currency)

billingPeriod

string

[Skip link to billingPeriod](https://docs.nadapay.io/reference/productcontroller_update#body-params-billingPeriod)

status

string

[Skip link to status](https://docs.nadapay.io/reference/productcontroller_update#body-params-status)

metadata

object

[Skip link to metadata](https://docs.nadapay.io/reference/productcontroller_update#body-params-metadata)

metadata object

# 

200

Product updated successfully.

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
     --url https://core.nadapay.io/api/v1/organization/products/id \
3
     --header 'accept: application/json' \
4
     --header 'content-type: application/json'
```

Click `Try It!` to start a request and see the response here! Or choose an example:

application/json

200

Updated 3 months ago

---

Did this page help you?

Yes

No