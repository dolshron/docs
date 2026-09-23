# Source: https://docs.nadapay.io/reference/invoicecontroller_create

| Time | Status | User Agent | |
| :-- | :-- | :-- | :-- |
| 
Retrieving recent requests…

 |

Loading…

#### URL Expired

The URL for this request expired after 30 days.

customerId

string

required

[Skip link to customerId](https://docs.nadapay.io/reference/invoicecontroller_create#body-params-customerId)

number

string

required

[Skip link to number](https://docs.nadapay.io/reference/invoicecontroller_create#body-params-number)

issueDate

string

required

[Skip link to issueDate](https://docs.nadapay.io/reference/invoicecontroller_create#body-params-issueDate)

dueDate

string

required

[Skip link to dueDate](https://docs.nadapay.io/reference/invoicecontroller_create#body-params-dueDate)

currency

string

required

[Skip link to currency](https://docs.nadapay.io/reference/invoicecontroller_create#body-params-currency)

items

array of objects

required

[Skip link to items](https://docs.nadapay.io/reference/invoicecontroller_create#body-params-items)

items\*

ADD object

taxRate

number

[Skip link to taxRate](https://docs.nadapay.io/reference/invoicecontroller_create#body-params-taxRate)

taxName

string

[Skip link to taxName](https://docs.nadapay.io/reference/invoicecontroller_create#body-params-taxName)

discountValue

number

[Skip link to discountValue](https://docs.nadapay.io/reference/invoicecontroller_create#body-params-discountValue)

discountType

string

[Skip link to discountType](https://docs.nadapay.io/reference/invoicecontroller_create#body-params-discountType)

settlementAccountId

string

required

[Skip link to settlementAccountId](https://docs.nadapay.io/reference/invoicecontroller_create#body-params-settlementAccountId)

paymentMethods

array of strings

required

[Skip link to paymentMethods](https://docs.nadapay.io/reference/invoicecontroller_create#body-params-paymentMethods)

paymentMethods\*

ADD string

notesToClient

string

[Skip link to notesToClient](https://docs.nadapay.io/reference/invoicecontroller_create#body-params-notesToClient)

internalNotes

string

[Skip link to internalNotes](https://docs.nadapay.io/reference/invoicecontroller_create#body-params-internalNotes)

sendEmailReminder

boolean

[Skip link to sendEmailReminder](https://docs.nadapay.io/reference/invoicecontroller_create#body-params-sendEmailReminder)

truefalse

allowPartialPayment

boolean

[Skip link to allowPartialPayment](https://docs.nadapay.io/reference/invoicecontroller_create#body-params-allowPartialPayment)

truefalse

sendNow

boolean

[Skip link to sendNow](https://docs.nadapay.io/reference/invoicecontroller_create#body-params-sendNow)

If true, transitions to SENT immediately and triggers email

truefalse

scheduledAt

string

[Skip link to scheduledAt](https://docs.nadapay.io/reference/invoicecontroller_create#body-params-scheduledAt)

Schedule the invoice to be sent at this date

metadata

object

[Skip link to metadata](https://docs.nadapay.io/reference/invoicecontroller_create#body-params-metadata)

metadata object

# 

201

Invoice created successfully.

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
     --url https://core.nadapay.io/api/v1/organization/invoices \
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