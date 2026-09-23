# Source: https://docs.nadapay.io/reference/paymentlinkcontroller_share

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

[Skip link to id](https://docs.nadapay.io/reference/paymentlinkcontroller_share#path-params-id)

The unique identifier

emails

array of strings

required

[Skip link to emails](https://docs.nadapay.io/reference/paymentlinkcontroller_share#body-params-emails)

emails\*

ADD string

metadata

object

[Skip link to metadata](https://docs.nadapay.io/reference/paymentlinkcontroller_share#body-params-metadata)

metadata object

# 

200

Payment link shared successfully.

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
     --url https://core.nadapay.io/api/v1/organization/payment-links/id/share \
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