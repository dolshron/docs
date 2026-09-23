# Source: https://docs.nadapay.io/reference/beneficiarycontroller_update-1

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

[Skip link to id](https://docs.nadapay.io/reference/beneficiarycontroller_update-1#path-params-id)

name

string

[Skip link to name](https://docs.nadapay.io/reference/beneficiarycontroller_update-1#body-params-name)

Beneficiary name

email

string

[Skip link to email](https://docs.nadapay.io/reference/beneficiarycontroller_update-1#body-params-email)

Beneficiary email

phone

string

[Skip link to phone](https://docs.nadapay.io/reference/beneficiarycontroller_update-1#body-params-phone)

Beneficiary phone number

status

string

[Skip link to status](https://docs.nadapay.io/reference/beneficiarycontroller_update-1#body-params-status)

Status

x-idempotency-key

string

[Skip link to x-idempotency-key](https://docs.nadapay.io/reference/beneficiarycontroller_update-1#header-params-x-idempotency-key)

Unique key to prevent duplicate processing.

200

Beneficiary profile updated.

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
     --url https://core.nadapay.io/api/v1/beneficiaries/id \
3
     --header 'content-type: application/json'
```

Click `Try It!` to start a request and see the response here!

Updated 3 months ago

---

Did this page help you?

Yes

No