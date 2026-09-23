# Source: https://docs.nadapay.io/reference/organizationmarketcontroller_findall

| Time | Status | User Agent | |
| :-- | :-- | :-- | :-- |
| 
Retrieving recent requests…

 |

Loading…

#### URL Expired

The URL for this request expired after 30 days.

channel

string

enum

[Skip link to channel](https://docs.nadapay.io/reference/organizationmarketcontroller_findall#query-params-channel)

Filter markets by supported payment channel.

collectionpayoutswap

Allowed:

`collection``payout``swap`

isActive

boolean

[Skip link to isActive](https://docs.nadapay.io/reference/organizationmarketcontroller_findall#query-params-isActive)

Filter by market active status.

truefalse

# 

200

List of supported markets.

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
     --url https://core.nadapay.io/api/v1/organization/markets \
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