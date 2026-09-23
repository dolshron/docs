# Source: https://docs.nadapay.io/reference/paymentlinkcontroller_update

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

[Skip link to id](https://docs.nadapay.io/reference/paymentlinkcontroller_update#path-params-id)

The unique identifier

name

string

[Skip link to name](https://docs.nadapay.io/reference/paymentlinkcontroller_update#body-params-name)

description

string

[Skip link to description](https://docs.nadapay.io/reference/paymentlinkcontroller_update#body-params-description)

status

string

[Skip link to status](https://docs.nadapay.io/reference/paymentlinkcontroller_update#body-params-status)

redirectUrl

string

[Skip link to redirectUrl](https://docs.nadapay.io/reference/paymentlinkcontroller_update#body-params-redirectUrl)

# 

200

Payment link updated successfully.

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
     --url https://core.nadapay.io/api/v1/organization/payment-links/id \
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