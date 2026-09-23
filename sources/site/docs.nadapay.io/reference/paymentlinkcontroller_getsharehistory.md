# Source: https://docs.nadapay.io/reference/paymentlinkcontroller_getsharehistory

| Time | Status | User Agent | |
| :-- | :-- | :-- | :-- |
| 
Retrieving recent requests…

 |

Loading…

#### URL Expired

The URL for this request expired after 30 days.

page

number

Defaults to 1

[Skip link to page](https://docs.nadapay.io/reference/paymentlinkcontroller_getsharehistory#query-params-page)

limit

number

Defaults to 10

[Skip link to limit](https://docs.nadapay.io/reference/paymentlinkcontroller_getsharehistory#query-params-limit)

sortBy

string

Defaults to createdAt

[Skip link to sortBy](https://docs.nadapay.io/reference/paymentlinkcontroller_getsharehistory#query-params-sortBy)

sortOrder

string

enum

Defaults to desc

[Skip link to sortOrder](https://docs.nadapay.io/reference/paymentlinkcontroller_getsharehistory#query-params-sortOrder)

ascdesc

Allowed:

`asc``desc`

paymentLinkId

string

[Skip link to paymentLinkId](https://docs.nadapay.io/reference/paymentlinkcontroller_getsharehistory#query-params-paymentLinkId)

# 

200

Share history retrieved successfully.

Updated 3 months ago

---

Did this page help you?

Yes

No

ShellNodeRubyPHPPython

```
xxxxxxxxxx
1
curl --request GET \
2
     --url https://core.nadapay.io/api/v1/organization/payment-links/shares/history \
3
     --header 'accept: application/json'
```

Click `Try It!` to start a request and see the response here! Or choose an example:

application/json

200

Updated 3 months ago

---

Did this page help you?

Yes

No