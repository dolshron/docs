# Source: https://docs.nadapay.io/reference/beneficiarycontroller_batchcreate

| Time | Status | User Agent | |
| :-- | :-- | :-- | :-- |
| 
Retrieving recent requests…

 |

Loading…

#### URL Expired

The URL for this request expired after 30 days.

beneficiaries

array of objects

required

[Skip link to beneficiaries](https://docs.nadapay.io/reference/beneficiarycontroller_batchcreate#body-params-beneficiaries)

List of beneficiaries to create

beneficiaries\*

ADD object

x-idempotency-key

string

[Skip link to x-idempotency-key](https://docs.nadapay.io/reference/beneficiarycontroller_batchcreate#header-params-x-idempotency-key)

Unique key to prevent duplicate processing.

201

Beneficiaries successfully registered.

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
     --url https://core.nadapay.io/api/v1/beneficiaries/batch \
3
     --header 'content-type: application/json'
```

Click `Try It!` to start a request and see the response here!

Updated 3 months ago

---

Did this page help you?

Yes

No