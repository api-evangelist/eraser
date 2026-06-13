# Eraser (eraser)

Eraser is an AI-powered diagramming and technical documentation platform designed for engineering teams. It provides a REST API for generating diagrams from natural language prompts or structured DSL, managing files and workspaces, and embedding interactive technical visuals into documentation workflows. The platform supports flow charts, ERDs, sequence diagrams, cloud architecture diagrams, and BPMN diagrams, and integrates with GitHub, VS Code, Notion, and Confluence. Eraser also provides an MCP server for AI agent-driven diagram automation.

APIs.json: https://raw.githubusercontent.com/api-evangelist/eraser/refs/heads/main/apis.yml

Naftiko: https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=eraser-api-evangelist&utm_content=repo

## Tags

- Diagrams
- Documentation
- AI
- Technical Documentation
- Diagramming
- Architecture
- Developer Tools

## APIs

### Eraser API

The Eraser REST API provides programmatic access to diagram generation, file management, folder management, audit logs, and team usage metrics. API access requires a team API token and is available on paid plans (Starter, Business, Enterprise) with usage-based billing for API calls.

- Documentation: https://docs.eraser.io/docs/eraser-api
- API Reference: https://docs.eraser.io/reference
- OpenAPI Spec: https://app.eraser.io/.well-known/api-spec.json
- Quickstart: https://docs.eraser.io/docs/quickstart

## Plans, Rate Limits, and FinOps

### Plans

Eraser offers four tiers:

| Plan       | Price                        | AI Credits/Month | API Access |
|------------|------------------------------|------------------|------------|
| Free       | $0                           | 5                | No         |
| Starter    | $15/member/month (annual)    | 40               | Yes        |
| Business   | $45/member/month (annual)    | 250              | Yes        |
| Enterprise | Custom                       | Unlimited        | Yes        |

Full plans detail: [plans/eraser-plans-pricing.yml](plans/eraser-plans-pricing.yml)

### Rate Limits

API calls are billed on a usage-based model with configurable monthly spending caps:

- `/render/prompt` (AI diagram generation): $0.80 per call ($80 per 100 calls)
- `/render/elements` (DSL rendering): $0.20 per call ($20 per 100 calls)
- Additional AI credits beyond plan: $0.60 per credit

When 80% of the spending cap is reached, team admins receive an alert. API calls are blocked once the cap is fully consumed until the next calendar month.

Full rate limits detail: [rate-limits/eraser-rate-limits.yml](rate-limits/eraser-rate-limits.yml)

### FinOps

Eraser uses a hybrid pricing model combining fixed per-seat subscriptions with variable usage-based billing. Key optimization strategies include preferring the `/render/elements` endpoint (75% cheaper than `/render/prompt`) for structured diagrams, setting conservative spending caps, and using the team usage metrics API for cost tracking.

Full FinOps detail: [finops/eraser-finops.yml](finops/eraser-finops.yml)

## Timestamps

- Created: 2026-06-13
- Modified: 2026-06-13

## Common

| Type          | URL                                                     |
|---------------|---------------------------------------------------------|
| Website       | https://www.eraser.io/                                  |
| Documentation | https://docs.eraser.io/                                 |
| API Reference | https://docs.eraser.io/reference                        |
| GitHub Org    | https://github.com/eraserlabs                           |
| LinkedIn      | https://www.linkedin.com/company/eraser                 |
| Blog          | https://www.eraser.io/decision-node                     |
| Pricing       | https://www.eraser.io/pricing                           |
| X             | https://x.com/eraserlabs                                |

## Maintainers

- Kin Lane (kin@apievangelist.com)
