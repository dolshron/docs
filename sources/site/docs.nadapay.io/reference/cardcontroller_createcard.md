# Source: https://docs.nadapay.io/reference/cardcontroller_createcard

| Time | Status | User Agent | |
| :-- | :-- | :-- | :-- |
| 
Retrieving recent requests…

 |

Loading…

#### URL Expired

The URL for this request expired after 30 days.

nadapayCode

string

required

[Skip link to nadapayCode](https://docs.nadapay.io/reference/cardcontroller_createcard#body-params-nadapayCode)

The NadapayCode of the account to tie the card to

limit

number

[Skip link to limit](https://docs.nadapay.io/reference/cardcontroller_createcard#body-params-limit)

Spending limit in cents

# 

201

Card issued successfully.

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
     --url https://core.nadapay.io/api/v1/organization/cards \
3
     --header 'accept: application/json' \
4
     --header 'content-type: application/json'
```

Click `Try It!` to start a request and see the response here! Or choose an example:

application/json

201

Updated 3 months ago

---

Did this page help you?

Yes

No