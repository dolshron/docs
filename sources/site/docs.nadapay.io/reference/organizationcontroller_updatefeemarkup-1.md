# Source: https://docs.nadapay.io/reference/organizationcontroller_updatefeemarkup-1

| Time | Status | User Agent | |
| :-- | :-- | :-- | :-- |
| 
Retrieving recent requests…

 |

Loading…

#### URL Expired

The URL for this request expired after 30 days.

txType

string

enum

required

[Skip link to txType](https://docs.nadapay.io/reference/organizationcontroller_updatefeemarkup-1#body-params-txType)

PAYOUTDEPOSITFX\_SWAP

Allowed:

`PAYOUT``DEPOSIT``FX_SWAP`

markupBps

number

required

[Skip link to markupBps](https://docs.nadapay.io/reference/organizationcontroller_updatefeemarkup-1#body-params-markupBps)

Markup in basis points (50 = 0.5%)

reason

string

[Skip link to reason](https://docs.nadapay.io/reference/organizationcontroller_updatefeemarkup-1#body-params-reason)

x-idempotency-key

string

[Skip link to x-idempotency-key](https://docs.nadapay.io/reference/organizationcontroller_updatefeemarkup-1#header-params-x-idempotency-key)

Unique key to prevent duplicate processing.

200

Fee markup configuration updated.

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
     --url https://core.nadapay.io/api/v1/organizations/fees \
3
     --header 'content-type: application/json' \
4
     --data '{"txType":"PAYOUT"}'
```

Click `Try It!` to start a request and see the response here!

Updated 3 months ago

---

Did this page help you?

Yes

No