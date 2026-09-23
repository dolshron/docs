# Source: https://docs.nadapay.io/docs/get-available-markets

## 

Why this matters

[Skip link to Why this matters](https://docs.nadapay.io/docs/get-available-markets#why-this-matters)

Corridor availability can change per provider and per channel. Query this endpoint dynamically rather than assuming a fixed list is always accurate.

## 

Request

[Skip link to Request](https://docs.nadapay.io/docs/get-available-markets#request)

Bash

```
curl --request GET \
  --url "$baseUrl/api/v1/public/markets?channel=PAYOUT&isActive=true" \
  --header 'x-api-key: YOUR_API_KEY'
```

| Query param | Type | Required | Description |
| --- | --- | --- | --- |
| `channel` | `"COLLECTION"` | `"PAYOUT"` | `"SWAP"` | No | Filter by channel |
| `isActive` | boolean | No | Filter to only currently active corridors |

This is a **public** endpoint — confirm with your team whether it requires `x-api-key` in your environment, or is fully open.

## 

Currently supported currencies

[Skip link to Currently supported currencies](https://docs.nadapay.io/docs/get-available-markets#currently-supported-currencies)

At time of writing, the following currencies are available across deposit and payout corridors (subject to change; always confirm against a live call to this endpoint before relying on any specific currency in production):

| | Code | Type |
| --- | --- | --- |
| ![XOF](https://flagcdn.com/20x15/sn.png) | XOF | Fiat |
| ![BWP](https://flagcdn.com/20x15/bw.png) | BWP | Fiat |
| ![BRL](https://flagcdn.com/20x15/br.png) | BRL | Fiat |
| ![XAF](https://flagcdn.com/20x15/cm.png) | XAF | Fiat |
| ![CDF](https://flagcdn.com/20x15/cd.png) | CDF | Fiat |
| ![EUR](https://flagcdn.com/20x15/eu.png) | EUR | Fiat |
| ![GHS](https://flagcdn.com/20x15/gh.png) | GHS | Fiat |
| ![KES](https://flagcdn.com/20x15/ke.png) | KES | Fiat |
| ![MWK](https://flagcdn.com/20x15/mw.png) | MWK | Fiat |
| ![MXN](https://flagcdn.com/20x15/mx.png) | MXN | Fiat |
| ![NGN](https://flagcdn.com/20x15/ng.png) | NGN | Fiat |
| ![RWF](https://flagcdn.com/20x15/rw.png) | RWF | Fiat |
| ![TZS](https://flagcdn.com/20x15/tz.png) | TZS | Fiat |
| ![ZAR](https://flagcdn.com/20x15/za.png) | ZAR | Fiat |
| ![UGX](https://flagcdn.com/20x15/ug.png) | UGX | Fiat |
| ![AED](https://flagcdn.com/20x15/ae.png) | AED | Fiat |
| ![USD](https://flagcdn.com/20x15/us.png) | USD | Fiat |
| ![ZMW](https://flagcdn.com/20x15/zm.png) | ZMW | Fiat |
| ![USDC](https://assets.coingecko.com/coins/images/6319/small/usdc.png) | USDC | Stablecoin |
| ![USDT](https://assets.coingecko.com/coins/images/325/small/Tether.png) | USDT | Stablecoin |

## 

Response

[Skip link to Response](https://docs.nadapay.io/docs/get-available-markets#response)

Returns the list of active markets matching your filter, including the currency, channel, and provider availability for each.

## 

Best practices

[Skip link to Best practices](https://docs.nadapay.io/docs/get-available-markets#best-practices)

- Filter by `channel=COLLECTION`, `channel=PAYOUT`, or `channel=SWAP` separately if your product needs to show different options per flow direction.
- Re-check `isActive` at the point of transaction, not just once at app startup — corridors can be paused.

## 

Call this next

[Skip link to Call this next](https://docs.nadapay.io/docs/get-available-markets#call-this-next)

- [Get Supported Networks](https://docs.nadapay.io/docs/get-supported-networks) _(Payments API)_ — once you know the country/currency, get the specific rails available
- [Check Transaction Limits](https://docs.nadapay.io/docs/check-transaction-limits) _(Payments API)_

Updated 14 days ago

---

Did this page help you?

Yes

No

Copy Page