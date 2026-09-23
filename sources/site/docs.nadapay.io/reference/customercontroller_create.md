# Source: https://docs.nadapay.io/reference/customercontroller_create

| Time | Status | User Agent | |
| :-- | :-- | :-- | :-- |
| 
Retrieving recent requests…

 |

Loading…

#### URL Expired

The URL for this request expired after 30 days.

name

string

required

[Skip link to name](https://docs.nadapay.io/reference/customercontroller_create#body-params-name)

email

string

required

[Skip link to email](https://docs.nadapay.io/reference/customercontroller_create#body-params-email)

phoneNumber

string

[Skip link to phoneNumber](https://docs.nadapay.io/reference/customercontroller_create#body-params-phoneNumber)

address

string

[Skip link to address](https://docs.nadapay.io/reference/customercontroller_create#body-params-address)

metadata

object

[Skip link to metadata](https://docs.nadapay.io/reference/customercontroller_create#body-params-metadata)

metadata object

# 

201

Customer created successfully.

409

A customer with this email already exists.

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
     --url https://core.nadapay.io/api/v1/organization/customers \
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