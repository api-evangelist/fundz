# Fundz (fundz)

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

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/fundz/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/fundz/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **Position:** Producing
- **Access:** 3rd-Party

## Tags

- Business Intelligence
- Funding
- Private Markets
- Mergers And Acquisitions
- SEC Filings
- Signals
- Sales Intelligence
- MCP
- Agents

## Timestamps

- **Created:** 2026-08-03
- **Modified:** 2026-08-03

## APIs

### Fundz API

Company profiles, funding rounds, SEC filings and fund formations, keyed to real-time business events.

- **Human URL:** [https://www.fundz.net/fundz-api](https://www.fundz.net/fundz-api)
- **Base URL:** `https://api.fundz.net`

#### Tags

- Funding
- Companies
- SEC Filings
- Fund Formations
- Signals

#### Properties

- [Documentation](https://www.fundz.net/fundz-api)
- [API Reference](https://app.fundz.net/knowledge/api-references/companies)
- [Signup](https://fundz.net/api-trial)
- [Pricing](https://fundz.net/pricing)
- [Authentication](authentication/fundz-authentication.yml)
- [Plans](plans/fundz-plans.yml)
- [M C P Server](mcp/fundz-mcp.yml)
- [Llms Text](https://app.fundz.net/llms.txt)
- [Postman Collection](collections/fundz-acquisitions-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fundz-acquisitions-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/fundz-agreements-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fundz-agreements-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/fundz-crowdfundings-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fundz-crowdfundings-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/fundz-executives-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fundz-executives-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/fundz-fundings-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fundz-fundings-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/fundz-products-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fundz-products-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Fundz Acquisitions API

Company acquisitions and M&A events, with acquirer and target organization records where disclosed.

- **Human URL:** [https://www.fundz.net/fundz-api](https://www.fundz.net/fundz-api)
- **Base URL:** `https://api.fundz.net`

#### Tags

- Acquisitions

#### Properties

- [OpenAPI](openapi/fundz-acquisitions-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/fundz-acquisitions-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fundz-acquisitions-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Fundz Agreements API

Business agreements and partnerships announced by companies — distribution, licensing, joint ventures and similar.

- **Human URL:** [https://www.fundz.net/fundz-api](https://www.fundz.net/fundz-api)
- **Base URL:** `https://api.fundz.net`

#### Tags

- Agreements

#### Properties

- [OpenAPI](openapi/fundz-agreements-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/fundz-agreements-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fundz-agreements-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Fundz Crowdfundings API

Regulation CF and Regulation A crowdfunding campaigns, sourced from SEC Form C and Form 1-A filings.

- **Human URL:** [https://www.fundz.net/fundz-api](https://www.fundz.net/fundz-api)
- **Base URL:** `https://api.fundz.net`

#### Tags

- Crowdfundings

#### Properties

- [OpenAPI](openapi/fundz-crowdfundings-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/fundz-crowdfundings-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fundz-crowdfundings-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Fundz Executives API

Executive hires and appointments — new C-level, VP and board appointments at private and public companies.

- **Human URL:** [https://www.fundz.net/fundz-api](https://www.fundz.net/fundz-api)
- **Base URL:** `https://api.fundz.net`

#### Tags

- Executives

#### Properties

- [OpenAPI](openapi/fundz-executives-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/fundz-executives-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fundz-executives-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Fundz Fundings API

Funding rounds — seed through late-stage venture and private equity — with the investors on the round and the full organization record.

- **Human URL:** [https://www.fundz.net/fundz-api](https://www.fundz.net/fundz-api)
- **Base URL:** `https://api.fundz.net`

#### Tags

- Fundings

#### Properties

- [OpenAPI](openapi/fundz-fundings-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/fundz-fundings-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fundz-fundings-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Fundz Products API

Product launches and major product announcements.

- **Human URL:** [https://www.fundz.net/fundz-api](https://www.fundz.net/fundz-api)
- **Base URL:** `https://api.fundz.net`

#### Tags

- Products

#### Properties

- [OpenAPI](openapi/fundz-products-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/fundz-products-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fundz-products-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Website](https://www.fundz.net/)
- [Documentation](https://www.fundz.net/fundz-api)
- [Pricing](https://fundz.net/pricing)
- [Signup](https://fundz.net/api-trial)
- [Llms Text](https://app.fundz.net/llms.txt)
- [M C P Server](mcp/fundz-mcp.yml)
- [Plans](plans/fundz-plans.yml)
- [Authentication](authentication/fundz-authentication.yml)
- [GitHub Repository](https://github.com/Fund-z/fundzwatch-mcp)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
