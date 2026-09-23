# Source: https://docs.nadapay.io/reference/cardcontroller_switchaccount

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

[Skip link to id](https://docs.nadapay.io/reference/cardcontroller_switchaccount#path-params-id)

nadapayCode

string

required

[Skip link to nadapayCode](https://docs.nadapay.io/reference/cardcontroller_switchaccount#body-params-nadapayCode)

The new NadapayCode to tie the card to

# 

200

Card account switched successfully.

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
     --url https://core.nadapay.io/api/v1/organization/cards/id/account \
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