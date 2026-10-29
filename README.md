# Compresr

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

Compresr is an LLM context-compression API. You send the long context you would otherwise pass to a model plus the query you want answered, and Compresr returns a shorter context that keeps the answer-bearing spans and drops the rest — fewer input tokens, lower cost, a longer effective context window, and faster inference. It sits in front of whatever LLM stack you already use and replaces nothing. The public API exposes query-specific compression models (latte_v1 and the faster latte_v2) plus tool-output, conversation-history, and tool-discovery variants, over a hosted HTTP API with Python and TypeScript SDKs, first-party framework integrations (LangChain, LangGraph, LlamaIndex, LiteLLM), and per-key tiered rate limits. Compresr Inc. is a Y Combinator W26 company built by four EPFL-trained researchers in San Francisco, California and Switzerland.

**Areas:** LLM · Context Compression · Prompt Engineering · RAG · AI Infrastructure · Developer Tools · Agents · Tokens · Y Combinator

## Compresr on APIs.io

Everything profiled for Compresr is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/compresr/](https://apis.io/providers/compresr/)** — or go straight to one of the APIs or properties below.

### APIs (27)

- [Compresr Admin API](https://apis.io/apis/compresr/compresr-admin-api/) — The Admin API from Compresr — 18 operation(s) for admin.
- [Compresr Admin - Whitelist API](https://apis.io/apis/compresr/compresr-admin-whitelist-api/) — The Admin - Whitelist API from Compresr — 4 operation(s) for admin - whitelist.
- [Compresr API Keys API](https://apis.io/apis/compresr/compresr-api-keys-api/) — The API Keys API from Compresr — 4 operation(s) for api keys.
- [Compresr Auth API](https://apis.io/apis/compresr/compresr-auth-api/) — The Auth API from Compresr — 1 operation(s) for auth.
- [Compresr Billing API](https://apis.io/apis/compresr/compresr-billing-api/) — The Billing API from Compresr — 10 operation(s) for billing.
- [Compresr Careers API](https://apis.io/apis/compresr/compresr-careers-api/) — The Careers API from Compresr — 12 operation(s) for careers.
- [Compresr Platform API](https://apis.io/apis/compresr/compresr-compresr-platform-api-api/) — The Compresr Platform API API from Compresr — 1 operation(s) for compresr platform api.
- [Compresr Compression-Agentic API](https://apis.io/apis/compresr/compresr-compression-agentic-api/) — The Compression-Agentic API from Compresr — 18 operation(s) for compression-agentic.
- [Compresr Compression API](https://apis.io/apis/compresr/compresr-compression-api/) — The Compression API from Compresr — 6 operation(s) for compression.
- [Compresr Compression-Demo API](https://apis.io/apis/compresr/compresr-compression-demo-api/) — The Compression-Demo API from Compresr — 5 operation(s) for compression-demo.
- [Compresr Compression-Models API](https://apis.io/apis/compresr/compresr-compression-models-api/) — The Compression-Models API from Compresr — 2 operation(s) for compression-models.
- [Compresr Dashboard API](https://apis.io/apis/compresr/compresr-dashboard-api/) — The Dashboard API from Compresr — 1 operation(s) for dashboard.
- [Compresr Feature Requests API](https://apis.io/apis/compresr/compresr-feature-requests-api/) — The Feature Requests API from Compresr — 3 operation(s) for feature requests.
- [Compresr Gateway API](https://apis.io/apis/compresr/compresr-gateway-api/) — The Gateway API from Compresr — 5 operation(s) for gateway.
- [Compresr Health API](https://apis.io/apis/compresr/compresr-health-api/) — The Health API from Compresr — 3 operation(s) for health.
- [Compresr Inference API](https://apis.io/apis/compresr/compresr-inference-api/) — The Inference API from Compresr — 1 operation(s) for inference.
- [Compresr Logs API](https://apis.io/apis/compresr/compresr-logs-api/) — The Logs API from Compresr — 1 operation(s) for logs.
- [Compresr Metrics API](https://apis.io/apis/compresr/compresr-metrics-api/) — The Metrics API from Compresr — 2 operation(s) for metrics.
- [Compresr Newsletter API](https://apis.io/apis/compresr/compresr-newsletter-api/) — The Newsletter API from Compresr — 4 operation(s) for newsletter.
- [Compresr OAuth Authorization API](https://apis.io/apis/compresr/compresr-oauth-authorization-api/) — The OAuth Authorization API from Compresr — 3 operation(s) for oauth authorization.
- [Compresr On-Prem API](https://apis.io/apis/compresr/compresr-on-prem-api/) — The On-Prem API from Compresr — 1 operation(s) for on-prem.
- [Compresr On-Prem Telemetry API](https://apis.io/apis/compresr/compresr-on-prem-telemetry-api/) — The On-Prem Telemetry API from Compresr — 3 operation(s) for on-prem telemetry.
- [Compresr Pricing API](https://apis.io/apis/compresr/compresr-pricing-api/) — The Pricing API from Compresr — 2 operation(s) for pricing.
- [Compresr Profile API](https://apis.io/apis/compresr/compresr-profile-api/) — The Profile API from Compresr — 6 operation(s) for profile.
- [Compresr Ready API](https://apis.io/apis/compresr/compresr-ready-api/) — The Ready API from Compresr — 1 operation(s) for ready.
- [Compresr Usage API](https://apis.io/apis/compresr/compresr-usage-api/) — The Usage API from Compresr — 1 operation(s) for usage.
- [Compresr O Auth API](https://apis.io/apis/compresr/compresr-oauth-api/) — The OAuth API from Compresr — 6 operation(s) for oauth.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [compresr](https://apis.io/servers/compresr/compresr/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Compresr Agentic Access](https://apis.io/agentic-access/compresr/compresr-agentic-access/)

#### Collections (27)

Postman and Open Collection request collections.

- [Compresr Platform Admin API](https://apis.io/collections/compresr/open-compresr-admin-api/)
- [Compresr Platform Admin Admin - Whitelist API](https://apis.io/collections/compresr/open-compresr-admin-whitelist-api/)
- [Compresr Platform Admin API Keys API](https://apis.io/collections/compresr/open-compresr-api-keys-api/)
- [Compresr Platform Admin Auth API](https://apis.io/collections/compresr/open-compresr-auth-api/)
- [Compresr Platform Admin Billing API](https://apis.io/collections/compresr/open-compresr-billing-api/)
- [Compresr Platform Admin Careers API](https://apis.io/collections/compresr/open-compresr-careers-api/)
- [Compresr Platform Admin Compresr Platform API API](https://apis.io/collections/compresr/open-compresr-compresr-platform-api-api/)
- [Compresr Platform Admin Compression-Agentic API](https://apis.io/collections/compresr/open-compresr-compression-agentic-api/)
- [Compresr Platform Admin Compression API](https://apis.io/collections/compresr/open-compresr-compression-api/)
- [Compresr Platform Admin Compression-Demo API](https://apis.io/collections/compresr/open-compresr-compression-demo-api/)
- [Compresr Platform Admin Compression-Models API](https://apis.io/collections/compresr/open-compresr-compression-models-api/)
- [Compresr Platform Admin Dashboard API](https://apis.io/collections/compresr/open-compresr-dashboard-api/)
- [Compresr Platform Admin Feature Requests API](https://apis.io/collections/compresr/open-compresr-feature-requests-api/)
- [Compresr Platform Admin Gateway API](https://apis.io/collections/compresr/open-compresr-gateway-api/)
- [Compresr Platform Admin Health API](https://apis.io/collections/compresr/open-compresr-health-api/)
- [Compresr Platform Admin Inference API](https://apis.io/collections/compresr/open-compresr-inference-api/)
- [Compresr Platform Admin Logs API](https://apis.io/collections/compresr/open-compresr-logs-api/)
- [Compresr Platform Admin Metrics API](https://apis.io/collections/compresr/open-compresr-metrics-api/)
- [Compresr Platform Admin Newsletter API](https://apis.io/collections/compresr/open-compresr-newsletter-api/)
- [Compresr Platform Admin OAuth API](https://apis.io/collections/compresr/open-compresr-oauth-api/)
- [Compresr Platform Admin OAuth Authorization API](https://apis.io/collections/compresr/open-compresr-oauth-authorization-api/)
- [Compresr Platform Admin On-Prem API](https://apis.io/collections/compresr/open-compresr-on-prem-api/)
- [Compresr Platform Admin On-Prem Telemetry API](https://apis.io/collections/compresr/open-compresr-on-prem-telemetry-api/)
- [Compresr Platform Admin Pricing API](https://apis.io/collections/compresr/open-compresr-pricing-api/)
- [Compresr Platform Admin Profile API](https://apis.io/collections/compresr/open-compresr-profile-api/)
- …and 2 more published on APIs.io

#### Overlays (1)

OpenAPI overlays, including conversational phrasing for each operation.

- [Compresr Openapi Overlay](https://apis.io/overlays/compresr/compresr-openapi-overlay/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Compresr Authentication](https://apis.io/security/compresr/compresr-authentication/)
- [Compresr Domain Security](https://apis.io/security/compresr/compresr-domain-security/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Compresr Plans](https://apis.io/plans/compresr/compresr-plans/)

#### Rate limits (1)

Published request limits.

- [Compresr Rate Limits](https://apis.io/rate-limits/compresr/compresr-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Compresr Finops](https://apis.io/finops/compresr/compresr-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.compresr.ai/)
- [Documentation](https://compresr.ai/docs)
- [Getting started](https://compresr.ai/docs/quick-start)
- [API reference](https://compresr.ai/docs/api-reference/conventions)
- [Pricing](https://compresr.ai/pricing)
- [Sign up](https://compresr.ai/dashboard)
- [Support](https://compresr.ai/contact)
- [Changelog](https://compresr.ai/changelog)
- [Terms of service](https://compresr.ai/terms)
- [Privacy policy](https://compresr.ai/privacy)
- [GitHub](https://github.com/Compresr-ai)

## API Evangelist rating

**Kin Score 59.7** — strong · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 73.2 |
| Contract quality | 44.1 |
| Contract governance | 4.5 |
| Operational transparency | 57.9 |
| Developer ergonomics | 84.5 |
| Access clarity | 65.8 |

**Agent readiness 35.7** — agent-ready

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | verified |
| Error Semantics | verified |
| OpenAPI Examples | — |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | — |
| Agent Skills | yes |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | — |
| Operation Distinctiveness | distinct |

**Regulatory alignment 22.7** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/compresr/](https://apis.io/providers/compresr/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Compresr: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/compresr/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
