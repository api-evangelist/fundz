---
name: Reach Fundz data from an agent without a paid API key
description: >-
  Use the first-party FundzWatch MCP server to get live Fundz business-event intelligence into an
  agent, including the seven tools that need no credential at all, and know which capabilities are
  only reachable this way versus only reachable over REST.
api: mcp/fundz-mcp.yml
operations: [get_funded_and_hiring, get_refinancing_windows, get_stacked_borrowers, get_benefit_plans_in_play, get_money_in_motion, get_lender_directory, get_broker_directory, get_events, get_scored_leads, get_market_pulse, get_market_brief, manage_watchlist, get_watchlist_events, get_usage]
generated: '2026-08-14'
method: generated
source: https://github.com/Fund-z/fundzwatch-mcp, https://fundzwatch.ai/docs, mcp/fundz-tool-crosswalk.yml
---

# Reach Fundz data from an agent without a paid API key

The Fundz core API is paid-plans-only. The FundzWatch MCP server is not — **7 of its 14 tools
return live data with no credential at all**, and a free key unlocks the rest. If the task is
"get Fundz intelligence into an agent", start here, not at `GET /fundings`.

## Setup

This is a **locally-run stdio server**, not a hosted endpoint. There is no URL an MCP client can
POST to — a human installs it once. Verified 2026-08-14: `fundzwatch.ai/mcp` and
`api.fundz.net/mcp` both 404.

```json
{
  "mcpServers": {
    "fundzwatch": {
      "command": "npx",
      "args": ["-y", "@fundzwatch/mcp-server"]
    }
  }
}
```

Add `"env": {"FUNDZWATCH_API_KEY": "fundz_test_..."}` to unlock the keyed tools. Free key, no
card, at `https://www.fundz.net/api-trial` or `https://fundzwatch.ai/onboarding`. Package:
`@fundzwatch/mcp-server` (npm, MIT, 1.2.3, published 2026-08-03). Also installable via Smithery.

## The seven key-less tools

These answer cross-dataset questions that **exist nowhere in the REST API**. Reach for them when
the question is a join rather than a lookup.

| Tool | Answers |
|---|---|
| `get_funded_and_hiring` | Funded in the last 12 months **and** hiring now — the strongest buying window |
| `get_money_in_motion` | Recent exec move **and** recent funding on the same company |
| `get_refinancing_windows` | UCC-1 liens lapsing within 12 months (CA + CO coverage) |
| `get_stacked_borrowers` | Active secured debt from 2+ distinct lenders |
| `get_benefit_plans_in_play` | Funded companies with a DOL Form 5500 plan — renewal timing, incumbent carrier |
| `get_lender_directory` | 8,600+ UCC secured parties by filing volume |
| `get_broker_directory` | 65,000+ Form 5500 Schedule A benefits brokers |

## The seven keyed tools

`get_scored_leads` (ICP-matched leads with buyer intent), `get_events` (raw funding /
acquisition / hiring / contract / product_launch events), `get_market_pulse` and
`get_market_brief` (aggregates, pre-computed nightly), `manage_watchlist`,
`get_watchlist_events`, `get_usage`.

## Rules

- **`manage_watchlist` is the only write.** Everything else in the Fundz tool surface is
  read-only. If your agent policy gates mutations, that is the one tool to gate.
- **Call `get_usage` before a long run.** The free Developer tier is 1,000 API calls and 100 AI
  score calls per month — a monthly budget, not a daily one, so a runaway loop burns the whole
  month. On exhaustion the underlying API returns 429.
- **Tool input schemas are not published anywhere.** The server is stdio-only, so there is no
  remote `tools/list` to read; discover parameters from the running server, not from the docs.
- **Do not expect MCP to reach the spec'd feeds.** MCP fronts FundzWatch; the OpenAPI describes the
  Fundz event feeds. Only `get_events` overlaps.

## When to drop to REST instead

Switch to the core API (`openapi/`, see `skills/fundz-track-funding-rounds.md`) when you need:

- **Amount, employee-count, stage, investor or offering-type filters.** `get_events` documents only
  `types`, `days`, `limit`, `offset`, `industries`, `locations`.
- **Crowdfunding (SEC Form C / Form 1-A)** or **business agreements** — no MCP tool covers either.
- **A machine-readable input contract.** REST has an OpenAPI; the tools do not.

`mcp/fundz-tool-crosswalk.yml` in this repository is the full map of which capability lives where.
