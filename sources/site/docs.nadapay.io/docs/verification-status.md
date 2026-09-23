# Source: https://docs.nadapay.io/docs/verification-status

## 

Request

[Skip link to Request](https://docs.nadapay.io/docs/verification-status#request)

Bash

```
curl --request GET \
  --url $baseUrl/organizations/verification/KYB \
  --header 'x-api-key: YOUR_API_KEY'
```

## 

Response

[Skip link to Response](https://docs.nadapay.io/docs/verification-status#response)

JSON

```
{
  "data": {
    "status": "approved",
    "type": "kyb",
    "verified_at": "2026-01-01T00:00:00Z",
    "details": {
      "business_name": "Acme Corp",
      "country": "NG"
    }
  }
}
```

## 

Status values

[Skip link to Status values](https://docs.nadapay.io/docs/verification-status#status-values)

| Status | Meaning | Can transact in production? |
| --- | --- | --- |
| `pending` | Not yet submitted | ❌ |
| `review` | Submitted, under review | ❌ |
| `approved` | Verification passed | ✅ |
| `rejected` | Verification was rejected | ❌ |
| `failed` | Verification attempt failed | ❌ |

## 

Handling each status

[Skip link to Handling each status](https://docs.nadapay.io/docs/verification-status#handling-each-status)

- `pending` — direct the org to submit onboarding info before attempting live processing
- `review` — keep the org in a non-transacting state; poll at a reasonable interval, don't retry aggressively
- `approved` — cleared to transact; proceed with funding, beneficiaries, and execution in production
- `rejected` — review the returned `details`, correct the issue, and resubmit through the approved channel
- `failed` — treat as blocking; review response details before retrying or escalating

> **Sandbox note:** organizations are automatically approved in sandbox mode.

## 

Recheck until resolved

[Skip link to Recheck until resolved](https://docs.nadapay.io/docs/verification-status#recheck-until-resolved)

If status is `review`, re-run the same request until it changes to `approved`, `rejected`, or `failed`.

Updated 2 months ago

---

Did this page help you?

Yes

No

Copy Page