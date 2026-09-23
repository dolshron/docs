# Source: https://docs.nadapay.io/reference/webhookcontroller_gethistory

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

[Skip link to page](https://docs.nadapay.io/reference/webhookcontroller_gethistory#query-params-page)

limit

number

Defaults to 10

[Skip link to limit](https://docs.nadapay.io/reference/webhookcontroller_gethistory#query-params-limit)

sortBy

string

Defaults to createdAt

[Skip link to sortBy](https://docs.nadapay.io/reference/webhookcontroller_gethistory#query-params-sortBy)

sortOrder

string

enum

Defaults to desc

[Skip link to sortOrder](https://docs.nadapay.io/reference/webhookcontroller_gethistory#query-params-sortOrder)

ascdesc

Allowed:

`asc``desc`

webhookId

string

required

[Skip link to webhookId](https://docs.nadapay.io/reference/webhookcontroller_gethistory#query-params-webhookId)

# 

200

Delivery history retrieved successfully.

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
     --url https://core.nadapay.io/api/v1/organization/webhooks/deliveries/history \
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