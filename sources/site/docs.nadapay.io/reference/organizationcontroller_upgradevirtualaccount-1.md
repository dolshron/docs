# Source: https://docs.nadapay.io/reference/organizationcontroller_upgradevirtualaccount-1

| Time | Status | User Agent | |
| :-- | :-- | :-- | :-- |
| 
Retrieving recent requests…

 |

Loading…

#### URL Expired

The URL for this request expired after 30 days.

currency

string

required

[Skip link to currency](https://docs.nadapay.io/reference/organizationcontroller_upgradevirtualaccount-1#body-params-currency)

Currency of the fiat account to upgrade (e.g., USD)

x-idempotency-key

string

[Skip link to x-idempotency-key](https://docs.nadapay.io/reference/organizationcontroller_upgradevirtualaccount-1#header-params-x-idempotency-key)

Unique key to prevent duplicate processing.

200

Virtual account details (account number, bank name) successfully provisioned.

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
     --url https://core.nadapay.io/api/v1/organizations/upgrade-virtual-account \
3
     --header 'content-type: application/json'
```

Click `Try It!` to start a request and see the response here!

Updated 3 months ago

---

Did this page help you?

Yes

No