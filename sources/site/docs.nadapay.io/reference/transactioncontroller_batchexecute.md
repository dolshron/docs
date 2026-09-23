# Source: https://docs.nadapay.io/reference/transactioncontroller_batchexecute

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

[Skip link to source](https://docs.nadapay.io/reference/transactioncontroller_batchexecute#body-params-source)

Source account details

source object

reason

string

enum

required

[Skip link to reason](https://docs.nadapay.io/reference/transactioncontroller_batchexecute#body-params-reason)

Reason for the transaction

giftbillsgroceriestravelhealthentertainmenthousingschool-feesConversionother

Show 10 enum values

reasonDescription

string

[Skip link to reasonDescription](https://docs.nadapay.io/reference/transactioncontroller_batchexecute#body-params-reasonDescription)

Reason description if others is selected as reason

metadata

object

[Skip link to metadata](https://docs.nadapay.io/reference/transactioncontroller_batchexecute#body-params-metadata)

Additional metadata

metadata object

payouts

array of objects

required

[Skip link to payouts](https://docs.nadapay.io/reference/transactioncontroller_batchexecute#body-params-payouts)

payouts\*

ADD object

x-idempotency-key

string

[Skip link to x-idempotency-key](https://docs.nadapay.io/reference/transactioncontroller_batchexecute#header-params-x-idempotency-key)

Unique key to prevent duplicate processing.

202

Batch payout successfully queued for background execution.

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
     --url https://core.nadapay.io/api/v1/transactions/batch \
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