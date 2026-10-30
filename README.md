# Factorial

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

Factorial is an all-in-one HR, payroll, time, talent, finance, and IT management platform headquartered in Barcelona, Spain, used by 16,000+ companies worldwide. The Factorial public API is a date-versioned REST API (current major 2026-04-01 "Legendre") covering employees, contracts, attendance, time off, payroll, ATS, performance, trainings, projects, finance, banking, procurement, IT assets, documents, webhooks, and an Approvals workflow surface. Authentication uses OAuth2 (on behalf of a user) or an x-api-key header (on behalf of the company), with 30+ scopes for granular partner access. Factorial publishes the OpenAPI schema and generated SDKs (Ruby, Python, Java, PHP, TypeScript, Node.js) at github.com/factorialco/oas and exposes an llms.txt index for AI agents.

**Areas:** Human Resources · Payroll · Time Off · Time Tracking · Applicant Tracking · Performance · Finance · Expenses · Spain · Barcelona · All-in-One

## Factorial on APIs.io

Everything profiled for Factorial is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/factorial-hr/](https://apis.io/providers/factorial-hr/)** — or go straight to one of the APIs or properties below.

### APIs (24)

- [Factorial Webhooks API](https://apis.io/apis/factorial-hr/factorial-webhooks-api/) — Subscribe to lifecycle events fired by Factorial (employee created, employee terminated, attendance clock-in/out, ATS application created/updated, time-off…
- [Factorial ATS API](https://apis.io/apis/factorial-hr/factorial-ats-api/) — Applicant Tracking surface — Candidates, Applications, Application Phases, Job Postings, Feedback, Evaluation Forms, Answers. Read, create, update, and…
- [Factorial Attendance API](https://apis.io/apis/factorial-hr/factorial-attendance-api/) — Manage attendance shifts, breaks, overtime requests, timesheet edits, and attendance reviews. v2026-04-01 introduces an api_source field on shift DTOs so…
- [Factorial Time Off API](https://apis.io/apis/factorial-hr/factorial-time-off-api/) — Time-off leaves, leave types, and time-off allowances with enriched statistics. Trigger webhooks on leave creation, update, and approval. Combine with the…
- [Factorial Contracts and Compensations API](https://apis.io/apis/factorial-hr/factorial-contracts-compensations-api/) — Manage contract versions and compensation records. v2026-04-01 is a breaking-change release that removes legacy job catalog fields (job_title,…
- [Factorial Payroll API](https://apis.io/apis/factorial-hr/factorial-payroll-api/) — Payroll supplements, payroll identifiers, family situations, and bookkeeper resources. Backs Factorial's integrations with country- specific payroll engines.
- [Factorial Finance and Banking API](https://apis.io/apis/factorial-hr/factorial-finance-banking-api/) — Bank accounts, transactions, ledger accounts, journal entries, tax rates and tax types, cost centers, cost center memberships, and budgets. Cost center…
- [Factorial Expenses API](https://apis.io/apis/factorial-hr/factorial-expenses-api/) — Submit, approve, and reconcile employee expenses, mileage claims, and per-diem requests.
- [Factorial Documents API](https://apis.io/apis/factorial-hr/factorial-documents-api/) — Manage company- and employee-scoped documents and folders. Create, update, retrieve, and delete documents, request legal e-signatures, and fire…
- [Factorial Performance API](https://apis.io/apis/factorial-hr/factorial-performance-api/) — Performance reviews, review processes, evaluations, and performance agreements. Configurable review cycles backed by the Job Catalog Tree introduced in…
- [Factorial Trainings API](https://apis.io/apis/factorial-hr/factorial-trainings-api/) — Manage training programs and training classes, expanded in v2026-04-01 with new class-level capabilities.
- [Factorial Job Catalog API](https://apis.io/apis/factorial-hr/factorial-job-catalog-api/) — Job levels, roles, functions, and the hierarchical Job Catalog Tree introduced in v2026-01-01. Replaces the legacy free-text job_title on contracts via…
- [Factorial Project Management API](https://apis.io/apis/factorial-hr/factorial-project-management-api/) — Projects, subprojects, tasks, project workers, planned and flexible time records, and budget strategies (full CRUD added in v2026-04-01).
- [Factorial IT Management API](https://apis.io/apis/factorial-hr/factorial-it-management-api/) — IT asset and IT model endpoints (added in v2026-01-01) backing the SaaS, Inventory, MDM, and Cybersecurity modules.
- [Factorial Procurement API](https://apis.io/apis/factorial-hr/factorial-procurement-api/) — Purchase orders, purchase requests, and purchase types. Added in v2026-01-01.
- [Factorial Approvals API](https://apis.io/apis/factorial-hr/factorial-approvals-api/) — Programmatically approve or reject pending steps of a materialized approval flow, either by id or by resource_id+resource_type. Added in v2026-04-01.
- [Factorial Locations and Holidays API](https://apis.io/apis/factorial-hr/factorial-locations-holidays-api/) — Company locations, work areas, and company holidays.
- [Factorial Posts and Communities API](https://apis.io/apis/factorial-hr/factorial-posts-communities-api/) — Groups, posts, and comments backing the Communities V2 feature. Requires Communities V2 to be enabled on the company.
- [Factorial Marketplace and Integrations API](https://apis.io/apis/factorial-hr/factorial-marketplace-integrations-api/) — Integrations Framework and Marketplace endpoints used by partner integrations to register, surface, and operate within the Factorial app.
- [Factorial Keys and OAuth API](https://apis.io/apis/factorial-hr/factorial-keys-oauth-api/) — Two authentication methods. OAuth2 (authorization code flow at /oauth/authorize and /oauth/token) is used to act on behalf of a user; Credentials/API Keys…
- [Factorial Core::Employees::V2 API](https://apis.io/apis/factorial-hr/factorial-hr-core-employees-v2-api/) — The Core::Employees::V2 API from Factorial — 2 operation(s) for core::employees::v2.
- [Factorial Core::Me API](https://apis.io/apis/factorial-hr/factorial-hr-core-me-api/) — The Core::Me API from Factorial — 1 operation(s) for core::me.
- [Factorial Developer API](https://apis.io/apis/factorial-hr/developer-api/) — Versioned REST API for managing employees, contracts, leaves, attendance shifts, time off, documents, and other HR resources in Factorial. Supports API key…
- [Factorial Resources API](https://apis.io/apis/factorial-hr/factorial-hr-resources-api/) — The Resources API from Factorial — 16 operation(s) for resources.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [factorial-hr](https://apis.io/servers/factorial-hr/factorial-hr/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Factorial Hr Agentic Access](https://apis.io/agentic-access/factorial-hr/factorial-hr-agentic-access/)

#### JSON Schema (2)

The data models the API reads and writes.

- [Factorial Employee](https://apis.io/schemas/factorial-hr/factorial-employee/)
- [Factorial Webhook Subscription](https://apis.io/schemas/factorial-hr/factorial-webhook-subscription/)

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [Factorial Hr Context](https://apis.io/jsonld/factorial-hr/factorial-hr-context/)

#### Vocabulary (1)

The provider's domain terms, defined.

- [Factorial Hr Vocabulary](https://apis.io/vocabularies/factorial-hr/factorial-hr-vocabulary/)

#### Examples (2)

Example requests and responses.

- [Factorial Create Employee Example](https://apis.io/examples/factorial-hr/factorial-create-employee-example/)
- [Factorial Get Current User Example](https://apis.io/examples/factorial-hr/factorial-get-current-user-example/)

#### Collections (3)

Postman and Open Collection request collections.

- [Factorial API](https://apis.io/collections/factorial-hr/open-factorial/)
- [Factorial Core::Employees::V2 API](https://apis.io/collections/factorial-hr/open-factorial-hr-core-employees-v2-api/)
- [Factorial Core::Employees::V2 Core::Me API](https://apis.io/collections/factorial-hr/open-factorial-hr-core-me-api/)

#### Governance rules (2)

Spectral rulesets for the provider's contracts.

- [Factorial — jsonschema rules](https://apis.io/rules/factorial-hr/factorial-hr-jsonschema-spectral-rules/)
- [Factorial — factorial rules](https://apis.io/rules/factorial-hr/factorial-rules/)

#### Security (4)

Authentication, trust centre, and vulnerability disclosure.

- [Factorial Hr Authentication](https://apis.io/security/factorial-hr/factorial-hr-authentication/)
- [Factorial Hr Domain Security](https://apis.io/security/factorial-hr/factorial-hr-domain-security/)
- [Factorial Hr Trust Center](https://apis.io/security/factorial-hr/factorial-hr-trust-center/)
- [Factorial Hr Vulnerability Disclosure](https://apis.io/security/factorial-hr/factorial-hr-vulnerability-disclosure/)

#### OAuth scopes (1)

The permissions the API asks for.

- [Factorial Hr Scopes](https://apis.io/scopes/factorial-hr/factorial-hr-scopes/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Factorial Plans Pricing](https://apis.io/plans/factorial-hr/factorial-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Factorial Rate Limits](https://apis.io/rate-limits/factorial-hr/factorial-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Factorial Finops](https://apis.io/finops/factorial-hr/factorial-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.factorialhr.com/)
- [Documentation](https://apidoc.factorialhr.com/)
- [Getting started](https://apidoc.factorialhr.com/docs/getting-started)
- [Pricing](https://factorialhr.com/pricing)
- [Support](https://apidoc.factorialhr.com/docs/contact-page)
- [Changelog](https://apidoc.factorialhr.com/changelog)
- [Blog](https://factorialhr.com/blog)
- [Terms of service](https://factorialhr.com/terms-and-conditions)
- [Privacy policy](https://factorialhr.com/privacy-policy)
- [GitHub](https://github.com/factorialco)
- [Status](https://factorial.statuspage.io/)

## API Evangelist rating

**Kin Score 48.4** — developing · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 60.0 |
| Contract quality | 62.8 |
| Contract governance | 27.3 |
| Operational transparency | 40.8 |
| Developer ergonomics | 47.6 |
| Access clarity | 32.9 |

**Agent readiness 48.5** — agent-ready (gated down from agent-native)

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | verified |
| Auth Clarity | served (partial credit) |
| Idempotency | — |
| Error Semantics | — |
| OpenAPI Examples | partial |
| Rate Limit Signal | derived (partial credit) |
| Event Surface Described | unknown |
| Agent Skills | — |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | served (partial credit) |
| Protected Resource Metadata | verified |
| Dynamic Client Registration | yes |
| Agentic Commerce | — |
| Pagination Ratio | — |
| Operation Distinctiveness | distinct |

**Regulatory alignment 37.3** — Employment & Payroll

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/factorial-hr/](https://apis.io/providers/factorial-hr/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Factorial: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/factorial-hr/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
