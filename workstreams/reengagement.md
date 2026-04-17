---
summary: Lapsed customer re-engagement via voucher-led campaigns across Email, WhatsApp, and Push.
status: Active
last_updated: 17.04.2026
---

# Re-engagement

## Current Status

Re-engagement is operated primarily through voucher-based campaigns across Email, WhatsApp, and Push. Campaigns are deployed via CleverTap and tracked via Adjust. Active across multiple verticals. No reactivation rate numbers available from source yet.

## Segments Being Targeted

Inferred from campaign activity Jan–Apr 2026:
- Lapsed home cleaning customers (vouchers: WIPE40, 30LESS, CARE10)
- Lapsed beauty customers (SALONVIBE, NYGLAM, VAL60)
- Lapsed health customers (NADIV, FOCUSIV, TEST4LESS, DOC4LESS, IVT150, LABT60)
- Lapsed pet care customers (50PETS, VPET100)
- Seasonal / occasion-based lapsed customers (Valentine's: VDAY200, VLOVE60, MENLOVE60, LOVE90)

## Campaign Mechanics

- Voucher codes embedded in deep links sent via Email, WhatsApp, or Push
- Deep links route directly to vertical checkout with voucher pre-applied
- `flex=true` parameter used on most links (flexible scheduling)
- Attribution tracked with Adjust tracker (`adj_t` parameter)

## Open Items

| Item | Owner | Status |
|---|---|---|
| Establish baseline reactivation rate per vertical | Sabhyata | [OPEN] |
| Track voucher redemption rate per campaign | Sabhyata | [OPEN] |

## Backlinks

- [[people/sabhyata]]
- [[workstreams/email-sms]]
- [[workstreams/segmentation]]
