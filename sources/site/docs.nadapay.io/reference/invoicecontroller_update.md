# Source: https://docs.nadapay.io/reference/invoicecontroller_update

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

[Skip link to id](https://docs.nadapay.io/reference/invoicecontroller_update#path-params-id)

The unique identifier

status

string

enum

[Skip link to status](https://docs.nadapay.io/reference/invoicecontroller_update#body-params-status)

DRAFTSENTPAIDOVERDUECANCELLED

Allowed:

`DRAFT``SENT``PAID``OVERDUE``CANCELLED`

notesToClient

string

[Skip link to notesToClient](https://docs.nadapay.io/reference/invoicecontroller_update#body-params-notesToClient)

internalNotes

string

[Skip link to internalNotes](https://docs.nadapay.io/reference/invoicecontroller_update#body-params-internalNotes)

# 

200

Invoice updated successfully.

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
     --url https://core.nadapay.io/api/v1/organization/invoices/id \
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