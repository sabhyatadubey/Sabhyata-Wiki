---
summary: Customer segmentation by vertical and behaviour feeding into CRM campaigns.
status: Active
last_updated: 17.04.2026
---

# Segmentation

## Current Status

Segmentation is operational at the vertical level, with campaigns targeted by service category. Adjust campaign parameters reveal segmentation dimensions in use. CleverTap is the segmentation and journey platform.

## Active Segmentation Dimensions

Inferred from campaign UTM and Adjust parameters:
- **Channel**: Email, WhatsApp, Push
- **Language**: EN (primary), All
- **Country**: UAE
- **Vertical**: Home Cleaning, Beauty for Her, IV Therapy, Lab Tests, Spa, Premium Grooming, Pet Healthcare, etc.
- **Occasion**: Valentine's, general ad-hoc

## Segment-to-Campaign Flow

1. Segment defined in CleverTap by vertical + recency/lapse status
2. Campaign or journey triggered with vertical-specific deep link and voucher
3. Attribution tracked via Adjust tracker `11yc028z_11tq6grd`

## Open Items

| Item | Owner | Status |
|---|---|---|
| Document segment definitions per vertical in CleverTap | Sabhyata | [OPEN] |
| Add neighbourhood-level segmentation (in A/B test) | Sabhyata | In progress |

## Backlinks

- [[people/sabhyata]]
- [[workstreams/email-sms]]
- [[workstreams/reengagement]]
- [[experiments/subject-line-personalisation]]
