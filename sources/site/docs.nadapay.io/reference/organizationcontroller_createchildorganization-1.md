# Source: https://docs.nadapay.io/reference/organizationcontroller_createchildorganization-1

| Time | Status | User Agent | |
| :-- | :-- | :-- | :-- |
| 
Retrieving recent requests…

 |

Loading…

#### URL Expired

The URL for this request expired after 30 days.

businessName

string

required

[Skip link to businessName](https://docs.nadapay.io/reference/organizationcontroller_createchildorganization-1#body-params-businessName)

Business name

businessType

string

required

[Skip link to businessType](https://docs.nadapay.io/reference/organizationcontroller_createchildorganization-1#body-params-businessType)

Type of business

businessEmail

string

required

[Skip link to businessEmail](https://docs.nadapay.io/reference/organizationcontroller_createchildorganization-1#body-params-businessEmail)

Business email

phoneNumber

string

required

[Skip link to phoneNumber](https://docs.nadapay.io/reference/organizationcontroller_createchildorganization-1#body-params-phoneNumber)

Business phone number

address

string

required

[Skip link to address](https://docs.nadapay.io/reference/organizationcontroller_createchildorganization-1#body-params-address)

Business address

country

string

required

[Skip link to country](https://docs.nadapay.io/reference/organizationcontroller_createchildorganization-1#body-params-country)

Business country

city

string

required

[Skip link to city](https://docs.nadapay.io/reference/organizationcontroller_createchildorganization-1#body-params-city)

Business city

state

string

required

[Skip link to state](https://docs.nadapay.io/reference/organizationcontroller_createchildorganization-1#body-params-state)

Business state

firstname

string

required

[Skip link to firstname](https://docs.nadapay.io/reference/organizationcontroller_createchildorganization-1#body-params-firstname)

First name of the contact person

lastname

string

required

[Skip link to lastname](https://docs.nadapay.io/reference/organizationcontroller_createchildorganization-1#body-params-lastname)

Last name of the contact person

website

string

[Skip link to website](https://docs.nadapay.io/reference/organizationcontroller_createchildorganization-1#body-params-website)

Business website

x-idempotency-key

string

[Skip link to x-idempotency-key](https://docs.nadapay.io/reference/organizationcontroller_createchildorganization-1#header-params-x-idempotency-key)

Unique key to prevent duplicate processing.

# 

201

Child organization and owner user successfully created.

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
     --url https://core.nadapay.io/api/v1/organizations/children \
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