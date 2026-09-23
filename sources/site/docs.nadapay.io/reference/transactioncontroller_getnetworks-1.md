# Source: https://docs.nadapay.io/reference/transactioncontroller_getnetworks-1

| Time | Status | User Agent | |
| :-- | :-- | :-- | :-- |
| 
Retrieving recent requests…

 |

Loading…

#### URL Expired

The URL for this request expired after 30 days.

country

string

required

[Skip link to country](https://docs.nadapay.io/reference/transactioncontroller_getnetworks-1#body-params-country)

Country ISO code (ISO 3166-2)

x-idempotency-key

string

[Skip link to x-idempotency-key](https://docs.nadapay.io/reference/transactioncontroller_getnetworks-1#header-params-x-idempotency-key)

Unique key to prevent duplicate processing.

200

List of available networks for the specified country.

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
     --url https://core.nadapay.io/api/v1/transactions/networks \
3
     --header 'content-type: application/json'
```

Click `Try It!` to start a request and see the response here!

Updated 3 months ago

---

Did this page help you?

Yes

No