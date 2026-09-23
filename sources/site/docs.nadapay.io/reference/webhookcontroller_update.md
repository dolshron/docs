# Source: https://docs.nadapay.io/reference/webhookcontroller_update

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

[Skip link to id](https://docs.nadapay.io/reference/webhookcontroller_update#path-params-id)

The unique identifier

url

string

[Skip link to url](https://docs.nadapay.io/reference/webhookcontroller_update#body-params-url)

events

array of strings

[Skip link to events](https://docs.nadapay.io/reference/webhookcontroller_update#body-params-events)

events

ADD string

status

string

enum

[Skip link to status](https://docs.nadapay.io/reference/webhookcontroller_update#body-params-status)

ACTIVEINACTIVE

Allowed:

`ACTIVE``INACTIVE`

# 

200

Webhook updated successfully.

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
     --url https://core.nadapay.io/api/v1/organization/webhooks/id \
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