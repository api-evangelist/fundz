---
name: Sweep every Fundz signal type for a target account list
description: >-
  Fan out across all six Fundz event feeds to assemble a complete signal picture for a set of
  target companies — funding, M&A, executive moves, partnerships, product launches and
  crowdfunding — and correlate the results on the shared organization identifier.
api: openapi/fundz-fundings-api-openapi.yml
operations: [listFundings, listAcquisitions, listExecutiveAppointments, listAgreements, listProductLaunches, listCrowdfundings]
generated: '2026-08-14'
method: generated
source: openapi/_original/fundz-openapi.json, data-model/fundz-data-model.yml, conventions/fundz-conventions.yml
---

# Sweep every Fundz signal type for a target account list

Use this when the job is "what has happened lately at these companies" rather than "who just
raised". The Fundz API has no cross-signal query on its spec'd surface: six feeds, one event type
each. Assembling a company view means calling all six and joining the results yourself.

## Before you start

- **Base URL** `https://api.fundz.net`. **Auth**: raw key in the `Authorization` header, no
  `Bearer` prefix.
- **Budget the calls first.** Six feeds × N pages each, against 50 calls/day on Pro or 500 on
  Strategic. A naive full sweep exhausts a Pro key quickly.

## The six operations

| operationId | Path | Event |
|---|---|---|
| `listFundings` | `GET /fundings` | Funding rounds, with investors and amount |
| `listAcquisitions` | `GET /acquisitions` | M&A, with `acquirers[]` and `acquirees[]` |
| `listExecutiveAppointments` | `GET /executives` | Executive hires and appointments |
| `listAgreements` | `GET /agreements` | Partnerships, distribution, licensing, JVs |
| `listProductLaunches` | `GET /products` | Product and feature launches |
| `listCrowdfundings` | `GET /crowdfundings` | SEC Form C / Form 1-A campaigns |

## Steps

1. **Narrow before you fan out.** All six feeds accept the shared filters `created_from`,
   `created_to`, `keywords`, `locations`, `industries` and `page`. Set `created_from` to your
   window first — an unfiltered sweep pages through the entire firehose.

2. **Call each feed for the window.** Same envelope every time:
   `{_attribution, _licensing, data[], meta, upgrade_url}`, 25 records per page, newest first.

3. **Join on the organization.** Four of the six feeds — `listFundings`,
   `listExecutiveAppointments`, `listAgreements`, `listProductLaunches` — carry a full
   `organization` object. **`organization.id` is the join key**: a stable slug such as `onelayer`,
   documented as safe to deduplicate on. `organization.domain.name` is the key to join Fundz
   against your CRM or any external dataset.

4. **Handle the two feeds that break the pattern.**
   - `listAcquisitions` has **no** `organization` object. It carries `acquirers[]` and
     `acquirees[]` — an M&A event is many-to-many between companies, so match by name, not by id.
   - `listCrowdfundings` has no `organization` either. It carries the issuer inline
     (`issuer_name`, `issuer_organization`, `issuer_website`) because the SEC filer may not resolve
     to a tracked company. Note the field is spelled `offerred_type` in the contract.

5. **Order the merged timeline on `created_at`.** It is the one field present on every event type,
   and it means "when Fundz published this", not "when it happened".

6. **Watch quota across the whole sweep.** `meta.remaining_searches` decrements across feeds — it
   is one account-level allowance, not one per endpoint. Re-read it after every call and stop the
   sweep before it hits zero rather than after the 429.

## If you need one company rather than a list

The provider documents `GET /companies/{id}` — one call returning the enriched company plus a
`signals` object with the latest of each event type, a `counts` summary and `last_signal_at`. That
is one call instead of six.

**It is not in the OpenAPI.** Neither is `GET /fund-formations`. Both are documented in prose only
at `https://app.fundz.net/knowledge/api-references/companies`. Use them if you can accept a
contract that is not machine-readable; stay on the six spec'd feeds if you cannot.

## Rules

- Empty queries are free — they return a `guidance` object and do not decrement quota. Probe with
  narrow filters before committing to pagination.
- Do not assume every event type will fire for a company. Most companies have `[]` on most feeds.
- Display `_attribution` wherever you surface the data; redistribution needs a licence.
- On 429 the body is `{error, current_tier, queries_limit, remaining_searches, upgrade_url}` — not
  the `{type, message}` shape the other errors use. Branch on status before parsing.
