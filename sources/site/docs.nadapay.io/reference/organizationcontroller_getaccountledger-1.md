# Source: https://docs.nadapay.io/reference/organizationcontroller_getaccountledger-1

| Time | Status | User Agent | |
| :-- | :-- | :-- | :-- |
| 
Retrieving recent requests…

 |

Loading…

#### URL Expired

The URL for this request expired after 30 days.

accountId

string

required

[Skip link to accountId](https://docs.nadapay.io/reference/organizationcontroller_getaccountledger-1#path-params-accountId)

page

number

Defaults to 1

[Skip link to page](https://docs.nadapay.io/reference/organizationcontroller_getaccountledger-1#query-params-page)

limit

number

Defaults to 10

[Skip link to limit](https://docs.nadapay.io/reference/organizationcontroller_getaccountledger-1#query-params-limit)

sortBy

string

Defaults to createdAt

[Skip link to sortBy](https://docs.nadapay.io/reference/organizationcontroller_getaccountledger-1#query-params-sortBy)

sortOrder

string

enum

Defaults to desc

[Skip link to sortOrder](https://docs.nadapay.io/reference/organizationcontroller_getaccountledger-1#query-params-sortOrder)

ascdesc

Allowed:

`asc``desc`

200

Ledger entries retrieved successfully.

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
     --url https://core.nadapay.io/api/v1/organizations/accounts/accountId/ledger
```

Click `Try It!` to start a request and see the response here!

Updated 3 months ago

---

Did this page help you?

Yes

No