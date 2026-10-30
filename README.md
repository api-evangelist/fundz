# Fundz

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Fundz is an event-first business intelligence platform, founded 2015, tracking 200,000+ companies and surfacing funding rounds, executive changes, M&A activity, SEC filings (8-K, 10-K, 10-Q, Form D) and website modifications in real time. Rather than storing millions of static records it focuses on companies showing active signals, and scores them against each user's criteria. The API exposes company profiles, fundings, SEC filings and fund formations from api.fundz.net with an API key in the Authorization header. It sits in the same category as Harmonic and Crunchbase, and competes explicitly on access: an API key is free and issued instantly with no card and no sales call, and pricing is published rather than quoted. Fundz also ships an MCP server listed on the official Model Context Protocol registry, and publishes an llms.txt.

**Areas:** Business Intelligence · Funding · Private Markets · Mergers and Acquisitions · SEC Filings · Signals · Sales Intelligence · MCP · Agents

## Fundz on APIs.io

Everything profiled for Fundz is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/fundz/](https://apis.io/providers/fundz/)** — or go straight to one of the APIs or properties below.

### APIs (8)

- [Fundz API](https://apis.io/apis/fundz/fundz-api/) — Company profiles, funding rounds, SEC filings and fund formations, keyed to real-time business events.
- [Fundz Acquisitions API](https://apis.io/apis/fundz/fundz-acquisitions-api/) — Company acquisitions and M&A events, with acquirer and target organization records where disclosed.
- [Fundz Agreements API](https://apis.io/apis/fundz/fundz-agreements-api/) — Business agreements and partnerships announced by companies — distribution, licensing, joint ventures and similar.
- [Fundz Crowdfundings API](https://apis.io/apis/fundz/fundz-crowdfundings-api/) — Regulation CF and Regulation A crowdfunding campaigns, sourced from SEC Form C and Form 1-A filings.
- [Fundz Executives API](https://apis.io/apis/fundz/fundz-executives-api/) — Executive hires and appointments — new C-level, VP and board appointments at private and public companies.
- [Fundz Fundings API](https://apis.io/apis/fundz/fundz-fundings-api/) — Funding rounds — seed through late-stage venture and private equity — with the investors on the round and the full organization record.
- [Fundz Products API](https://apis.io/apis/fundz/fundz-products-api/) — Product launches and major product announcements.
- [FundzWatch API](https://apis.io/apis/fundz/fundzwatch-api/) — The agent-facing Fundz surface, served on the same host under /v1/watch/*: AI-scored leads matched to an ICP, a raw business-event feed, a company…

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Fundz Webhooks](https://apis.io/asyncapis/fundz/fundz-webhooks/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [io.github.Fund-z/fundzwatch](https://apis.io/servers/fundz/io-github-fund-z-fundzwatch/)

#### Collections (6)

Postman and Open Collection request collections.

- [Fundz Acquisitions API](https://apis.io/collections/fundz/open-fundz-acquisitions-api/)
- [Fundz Agreements API](https://apis.io/collections/fundz/open-fundz-agreements-api/)
- [Fundz Crowdfundings API](https://apis.io/collections/fundz/open-fundz-crowdfundings-api/)
- [Fundz Executives API](https://apis.io/collections/fundz/open-fundz-executives-api/)
- [Fundz Fundings API](https://apis.io/collections/fundz/open-fundz-fundings-api/)
- [Fundz Products API](https://apis.io/collections/fundz/open-fundz-products-api/)

#### Overlays (6)

OpenAPI overlays, including conversational phrasing for each operation.

- [Fundz Acquisitions Api Overlay](https://apis.io/overlays/fundz/fundz-acquisitions-api-overlay/)
- [Fundz Agreements Api Overlay](https://apis.io/overlays/fundz/fundz-agreements-api-overlay/)
- [Fundz Crowdfundings Api Overlay](https://apis.io/overlays/fundz/fundz-crowdfundings-api-overlay/)
- [Fundz Executives Api Overlay](https://apis.io/overlays/fundz/fundz-executives-api-overlay/)
- [Fundz Fundings Api Overlay](https://apis.io/overlays/fundz/fundz-fundings-api-overlay/)
- [Fundz Products Api Overlay](https://apis.io/overlays/fundz/fundz-products-api-overlay/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Fundz Authentication](https://apis.io/security/fundz/fundz-authentication/)
- [Fundz Domain Security](https://apis.io/security/fundz/fundz-domain-security/)

#### Plans and pricing (2)

Published plans, tiers and prices.

- [Fundz Plans](https://apis.io/plans/fundz/fundz-plans/)
- [Fundz Plans Pricing](https://apis.io/plans/fundz/fundz-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Fundz Rate Limits](https://apis.io/rate-limits/fundz/fundz-rate-limits/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.fundz.net/)
- [Documentation](https://www.fundz.net/fundz-api)
- [Getting started](https://app.fundz.net/knowledge/api-references/authentication)
- [API reference](https://app.fundz.net/knowledge/api-references)
- [Pricing](https://fundz.net/pricing)
- [Support](https://www.fundz.net/contact)
- [Blog](https://www.fundz.net/blog)
- [Terms of service](https://www.fundz.net/terms)
- [Privacy policy](https://www.fundz.net/privacy)
- [GitHub](https://github.com/Fund-z)

## API Evangelist rating

**Kin Score 60.2** — strong · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 73.2 |
| Contract quality | 61.8 |
| Contract governance | 4.5 |
| Operational transparency | 44.7 |
| Developer ergonomics | 73.2 |
| Access clarity | 76.3 |

**Agent readiness 41.8** — agent-native

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | — |
| Reversibility Documented | na |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | na |
| Error Semantics | verified |
| OpenAPI Examples | verified |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | yes |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | na |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | paginated |
| Operation Distinctiveness | na |

**Regulatory alignment 28.7** — Securities & Market Data

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/fundz/](https://apis.io/providers/fundz/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Fundz: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/fundz/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
