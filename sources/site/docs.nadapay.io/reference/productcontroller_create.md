# Source: https://docs.nadapay.io/reference/productcontroller_create

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

[Skip link to name](https://docs.nadapay.io/reference/productcontroller_create#body-params-name)

description

string

[Skip link to description](https://docs.nadapay.io/reference/productcontroller_create#body-params-description)

image

string

[Skip link to image](https://docs.nadapay.io/reference/productcontroller_create#body-params-image)

sku

string

[Skip link to sku](https://docs.nadapay.io/reference/productcontroller_create#body-params-sku)

type

string

enum

required

Defaults to ONE\_TIME

[Skip link to type](https://docs.nadapay.io/reference/productcontroller_create#body-params-type)

RECURRINGONE\_TIME

Allowed:

`RECURRING``ONE_TIME`

price

number

required

[Skip link to price](https://docs.nadapay.io/reference/productcontroller_create#body-params-price)

Price in units (will be converted to micros)

currency

string

required

[Skip link to currency](https://docs.nadapay.io/reference/productcontroller_create#body-params-currency)

billingPeriod

string

[Skip link to billingPeriod](https://docs.nadapay.io/reference/productcontroller_create#body-params-billingPeriod)

Required if type is RECURRING

status

string

enum

Defaults to ACTIVE

[Skip link to status](https://docs.nadapay.io/reference/productcontroller_create#body-params-status)

ACTIVEARCHIVEDDRAFT

Allowed:

`ACTIVE``ARCHIVED``DRAFT`

metadata

object

[Skip link to metadata](https://docs.nadapay.io/reference/productcontroller_create#body-params-metadata)

metadata object

# 

201

Product created successfully.

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
     --url https://core.nadapay.io/api/v1/organization/products \
3
     --header 'accept: application/json' \
4
     --header 'content-type: application/json' \
5
     --data '{"type":"ONE_TIME"}'
```

Click `Try It!` to start a request and see the response here! Or choose an example:

application/json

201

Updated 3 months ago

---

Did this page help you?

Yes

No