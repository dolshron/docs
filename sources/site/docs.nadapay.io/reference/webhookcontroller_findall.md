# Source: https://docs.nadapay.io/reference/webhookcontroller_findall

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

[Skip link to page](https://docs.nadapay.io/reference/webhookcontroller_findall#query-params-page)

limit

number

Defaults to 10

[Skip link to limit](https://docs.nadapay.io/reference/webhookcontroller_findall#query-params-limit)

sortBy

string

Defaults to createdAt

[Skip link to sortBy](https://docs.nadapay.io/reference/webhookcontroller_findall#query-params-sortBy)

sortOrder

string

enum

Defaults to desc

[Skip link to sortOrder](https://docs.nadapay.io/reference/webhookcontroller_findall#query-params-sortOrder)

ascdesc

Allowed:

`asc``desc`

# 

200

Webhooks retrieved successfully.

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
     --url https://core.nadapay.io/api/v1/organization/webhooks \
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