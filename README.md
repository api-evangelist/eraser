# Eraser (eraser)

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
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
