# Source: https://docs.nadapay.io/reference/transactioncontroller_getquote-1

| Time | Status | User Agent | |
| :-- | :-- | :-- | :-- |
| 
Retrieving recent requests…

 |

Loading…

#### URL Expired

The URL for this request expired after 30 days.

source

object

required

[Skip link to source](https://docs.nadapay.io/reference/transactioncontroller_getquote-1#body-params-source)

source object

destination

object

required

[Skip link to destination](https://docs.nadapay.io/reference/transactioncontroller_getquote-1#body-params-destination)

destination object

metadata

object

[Skip link to metadata](https://docs.nadapay.io/reference/transactioncontroller_getquote-1#body-params-metadata)

Additional metadata

metadata object

x-idempotency-key

string

[Skip link to x-idempotency-key](https://docs.nadapay.io/reference/transactioncontroller_getquote-1#header-params-x-idempotency-key)

Unique key to prevent duplicate processing.

200

Detailed quote including fees, exchange rate, and expiration.

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
     --url https://core.nadapay.io/api/v1/transactions/quote \
3
     --header 'content-type: application/json'
```

Click `Try It!` to start a request and see the response here!

Updated 3 months ago

---

Did this page help you?

Yes

No