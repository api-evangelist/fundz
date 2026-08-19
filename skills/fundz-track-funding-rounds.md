---
name: Track new funding rounds with Fundz
description: >-
  Poll the Fundz funding feed incrementally to pick up new venture and private-equity rounds as
  they are published, filtered to a target profile, without re-reading events you have already seen.
api: openapi/fundz-fundings-api-openapi.yml
operations: [listFundings]
generated: '2026-08-14'
method: generated
source: openapi/_original/fundz-openapi.json, https://app.fundz.net/knowledge/api-references/fundings, conventions/fundz-conventions.yml
---

# Track new funding rounds with Fundz

Use this when the job is "tell me who just raised", scoped to a territory, industry, stage or
cheque size. The Fundz funding feed is newest-first and event-shaped: each record is one round,
carrying the investors, the amount, the stated use of proceeds, and a `source_url` back to the
press release or filing it was extracted from.

## Before you start

- **Base URL** is `https://api.fundz.net`.
- **Auth** is the API key as the **raw** value of the `Authorization` header. There is **no
  `Bearer` prefix** on this surface. `Authorization: YOUR_API_KEY`.
- The core API is **paid plans only** — Pro (50 calls/day) or Strategic (500 calls/day). A 401
  means either a bad key *or* a lapsed subscription; read the message before assuming the
  credential is wrong.
- Every response carries `_attribution` and `_licensing`. If you surface this data to a user,
  display the attribution. Redistribution or embedding requires a licence.

## Steps

1. **Call `listFundings`** — `GET /fundings`.

   Filter with any combination of: `created_from`, `created_to`, `series`, `money_raised_min`,
   `money_raised_max`, `number_of_employees_min`, `number_of_employees_max`, `locations`,
   `industries`, `investors`, `keywords`, `offered_types`, `page`.

   ```
   GET /fundings?series=Series%20A&money_raised_min=5000000&locations=California&created_from=2026-08-01
   ```

2. **Read the envelope, not just the array.** The body is
   `{_attribution, _licensing, data[], meta, upgrade_url}`. `data[]` holds at most **25** records.

3. **Page with `meta.next_page`.** Pages are 1-based via `?page=N`. Stop when `meta.next_page` is
   `null`. `meta.total_count` and `meta.total_pages` tell you the size of the result set before you
   commit calls to it — check them first, because on Pro you only have 50 calls a day and each page
   costs one.

4. **Go incremental with `created_from`.** `created_at` is when Fundz *published* the event, in
   UTC, and it is the documented field to poll on. Store the highest `created_at` you have
   processed and pass it as `created_from` on the next run. The feed is sorted newest-first, so the
   first page of a fresh poll holds the newest events.

5. **Deduplicate on `id`.** Each record's `id` is a stable slug
   (`onelayer-funding-round-series-a-4b2c1a`) documented as safe to use as a deduplication key.
   `created_from` is date-granular (`YYYY-MM-DD`), so a daily poll *will* re-deliver events you
   have already seen — the id is what makes the poll idempotent on your side.

6. **Pace against quota.** Every successful response carries `meta.remaining_searches` and
   `meta.tier`. Read them; do **not** hardcode per-plan numbers. There are no `RateLimit-*` response
   headers on this API, so the body is the only runtime signal you get.

## Rules

- **A query that returns nothing does not cost you a call.** The response carries a `guidance`
  object with suggestions instead. Broad exploratory queries are cheap; wide pagination is not.
- **`money_raised` is a display string** (`"$40 Million"`, `"$28,000,000"`), not a number. Filter
  on `money_raised_min`/`money_raised_max` server-side rather than parsing it client-side.
- **`series` values vary in the wild** — `"Seed"`, `"Series A"`, `"Venture - Series Unknown"`. Match
  loosely; do not assume a closed enum.
- **Nulls are normal.** `organization.founded`, `linkedin_url`, `ticker` and `money_raised` are all
  nullable. `use_of_proceeds` is frequently `[]`.
- **Attribute every number you display** to `source_url`. That field is why this data holds up in
  front of an end user.

## Errors

| Status | Body | What to do |
|---|---|---|
| 401 | `{type, message}` | Bad key **or** inactive subscription. Message points at fundz.net/pricing. |
| 403 | `{type, message}` | Missing, invalid, orphaned or non-entitled key. |
| 429 | `{error, current_tier, queries_limit, remaining_searches, upgrade_url}` | **Different shape.** Daily quota exhausted. There is no `Retry-After` — back off to the next quota window. |
| 500 | (no body schema) | Retry once, then stop. |

A client that only parses `type`/`message` **will fail to read a 429**. Branch on the status code
before you parse.
