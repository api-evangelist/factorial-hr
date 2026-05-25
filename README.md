# Factorial (factorial-hr)

Factorial is an all-in-one HR, payroll, time, talent, finance, and IT management platform headquartered in Barcelona, Spain, used by 16,000+ companies worldwide. The Factorial public API is a date-versioned REST API (current major **2026-04-01 "Legendre"**) covering employees, contracts, attendance, time off, payroll, ATS, performance, trainings, projects, finance, banking, procurement, IT assets, documents, webhooks, and an Approvals workflow surface. Authentication uses OAuth2 (on behalf of a user) or an `x-api-key` header (on behalf of the company), with 30+ scopes for granular partner access. Factorial publishes its OpenAPI schema and generated SDKs at [`github.com/factorialco/oas`](https://github.com/factorialco/oas) and exposes an [`llms.txt`](https://apidoc.factorialhr.com/llms.txt) index for AI agents.

**URL:** [Visit APIs.json](https://raw.githubusercontent.com/api-evangelist/factorial-hr/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags

HR, Human Resources, Payroll, Time Off, Time Tracking, ATS, Performance, Finance, Expenses, Spain, Barcelona, All-in-One

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## Environments

| Environment | Base URL |
|---|---|
| Production | `https://api.factorialhr.com/api` |
| Demo | `https://api.demo.factorialhr.com/api` |

Authentication: **OAuth2** (`/oauth/authorize`, `/oauth/token`) on behalf of a user, or **API Key** (`x-api-key` header) on behalf of the company. When both are supplied on the same request, the API key wins.

API versioning is **date-based and major**. Recent versions: `2026-04-01` (Legendre, current), `2026-01-01` (Lambert), `2025-10-01` (Dirichlet), `2025-07-01` (Laurent), `2025-04-01`.

## APIs

### Factorial Core Employees API
List, read, create, and update employees in the Factorial HR directory. The Core Employees v2 surface returns a clean, non-data-intensive employee shape (the legacy v1 was intentionally data-intensive and is being deprecated). `/v1/me` identifies the OAuth2 token holder.

**Human URL:** [https://apidoc.factorialhr.com/reference](https://apidoc.factorialhr.com/reference)

- [Documentation](https://apidoc.factorialhr.com/)
- [OpenAPI](openapi/factorial-openapi.yml)
- [JSON Schema - Employee](json-schema/factorial-employee-schema.json)
- [JSON-LD context](json-ld/factorial-hr-context.jsonld)
- [Naftiko Capability - Employees](capabilities/shared/employees.yaml)
- [Naftiko Capability - Me](capabilities/shared/me.yaml)
- [Naftiko Workflow - Onboard a New Hire](capabilities/onboard-new-hire.yaml)
- [Example - List Employees](examples/factorial-list-employees-example.json)
- [Example - Create Employee](examples/factorial-create-employee-example.json)
- [Example - Current User](examples/factorial-get-current-user-example.json)

### Factorial Webhooks API
Subscribe to lifecycle events fired by Factorial (employee_created, employee_terminated, attendance_clockin/clockout, ats_application_created/updated, ats_job_posting_created/updated/deleted, timeoff_leave_created/updated/approved, document_created, ...). Factorial POSTs the event payload to your URL and retries on failure; consumers must be idempotent.

- [Manage Webhooks](https://apidoc.factorialhr.com/docs/manage-webhooks)
- [Webhooks Policies](https://apidoc.factorialhr.com/docs/webhooks-policies)
- [What are webhooks?](https://apidoc.factorialhr.com/docs/webhooks-what)
- [Practical example - clock-in](https://apidoc.factorialhr.com/docs/webhook-attendance-clock-in)
- [JSON Schema - Webhook Subscription](json-schema/factorial-webhook-subscription-schema.json)

### Factorial ATS API
Candidates, applications, application phases, job postings, feedback, evaluation forms, answers. Full CRUD plus phase progression.

### Factorial Attendance API
Shifts, breaks, overtime requests, timesheet edits, attendance reviews. `v2026-04-01` introduces an `api_source` field on shift DTOs so integrations can identify themselves on clock operations.

### Factorial Time Off API
Time-off leaves, leave types, and time-off allowances with enriched statistics. Combine with the **Approvals API** to programmatically approve or reject pending leaves.

### Factorial Contracts and Compensations API
Contract versions and compensation records. `v2026-04-01` removes legacy job catalog fields (`job_title`, `professional_category_id`, `professional_category_description`) in favour of `job_catalog_tree_node_uuid`, and adds richer fields for German and Spanish payroll integrations.

### Factorial Payroll API
Payroll supplements, payroll identifiers, family situations, bookkeeper resources. Backs Factorial's country-specific payroll integrations.

- [Payroll Integrations guide](https://apidoc.factorialhr.com/docs/payroll-integrations)

### Factorial Finance and Banking API
Bank accounts, transactions, ledger accounts, journal entries, tax rates and tax types, cost centers, cost center memberships (bulk-updatable with percentage splits), and budgets.

- [Finance Integrations guide](https://apidoc.factorialhr.com/docs/finance-integrations)

### Factorial Expenses API
Employee expenses, mileage claims, per-diem requests.

### Factorial Documents API
Company- and employee-scoped documents and folders. Includes legal e-signature workflows; admin-only for document creation; fires `document_created` webhook events.

### Factorial Performance API
Performance reviews, review processes, evaluations, and performance agreements, configurable against the Job Catalog Tree.

### Factorial Trainings API
Training programs and training classes (class-level capabilities expanded in `v2026-04-01`).

### Factorial Job Catalog API
Job levels, roles, functions, and the hierarchical **Job Catalog Tree** introduced in `v2026-01-01`.

### Factorial Project Management API
Projects, subprojects, tasks, project workers, planned and flexible time records, and **budget strategies** (full CRUD added in `v2026-04-01`).

### Factorial IT Management API
IT assets and IT models (added in `v2026-01-01`) backing the SaaS, Inventory, MDM, and Cybersecurity / EDR modules.

### Factorial Procurement API
Purchase orders, purchase requests, purchase types (added in `v2026-01-01`).

### Factorial Approvals API
Programmatically **approve** or **reject** the current pending step of a materialized approval flow, either by ID or by `resource_id` + `resource_type` (added in `v2026-04-01`).

### Factorial Locations and Holidays API
Company locations, work areas, company holidays.

### Factorial Custom Fields API
Define custom fields, options, values, and schemas to extend Factorial resources with company-specific metadata.

### Factorial Posts and Communities API
Groups, posts, and comments. Requires the Communities V2 feature.

### Factorial Marketplace and Integrations API
Integrations Framework and Marketplace endpoints for partner integrations.

- [Integrations Framework](https://apidoc.factorialhr.com/docs/integrations-framework)

### Factorial Keys and OAuth API
OAuth2 authorization-code flow (`/oauth/authorize`, `/oauth/token`) for user-context tokens, plus API Keys (`x-api-key`) for full-admin company-context access. 30+ scopes available.

- [API Keys](https://apidoc.factorialhr.com/docs/api-keys)
- [OAuth 2](https://apidoc.factorialhr.com/docs/oauth-2)
- [OAuth Scopes](https://apidoc.factorialhr.com/docs/oauth-scopes)
- [Create an OAuth Application](https://apidoc.factorialhr.com/docs/create-a-new-oauth-application)
- [Partner guide](https://apidoc.factorialhr.com/docs/oauth2-partner-guide)

## Common Properties

- [Portal - factorialhr.com](https://factorialhr.com)
- [Documentation - apidoc.factorialhr.com](https://apidoc.factorialhr.com/)
- [API Reference](https://apidoc.factorialhr.com/reference)
- [GettingStarted](https://apidoc.factorialhr.com/docs/getting-started)
- [Authentication](https://apidoc.factorialhr.com/docs/authentication)
- [API Versioning](https://apidoc.factorialhr.com/docs/api-versioning)
- [Production and Demo environments](https://apidoc.factorialhr.com/docs/production-and-demo)
- [Pagination](https://apidoc.factorialhr.com/docs/pagination)
- [FAQs](https://apidoc.factorialhr.com/docs/faqs)
- [ChangeLog](https://apidoc.factorialhr.com/changelog)
- [Pricing](https://factorialhr.com/pricing) (from $8/user/month, modular add-ons)
- [SignUp](https://factorialhr.com/signup)
- [Login - app.factorialhr.com](https://app.factorialhr.com/users/sign_in)
- [StatusPage](https://factorial.statuspage.io/)
- [Blog](https://factorialhr.com/blog)
- [GitHubOrganization](https://github.com/factorialco)
- [OpenAPI Schema Repository - factorialco/oas](https://github.com/factorialco/oas)
- [SDK - Ruby](https://github.com/factorialco/oas/tree/main/sdk-ruby)
- [SDK - Python](https://github.com/factorialco/oas/tree/main/sdk-python)
- [SDK - Java](https://github.com/factorialco/oas/tree/main/sdk-java)
- [SDK - PHP](https://github.com/factorialco/oas/tree/main/sdk-php)
- [SDK - TypeScript (axios)](https://github.com/factorialco/oas/tree/main/sdk-typescript-axios)
- [SDK - Node.js server](https://github.com/factorialco/oas/tree/main/sdk-nodejs-server)
- [Tool - f0 Design System](https://github.com/factorialco/f0)
- [LinkedIn](https://www.linkedin.com/company/factorial-hr/)
- [llms.txt - AI-agent index](https://apidoc.factorialhr.com/llms.txt)

## Artifacts

Machine-readable API specifications and accompanying artifacts, organized by format.

### OpenAPI

- [Factorial API (Core Employees v1/v2 + Custom Fields)](openapi/factorial-openapi.yml)

> The canonical multi-SDK source of truth is mirrored upstream at [`github.com/factorialco/oas`](https://github.com/factorialco/oas). The full `2026-04-01` per-resource reference (681+ endpoints across 30+ resource domains) is browseable at [apidoc.factorialhr.com/reference](https://apidoc.factorialhr.com/reference).

### JSON Schema

- [Employee](json-schema/factorial-employee-schema.json)
- [Webhook Subscription](json-schema/factorial-webhook-subscription-schema.json)

### JSON-LD

- [Factorial HR Context](json-ld/factorial-hr-context.jsonld)

### Capabilities (Naftiko)

- [Employees](capabilities/shared/employees.yaml)
- [Me](capabilities/shared/me.yaml)
- [Workflow - Onboard a New Hire](capabilities/onboard-new-hire.yaml)

### Examples

- [List employees](examples/factorial-list-employees-example.json)
- [Create employee](examples/factorial-create-employee-example.json)
- [Current user](examples/factorial-get-current-user-example.json)

### Spectral Rules

- [Factorial Spectral Ruleset](rules/factorial-rules.yml)

### Vocabulary

- [Factorial HR Vocabulary](vocabulary/factorial-hr-vocabulary.yml)

### Commercial artifacts

- [Plans / Pricing](plans/factorial-plans-pricing.yml)
- [Rate Limits](rate-limits/factorial-rate-limits.yml)
- [FinOps Definition](finops/factorial-finops.yml)

## Maintainers

**FN:** Kin Lane

**Email:** info@apievangelist.com
