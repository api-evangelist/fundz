# Fundz

Event-first business intelligence — funding rounds, executive changes, M&A, SEC filings and
website-change signals across 200,000+ companies.

- **Website:** https://www.fundz.net/
- **API:** https://www.fundz.net/fundz-api · base `https://api.fundz.net`
- **API reference:** https://app.fundz.net/knowledge/api-references/companies
- **Free instant API key:** https://fundz.net/api-trial
- **Pricing:** https://fundz.net/pricing
- **llms.txt:** https://app.fundz.net/llms.txt
- **MCP server:** `io.github.Fund-z/fundzwatch` on the official MCP registry

Part of the [API Evangelist](https://apievangelist.com) network. Profiled 2026-08-03 after the
founder wrote in. Every claim in that email was checked against the live surface before this
profile was written — see `X-Discovery` in `apis.yml`.

## What was confirmed

| Claim | Result |
| --- | --- |
| MCP server on the official registry | **Confirmed** — `io.github.Fund-z/fundzwatch` v1.2.2, npm `@fundzwatch/mcp-server`, stdio |
| Free instant API key, no card | Page live at `/api-trial` |
| Published pricing rather than quoted | Live at `/pricing` |
| llms.txt | Live, 8.7KB |
| **Publishes an OpenAPI spec** | **Not confirmed — none discoverable** |

## The open gap

The founder states Fundz publishes an OpenAPI spec. None could be found: 404 on `/openapi.json`,
`/openapi.yaml`, `/swagger.json`, `/api-docs`, `/docs`, `/redoc`, `/spec`, `/v1/openapi.json` and
`/.well-known/openapi.json` across `api.fundz.net` and `app.fundz.net`, and none in the
`fundzwatch-mcp` repository. The API reference is hand-written HTML.

**No spec was modelled on their behalf.** Publishing one at a conventional path is the single
highest-value change available to this provider — it is the largest award in the rubric, and it
would let the catalog carry a real contract rather than a documentation link.
