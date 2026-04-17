# Bootstrap Prompt

Copy everything below the line into Claude Code to generate your wiki. Customize the sections marked with `<!-- CUSTOMIZE -->` before running.

---

You are doing a one-time bootstrap job. You will populate this repo with a structured knowledge wiki based on my operational history.

## STEP 1 — CONFIGURE

<!-- CUSTOMIZE: Set your data source -->
**Primary source:** Slack channel `D060DM1A9FT`
**Date range:** Fetch all messages from `2026-01-01` onwards
**Source type:** Daily CRM updates, campaign briefings, and operational notes from Sabhyata (CRM Executive, Justlife, India)

## STEP 2 — CREATE FOLDER STRUCTURE

```bash
mkdir -p workstreams people experiments decisions metrics
```

## STEP 3 — FETCH SOURCE MATERIAL

Use the Slack MCP tool to read channel `D060DM1A9FT`. Fetch all messages using pagination until you have everything from 2026-01-01 onwards. These are your source of truth. Do not invent or assume anything not explicitly stated in these messages.

## STEP 4 — CREATE ARTICLES

For each category below, extract everything relevant from the source history and write structured articles. Use only what appears in the source. Be specific. Include real numbers. Every article must have YAML frontmatter, content body, and a Backlinks section.

### Workstreams

**workstreams/retention.md** — Include: current retention rate, active retention campaigns, churn signals, interventions in progress, blockers, open items.

**workstreams/reengagement.md** — Include: lapsed customer segments being targeted, campaign mechanics, reactivation rate, active outreach, results to date.

**workstreams/email-sms.md** — Include: active email and SMS campaigns, send volumes, open rates, CTR, conversion rates, upcoming sends, A/B tests running.

**workstreams/loyalty-program.md** — Include: program status, active tiers or rewards, member counts, redemption rates, open items.

**workstreams/segmentation.md** — Include: active customer segments, segmentation logic, how segments feed into campaigns, any data quality issues.

**workstreams/onboarding.md** — Include: new customer onboarding flow, drop-off points, activation rate, open items and improvements in progress.

### People

**people/sabhyata.md** — Include: role (CRM Executive), ownership areas (retention, re-engagement, email/SMS, loyalty, segmentation, onboarding), open items, decisions made, key initiatives owned.

Extract any other team members mentioned in the source messages and create a people article for each. Include their role, ownership areas, open items assigned to them, and delivery patterns observed.

### Experiments

Extract every CRM experiment mentioned in the source. For each, create **experiments/[name].md** including: hypothesis, mechanic (audience, channel, variant), results with numbers (open rate, CTR, conversion, reactivation %), status (Active / Resolved), and next step.

Examples of what to look for:
- Email subject line A/B tests
- SMS vs email channel comparisons
- Discount vs no-discount re-engagement tests
- Loyalty reward structure experiments
- Onboarding sequence timing tests
- Push notification experiments

### Decisions Log

**decisions/log.md** — Format every entry as:

```
## DD.MM.YYYY

**Decision title**
What was decided, one to three sentences max. Source: [which message/meeting].
```

Extract every clear decision from all source messages in chronological order.

### Metrics

**metrics/definitions.md** — Define every CRM metric mentioned across source messages. At minimum define: Retention Rate, Churn Rate, Repeat Booking Rate, Reactivation Rate, Email Open Rate, Email CTR, SMS CTR, Campaign Conversion Rate, CLV (Customer Lifetime Value), NPS, Loyalty Redemption Rate. For each: name, definition as used at Justlife, current benchmark or target.

**metrics/weekly-benchmarks.md** — Extract every number mentioned as a target or threshold. Format as a table: Metric | Target/Threshold | Source | Date mentioned.

## STEP 5 — CREATE INDEX

Write `index.md` as a full catalog of every article created:

```markdown
# Wiki Index

Last updated: [today's date DD.MM.YYYY]
Source: [your source description]

## Workstreams
* [[workstreams/name]] - [one-line summary] | [status]

## People
* [[people/name]] - [one-line summary] | Active

## Experiments
* [[experiments/name]] - [one-line summary] | [status]

## Decisions
* [[decisions/log]] - Chronological log of all decisions

## Metrics
* [[metrics/definitions]] - Metric definitions and benchmarks
* [[metrics/weekly-benchmarks]] - Current targets and thresholds
```

## STEP 6 — CREATE LOG

Write `log.md`:

```markdown
# Wiki Log

## [today's date] bootstrap

Initial wiki created from [source description], covering [date range].
Articles created: [count per folder]. Source messages processed: [count].
```

## STEP 7 — GENERATE state.md

Using all articles you just created, generate the initial state.md. This is a compressed snapshot of current state for token-efficient loading.

Populate:
- CRITICAL/URGENT/HIGH sections: extract any items with hard deadlines or marked as urgent in the source
- Workstream Status table: one row per workstream article you created, current status from the article
- Open Items table: every open item across all workstream and people articles, with owner and estimated days open
- Active Experiments: any experiment with status Active or Pending decision
- People Watch List: people with open items assigned to them
- Key Metrics: every metric with a current known value from metrics/weekly-benchmarks.md

state.md is always a full rewrite. Generate it fresh from the wiki you just built.

## STEP 8 — COMMIT AND PUSH

```bash
git add .
git commit -m "bootstrap: initial wiki from [source] [date range]"
git push -u origin main
```

## STEP 9 — FINAL OUTPUT

After pushing, print:
1. GitHub repo URL
2. Article count per folder
3. Any gaps where source data was thin or missing
4. The raw base URL for fetching articles: `https://raw.githubusercontent.com/USERNAME/REPO/main/`
5. The Step 0 line to add to your agent prompts, with the real index.md URL
