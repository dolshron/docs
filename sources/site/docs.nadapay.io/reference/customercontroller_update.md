# Source: https://docs.nadapay.io/reference/customercontroller_update

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

[Skip link to id](https://docs.nadapay.io/reference/customercontroller_update#path-params-id)

The unique identifier

name

string

[Skip link to name](https://docs.nadapay.io/reference/customercontroller_update#body-params-name)

email

string

[Skip link to email](https://docs.nadapay.io/reference/customercontroller_update#body-params-email)

phoneNumber

string

[Skip link to phoneNumber](https://docs.nadapay.io/reference/customercontroller_update#body-params-phoneNumber)

address

string

[Skip link to address](https://docs.nadapay.io/reference/customercontroller_update#body-params-address)

metadata

object

[Skip link to metadata](https://docs.nadapay.io/reference/customercontroller_update#body-params-metadata)

metadata object

# 

200

Customer updated successfully.

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
     --url https://core.nadapay.io/api/v1/organization/customers/id \
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