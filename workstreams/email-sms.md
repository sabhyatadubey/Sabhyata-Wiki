---
summary: Multi-channel CRM campaign operations across Email, WhatsApp, and Push for Justlife UAE.
status: Active
last_updated: 17.04.2026
---

# Email, WhatsApp & Push Campaigns

## Current Status

Active across three channels: Email, WhatsApp, and Push notifications. Campaigns managed via CleverTap. Attribution tracked via Adjust. Two app schemes in use: `justlife://` (current) and `justmop://` (legacy). All campaigns target UAE.

## Active Verticals

Campaigns actively running or recently tested across:
- Home Cleaning
- Beauty for Her
- IV Therapy at Home
- Lab Tests at Home
- Spa Treatments
- Premium Grooming (Men's)
- Pet Healthcare
- Men's Spa
- Furniture Cleaning
- Home Painting
- Packers & Movers
- Doctor at Home

## Campaign Naming Convention

`Channel:[Channel]_Language:[Lang]_Country:[Country]_City:[City]_Vertical:[Vertical]_Name:[DDMMYYYY]-[Description]`

Example: `Adhoc_UAE_HC_Whatsapp_20250630`

## Campaign Types

- **Ad-hoc**: One-off promotional sends
- **Automation**: Trigger-based journeys (e.g. lab test, IV therapy journeys in CleverTap)

## Active Journeys (CleverTap)

- Health Journey (IV + Lab) — set up 20.02.2026
- Beauty Journey — set up 20.02.2026

## Vouchers Active (Jan–Apr 2026)

| Voucher | Vertical | Channel |
|---|---|---|
| 25FURN | Furniture Cleaning | — |
| 50PETS | Pet Healthcare | — |
| VPET100 | Pet Healthcare | — |
| VDAY200 | IV Therapy | — |
| VAL60 / VLOVE60 | Beauty for Her (Valentine's) | — |
| MENLOVE60 | Premium Grooming (Valentine's) | — |
| LOVE90 | Spa Treatments (Valentine's) | — |
| NYGLAM | Beauty for Her | — |
| FOCUSIV | IV Therapy (NAD 100mg) | Email |
| NADIV | IV Therapy (NAD 100mg) | WhatsApp |
| WIPE40 | Home Cleaning | — |
| 30LESS | Home Cleaning | WhatsApp |
| CARE10 | Home Cleaning | — |
| JLAB60 | Lab Tests | — |
| TEST4LESS | Lab Tests | WhatsApp |
| DOC4LESS | Doctor at Home | — |
| SALONVIBE | Beauty for Her | — |
| MNS60 | Premium Grooming | — |
| SPALL | Spa Treatments | — |
| IVT150 | IV Therapy | — |
| LABT60 | Lab Tests | — |
| 4YOU | Home (general) | Email |

## A/B Tests Active (as of 02.04.2026)

See [[experiments/]] for full details. Five tests planned:
1. Subject line personalisation (neighbourhood mentions) — Beauty, SV, HC
2. Discount callout in subject line — Beauty, SV (priority)
3. Creative & banner testing — Beauty (GIF + banner variation, priority)
4. Health: symptom curiosity messaging
5. Health: IV Therapy attribute test (priority)

## Blockers

- Deep link format inconsistency: both `justlife://` and `justmop://` schemes in use — must verify correct scheme per campaign before send
- Voucher URL format bug: `4YOU?utm_source=...` seen instead of `4YOU&utm_source=...` (02.02.2026)

## Open Items

| Item | Owner | Status |
|---|---|---|
| Confirm correct app scheme for each campaign | Sabhyata | Ongoing |
| Prioritise 4 priority A/B tests | Sabhyata | In progress |
| Inform brand team to start A/B test creatives | Sabhyata | Pending approval (02.04.2026) |

## Backlinks

- [[people/sabhyata]]
- [[experiments/subject-line-personalisation]]
- [[experiments/discount-callout-subject-line]]
- [[experiments/beauty-banner-gif-test]]
- [[experiments/health-symptom-curiosity]]
- [[experiments/iv-therapy-attribute-test]]
- [[workstreams/reengagement]]
