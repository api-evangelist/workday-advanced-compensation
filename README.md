# Workday Advanced Compensation

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

Workday Advanced Compensation is the Workday HCM module for total-rewards administration — compensation plans and grades, merit and bonus cycles, stock and equity awards, compensation scorecards, budget pools and compensation review processes. Workday exposes it through three first-party machine-readable contracts published anonymously on its own hosts: a REST service (compensation v1-v3, OpenAPI 3.0.1) whose operation descriptions name the Advanced Compensation scope directly, the Compensation and Compensation_Review Workday Web Services SOAP contracts (89 operations across two WSDLs, v47.0), and a Compensation namespace inside Workday's published GraphQL schema. The capability surface is overwhelmingly SOAP: 89 SOAP operations against 14 REST operations. Every surface runs against a customer's own Workday tenant under OAuth 2.0 with Workday security domains; there is no public sandbox, no published pricing and no idempotency contract on any compensation write.

**Areas:** Compensation · Human Resources · Payroll · HCM · Enterprise Software · Total Rewards · Bonus · Merit · Stock-Compensation · SOAP · Software-as-a-Service

## Workday Advanced Compensation on APIs.io

Everything profiled for Workday Advanced Compensation is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/workday-advanced-compensation/](https://apis.io/providers/workday-advanced-compensation/)** — or go straight to one of the APIs or properties below.

### APIs (13)

- [Workday Compensation SOAP Web Services (WWS v47.0)](https://apis.io/apis/workday-advanced-compensation/workday-compensation-soap-wws/) — Workday Web Services for compensation, published as WSDL 1.1 on community.workday.com under the urn:com.workday/bsvc/Compensation namespace. The…
- [Workday Advanced Compensation Bonus Plans API](https://apis.io/apis/workday-advanced-compensation/workday-advanced-compensation-bonus-plans-api/) — Manage bonus and incentive plans
- [Workday Advanced Compensation Budgets API](https://apis.io/apis/workday-advanced-compensation/workday-advanced-compensation-compensation-budgets-api/) — Manage compensation budgets and allocations
- [Workday Advanced Compensation Grades API](https://apis.io/apis/workday-advanced-compensation/workday-advanced-compensation-compensation-grades-api/) — Manage compensation grade profiles and pay ranges
- [Workday Advanced Compensation Plans API](https://apis.io/apis/workday-advanced-compensation/workday-advanced-compensation-compensation-plans-api/) — Manage compensation plans and eligibility rules
- [Workday Advanced Compensation Reviews API](https://apis.io/apis/workday-advanced-compensation/workday-advanced-compensation-compensation-reviews-api/) — Manage compensation review processes and cycles
- [Workday Advanced Compensation Employee Compensation API](https://apis.io/apis/workday-advanced-compensation/workday-advanced-compensation-employee-compensation-api/) — Manage individual employee compensation packages
- [Workday Advanced Compensation Merit Plans API](https://apis.io/apis/workday-advanced-compensation/workday-advanced-compensation-merit-plans-api/) — Manage merit increase plans and cycles
- [Workday Advanced Compensation Stock Plans API](https://apis.io/apis/workday-advanced-compensation/workday-advanced-compensation-stock-plans-api/) — Manage equity and stock compensation plans
- [Workday Advanced Compensation Prompt Values API](https://apis.io/apis/workday-advanced-compensation/workday-advanced-compensation-prompt-values-api/) — Retrieves instances that can be used as values for other endpoint parameters in this service.
- [Workday Advanced Compensation Scorecard Results API](https://apis.io/apis/workday-advanced-compensation/workday-advanced-compensation-scorecardresults-api/) — Provides the ability to set up and retrieve Scores on Scorecard Results.
- [Workday Advanced Compensation Scorecards API](https://apis.io/apis/workday-advanced-compensation/workday-advanced-compensation-scorecards-api/) — Provides the ability to set up and retrieve Scores on Scorecard Results.
- [Workday Advanced Compensation Workers API](https://apis.io/apis/workday-advanced-compensation/workday-advanced-compensation-workers-api/) — The workers API from Workday Advanced Compensation — 3 operation(s) for workers.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [workday-advanced-compensation-mcp.yml](https://apis.io/servers/workday-advanced-compensation/workday-advanced-compensation-mcp-yml/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Workday Advanced Compensation Agentic Access](https://apis.io/agentic-access/workday-advanced-compensation/workday-advanced-compensation-agentic-access/)

#### JSON Schema (9)

The data models the API reads and writes.

- [Bonus Plan](https://apis.io/schemas/workday-advanced-compensation/workday-advanced-compensation-bonus-plan/)
- [Compensation Budget](https://apis.io/schemas/workday-advanced-compensation/workday-advanced-compensation-compensation-budget/)
- [Compensation Change Request](https://apis.io/schemas/workday-advanced-compensation/workday-advanced-compensation-compensation-change-request/)
- [Compensation Grade](https://apis.io/schemas/workday-advanced-compensation/workday-advanced-compensation-compensation-grade/)
- [Compensation Plan](https://apis.io/schemas/workday-advanced-compensation/workday-advanced-compensation-compensation-plan/)
- [Compensation Review](https://apis.io/schemas/workday-advanced-compensation/workday-advanced-compensation-compensation-review/)
- [Employee Compensation](https://apis.io/schemas/workday-advanced-compensation/workday-advanced-compensation-employee-compensation/)
- [Merit Plan](https://apis.io/schemas/workday-advanced-compensation/workday-advanced-compensation-merit-plan/)
- [Stock Plan](https://apis.io/schemas/workday-advanced-compensation/workday-advanced-compensation-stock-plan/)

#### JSON Structure (9)

Data models expressed in JSON Structure.

- [Workday Advanced Compensation Bonus Plan Structure](https://apis.io/json-structure/workday-advanced-compensation/workday-advanced-compensation-bonus-plan-structure/)
- [Workday Advanced Compensation Compensation Budget Structure](https://apis.io/json-structure/workday-advanced-compensation/workday-advanced-compensation-compensation-budget-structure/)
- [Workday Advanced Compensation Compensation Change Request Structure](https://apis.io/json-structure/workday-advanced-compensation/workday-advanced-compensation-compensation-change-request-structure/)
- [Workday Advanced Compensation Compensation Grade Structure](https://apis.io/json-structure/workday-advanced-compensation/workday-advanced-compensation-compensation-grade-structure/)
- [Workday Advanced Compensation Compensation Plan Structure](https://apis.io/json-structure/workday-advanced-compensation/workday-advanced-compensation-compensation-plan-structure/)
- [Workday Advanced Compensation Compensation Review Structure](https://apis.io/json-structure/workday-advanced-compensation/workday-advanced-compensation-compensation-review-structure/)
- [Workday Advanced Compensation Employee Compensation Structure](https://apis.io/json-structure/workday-advanced-compensation/workday-advanced-compensation-employee-compensation-structure/)
- [Workday Advanced Compensation Merit Plan Structure](https://apis.io/json-structure/workday-advanced-compensation/workday-advanced-compensation-merit-plan-structure/)
- [Workday Advanced Compensation Stock Plan Structure](https://apis.io/json-structure/workday-advanced-compensation/workday-advanced-compensation-stock-plan-structure/)

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [Workday Advanced Compensation Context](https://apis.io/jsonld/workday-advanced-compensation/workday-advanced-compensation-context/)

#### Vocabulary (1)

The provider's domain terms, defined.

- [Workday Advanced Compensation Vocabulary](https://apis.io/vocabularies/workday-advanced-compensation/workday-advanced-compensation-vocabulary/)

#### Examples (9)

Example requests and responses.

- [Workday Advanced Compensation Bonus Plan Example](https://apis.io/examples/workday-advanced-compensation/workday-advanced-compensation-bonus-plan-example/)
- [Workday Advanced Compensation Compensation Budget Example](https://apis.io/examples/workday-advanced-compensation/workday-advanced-compensation-compensation-budget-example/)
- [Workday Advanced Compensation Compensation Change Request Example](https://apis.io/examples/workday-advanced-compensation/workday-advanced-compensation-compensation-change-request-example/)
- [Workday Advanced Compensation Compensation Grade Example](https://apis.io/examples/workday-advanced-compensation/workday-advanced-compensation-compensation-grade-example/)
- [Workday Advanced Compensation Compensation Plan Example](https://apis.io/examples/workday-advanced-compensation/workday-advanced-compensation-compensation-plan-example/)
- [Workday Advanced Compensation Compensation Review Example](https://apis.io/examples/workday-advanced-compensation/workday-advanced-compensation-compensation-review-example/)
- [Workday Advanced Compensation Employee Compensation Example](https://apis.io/examples/workday-advanced-compensation/workday-advanced-compensation-employee-compensation-example/)
- [Workday Advanced Compensation Merit Plan Example](https://apis.io/examples/workday-advanced-compensation/workday-advanced-compensation-merit-plan-example/)
- [Workday Advanced Compensation Stock Plan Example](https://apis.io/examples/workday-advanced-compensation/workday-advanced-compensation-stock-plan-example/)

#### Collections (8)

Postman and Open Collection request collections.

- [Workday Advanced Compensation API](https://apis.io/collections/workday-advanced-compensation/open-workday-advanced-compensation/)
- [Workday Advanced Compensation Bonus Plans API](https://apis.io/collections/workday-advanced-compensation/open-workday-advanced-compensation-bonus-plans-api/)
- [Workday Advanced Compensation Bonus Plans Compensation Budgets API](https://apis.io/collections/workday-advanced-compensation/open-workday-advanced-compensation-compensation-budgets-api/)
- [Workday Advanced Compensation Bonus Plans Compensation Grades API](https://apis.io/collections/workday-advanced-compensation/open-workday-advanced-compensation-compensation-grades-api/)
- [Workday Advanced Compensation Bonus Plans Compensation Plans API](https://apis.io/collections/workday-advanced-compensation/open-workday-advanced-compensation-compensation-plans-api/)
- [Workday Advanced Compensation Bonus Plans Employee Compensation API](https://apis.io/collections/workday-advanced-compensation/open-workday-advanced-compensation-employee-compensation-api/)
- [Workday Advanced Compensation Bonus Plans Merit Plans API](https://apis.io/collections/workday-advanced-compensation/open-workday-advanced-compensation-merit-plans-api/)
- [Workday Advanced Compensation Bonus Plans Stock Plans API](https://apis.io/collections/workday-advanced-compensation/open-workday-advanced-compensation-stock-plans-api/)

#### Overlays (1)

OpenAPI overlays, including conversational phrasing for each operation.

- [Workday Advanced Compensation Compensation Rest V3 Overlay](https://apis.io/overlays/workday-advanced-compensation/workday-advanced-compensation-compensation-rest-v3-overlay/)

#### Governance rules (2)

Spectral rulesets for the provider's contracts.

- [Workday Advanced Compensation — jsonschema rules](https://apis.io/rules/workday-advanced-compensation/workday-advanced-compensation-jsonschema-spectral-rules/)
- [Workday Advanced Compensation API Rules](https://apis.io/rules/workday-advanced-compensation/workday-advanced-compensation-spectral-rules/)

#### Security (3)

Authentication, trust centre, and vulnerability disclosure.

- [Workday Advanced Compensation Authentication](https://apis.io/security/workday-advanced-compensation/workday-advanced-compensation-authentication/)
- [Workday Advanced Compensation Domain Security](https://apis.io/security/workday-advanced-compensation/workday-advanced-compensation-domain-security/)
- [Workday Advanced Compensation Trust Center](https://apis.io/security/workday-advanced-compensation/workday-advanced-compensation-trust-center/)

#### OAuth scopes (1)

The permissions the API asks for.

- [Workday Advanced Compensation Scopes](https://apis.io/scopes/workday-advanced-compensation/workday-advanced-compensation-scopes/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Workday Advanced Compensation Plans Pricing](https://apis.io/plans/workday-advanced-compensation/workday-advanced-compensation-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Workday Advanced Compensation Rate Limits](https://apis.io/rate-limits/workday-advanced-compensation/workday-advanced-compensation-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Workday Advanced Compensation Finops](https://apis.io/finops/workday-advanced-compensation/workday-advanced-compensation-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.workday.com/)
- [Documentation](https://developer.workday.com/)
- [Getting started](https://developer.workday.com/doc/GUID-1293c9bb-ea02-48cd-a523-254b5060b3a6-enHYPHENus.md)
- [API reference](https://community.workday.com/sites/default/files/file-hosting/restapi/index.html)
- [Support](https://www.workday.com/en-us/company/about-workday/contact-us.html)
- [Blog](https://blog.workday.com/)
- [Security](https://www.workday.com/en-us/why-workday/trust/overview.html)
- [Compliance](https://www.workday.com/en-us/why-workday/trust/compliance.html)
- [Trust centre](https://security.workday.com/)
- [Terms of service](https://www.workday.com/en-us/legal.html)
- [Privacy policy](https://www.workday.com/en-us/privacy.html)
- [GitHub](https://github.com/Workday)

## API Evangelist rating

**Kin Score 48.6** — developing · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 69.6 |
| Contract quality | 30.7 |
| Contract governance | 45.5 |
| Operational transparency | 44.7 |
| Developer ergonomics | 64.9 |
| Access clarity | 36.8 |

**Agent readiness 35.9** — agent-ready

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | negotiable (partial credit) |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | verified |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | — |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | paginated |
| Operation Distinctiveness | — |

**Regulatory alignment 39.2** — Employment & Payroll

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/workday-advanced-compensation/](https://apis.io/providers/workday-advanced-compensation/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Workday Advanced Compensation: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/workday-advanced-compensation/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
