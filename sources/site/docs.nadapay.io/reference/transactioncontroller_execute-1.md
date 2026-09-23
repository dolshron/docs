# Source: https://docs.nadapay.io/reference/transactioncontroller_execute-1

| Time | Status | User Agent | |
| :-- | :-- | :-- | :-- |
| 
Retrieving recent requests…

 |

Loading…

#### URL Expired

The URL for this request expired after 30 days.

quoteId

string

[Skip link to quoteId](https://docs.nadapay.io/reference/transactioncontroller_execute-1#body-params-quoteId)

Quote ID received from the quote endpoint

reason

string

enum

required

[Skip link to reason](https://docs.nadapay.io/reference/transactioncontroller_execute-1#body-params-reason)

Reason for the transaction

giftbillsgroceriestravelhealthentertainmenthousingschool-feesConversionother

Show 10 enum values

reasonDescription

string

[Skip link to reasonDescription](https://docs.nadapay.io/reference/transactioncontroller_execute-1#body-params-reasonDescription)

Reason description if others is selected as reason

metadata

object

[Skip link to metadata](https://docs.nadapay.io/reference/transactioncontroller_execute-1#body-params-metadata)

Additional metadata

metadata object

source

object

required

[Skip link to source](https://docs.nadapay.io/reference/transactioncontroller_execute-1#body-params-source)

source object

destination

object

required

[Skip link to destination](https://docs.nadapay.io/reference/transactioncontroller_execute-1#body-params-destination)

destination object

x-idempotency-key

string

[Skip link to x-idempotency-key](https://docs.nadapay.io/reference/transactioncontroller_execute-1#header-params-x-idempotency-key)

Unique key to prevent duplicate processing.

201

Transaction successfully initiated and queued for execution.

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
     --url https://core.nadapay.io/api/v1/transactions/execute \
3
     --header 'content-type: application/json' \
4
     --data '{"reason":"gift"}'
```

Click `Try It!` to start a request and see the response here!

Updated 3 months ago

---

Did this page help you?

Yes

No