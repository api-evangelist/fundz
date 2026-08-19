# Fundz (fundz)

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
