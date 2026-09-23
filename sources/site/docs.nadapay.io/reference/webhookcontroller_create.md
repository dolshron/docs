# Source: https://docs.nadapay.io/reference/webhookcontroller_create

| Time | Status | User Agent | |
| :-- | :-- | :-- | :-- |
| 
Retrieving recent requests…

 |

Loading…

#### URL Expired

The URL for this request expired after 30 days.

url

string

required

[Skip link to url](https://docs.nadapay.io/reference/webhookcontroller_create#body-params-url)

events

array of strings

[Skip link to events](https://docs.nadapay.io/reference/webhookcontroller_create#body-params-events)

events

ADD string

status

string

enum

[Skip link to status](https://docs.nadapay.io/reference/webhookcontroller_create#body-params-status)

ACTIVEINACTIVE

Allowed:

`ACTIVE``INACTIVE`

# 

201

Webhook registered successfully.

401

Invalid or missing authentication credentials.

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
     --url https://core.nadapay.io/api/v1/organization/webhooks \
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