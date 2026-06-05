# Factorial (factorial)

Factorial is an all-in-one HR, payroll, time, talent, finance, and IT management platform headquartered in Barcelona, Spain, used by 16,000+ companies worldwide. The Factorial public API is a date-versioned REST API (current major 2026-04-01 "Legendre") covering employees, contracts, attendance, time off, payroll, ATS, performance, trainings, projects, finance, banking, procurement, IT assets, documents, webhooks, and an Approvals workflow surface. Authentication uses OAuth2 (on behalf of a user) or an x-api-key header (on behalf of the company), with 30+ scopes for granular partner access. Factorial publishes the OpenAPI schema and generated SDKs (Ruby, Python, Java, PHP, TypeScript, Node.js) at github.com/factorialco/oas and exposes an llms.txt index for AI agents.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/factorial-hr/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/factorial-hr/refs/heads/main/apis.yml)

## Scope

- **Position:** Consuming
- **Access:** 3rd-Party

## Tags

- HR
- Human Resources
- Payroll
- Time Off
- Time Tracking
- ATS
- Performance
- Finance
- Expenses
- Spain
- Barcelona
- All-in-One

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## APIs

### Factorial Core Employees API

List, read, create, and update employees in the Factorial HR directory. The Core Employees v2 API exposes a clean, non-data-intensive employee record (replacing the legacy v1 shape) plus the /v1/me endpoint for identifying the current OAuth2 token holder. Supports both OAuth2 and x-api-key authentication.

- **Human URL:** [https://apidoc.factorialhr.com/reference](https://apidoc.factorialhr.com/reference)

#### Tags

- HR
- Employees
- Core

#### Properties

- [Documentation](https://apidoc.factorialhr.com/)
- [Documentation](https://apidoc.factorialhr.com/reference)
- [OpenAPI](openapi/factorial-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/factorial.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/factorial.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/factorial-employee-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON-LD](json-ld/factorial-hr-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Example](examples/factorial-list-employees-example.json)
- [Example](examples/factorial-create-employee-example.json)
- [Example](examples/factorial-get-current-user-example.json)

### Factorial Webhooks API

Subscribe to lifecycle events fired by Factorial (employee created, employee terminated, attendance clock-in/out, ATS application created/updated, time-off leave created/approved, document created, etc.). Factorial POSTs the event payload to your target URL and retries on failure; consumer endpoints must be idempotent.

- **Human URL:** [https://apidoc.factorialhr.com/docs/manage-webhooks](https://apidoc.factorialhr.com/docs/manage-webhooks)

#### Tags

- HR
- Webhooks
- Events

#### Properties

- [Documentation](https://apidoc.factorialhr.com/docs/manage-webhooks)
- [Documentation](https://apidoc.factorialhr.com/docs/webhooks-policies)
- [Documentation](https://apidoc.factorialhr.com/docs/webhooks-what)
- [Documentation](https://apidoc.factorialhr.com/docs/webhook-attendance-clock-in)
- [JSON Schema](json-schema/factorial-webhook-subscription-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [Postman Collection](collections/factorial.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/factorial.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Factorial ATS API

Applicant Tracking surface — Candidates, Applications, Application Phases, Job Postings, Feedback, Evaluation Forms, Answers. Read, create, update, and delete candidates and applications, plus phase progression and structured feedback collection. Part of the dated 2026-04-01 resource API.

- **Human URL:** [https://apidoc.factorialhr.com/reference](https://apidoc.factorialhr.com/reference)

#### Tags

- HR
- Recruiting
- ATS

#### Properties

- [Documentation](https://apidoc.factorialhr.com/reference)
- [Postman Collection](collections/factorial.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/factorial.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Factorial Attendance API

Manage attendance shifts, breaks, overtime requests, timesheet edits, and attendance reviews. v2026-04-01 introduces an api_source field on shift DTOs so integrations can identify themselves on clock operations.

- **Human URL:** [https://apidoc.factorialhr.com/reference](https://apidoc.factorialhr.com/reference)

#### Tags

- HR
- Time
- Attendance

#### Properties

- [Documentation](https://apidoc.factorialhr.com/reference)
- [Postman Collection](collections/factorial.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/factorial.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Factorial Time Off API

Time-off leaves, leave types, and time-off allowances with enriched statistics. Trigger webhooks on leave creation, update, and approval. Combine with the Approvals API to programmatically approve or reject pending leaves.

- **Human URL:** [https://apidoc.factorialhr.com/reference](https://apidoc.factorialhr.com/reference)

#### Tags

- HR
- Time Off
- PTO

#### Properties

- [Documentation](https://apidoc.factorialhr.com/reference)
- [Postman Collection](collections/factorial.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/factorial.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Factorial Contracts and Compensations API

Manage contract versions and compensation records. v2026-04-01 is a breaking-change release that removes legacy job catalog fields (job_title, professional_category_id, professional_category_description) in favour of job_catalog_tree_node_uuid, and adds richer fields for German and Spanish payroll integrations.

- **Human URL:** [https://apidoc.factorialhr.com/reference](https://apidoc.factorialhr.com/reference)

#### Tags

- HR
- Contracts
- Compensation

#### Properties

- [Documentation](https://apidoc.factorialhr.com/reference)
- [Postman Collection](collections/factorial.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/factorial.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Factorial Payroll API

Payroll supplements, payroll identifiers, family situations, and bookkeeper resources. Backs Factorial's integrations with country- specific payroll engines.

- **Human URL:** [https://apidoc.factorialhr.com/docs/payroll-integrations](https://apidoc.factorialhr.com/docs/payroll-integrations)

#### Tags

- HR
- Payroll
- Finance

#### Properties

- [Documentation](https://apidoc.factorialhr.com/docs/payroll-integrations)
- [Documentation](https://apidoc.factorialhr.com/reference)
- [Postman Collection](collections/factorial.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/factorial.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Factorial Finance and Banking API

Bank accounts, transactions, ledger accounts, journal entries, tax rates and tax types, cost centers, cost center memberships, and budgets. Cost center memberships are bulk-updatable so percentage splits can be applied atomically per employee.

- **Human URL:** [https://apidoc.factorialhr.com/docs/finance-integrations](https://apidoc.factorialhr.com/docs/finance-integrations)

#### Tags

- Finance
- Banking
- Accounting

#### Properties

- [Documentation](https://apidoc.factorialhr.com/docs/finance-integrations)
- [Documentation](https://apidoc.factorialhr.com/reference)
- [Postman Collection](collections/factorial.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/factorial.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Factorial Expenses API

Submit, approve, and reconcile employee expenses, mileage claims, and per-diem requests.

- **Human URL:** [https://apidoc.factorialhr.com/reference](https://apidoc.factorialhr.com/reference)

#### Tags

- Finance
- Expenses
- Mileage

#### Properties

- [Documentation](https://apidoc.factorialhr.com/reference)
- [Postman Collection](collections/factorial.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/factorial.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Factorial Documents API

Manage company- and employee-scoped documents and folders. Create, update, retrieve, and delete documents, request legal e-signatures, and fire document_created webhook events. Admin-only for document creation.

- **Human URL:** [https://apidoc.factorialhr.com/reference](https://apidoc.factorialhr.com/reference)

#### Tags

- HR
- Documents
- E-Signature

#### Properties

- [Documentation](https://apidoc.factorialhr.com/reference)
- [Postman Collection](collections/factorial.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/factorial.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Factorial Performance API

Performance reviews, review processes, evaluations, and performance agreements. Configurable review cycles backed by the Job Catalog Tree introduced in v2026-01-01.

- **Human URL:** [https://apidoc.factorialhr.com/reference](https://apidoc.factorialhr.com/reference)

#### Tags

- HR
- Performance
- Talent

#### Properties

- [Documentation](https://apidoc.factorialhr.com/reference)
- [Postman Collection](collections/factorial.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/factorial.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Factorial Trainings API

Manage training programs and training classes, expanded in v2026-04-01 with new class-level capabilities.

- **Human URL:** [https://apidoc.factorialhr.com/reference](https://apidoc.factorialhr.com/reference)

#### Tags

- HR
- Training
- Learning

#### Properties

- [Documentation](https://apidoc.factorialhr.com/reference)
- [Postman Collection](collections/factorial.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/factorial.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Factorial Job Catalog API

Job levels, roles, functions, and the hierarchical Job Catalog Tree introduced in v2026-01-01. Replaces the legacy free-text job_title on contracts via job_catalog_tree_node_uuid.

- **Human URL:** [https://apidoc.factorialhr.com/reference](https://apidoc.factorialhr.com/reference)

#### Tags

- HR
- Job Catalog
- Levels

#### Properties

- [Documentation](https://apidoc.factorialhr.com/reference)
- [Postman Collection](collections/factorial.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/factorial.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Factorial Project Management API

Projects, subprojects, tasks, project workers, planned and flexible time records, and budget strategies (full CRUD added in v2026-04-01).

- **Human URL:** [https://apidoc.factorialhr.com/reference](https://apidoc.factorialhr.com/reference)

#### Tags

- Projects
- Tasks
- Time Tracking

#### Properties

- [Documentation](https://apidoc.factorialhr.com/reference)
- [Postman Collection](collections/factorial.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/factorial.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Factorial IT Management API

IT asset and IT model endpoints (added in v2026-01-01) backing the SaaS, Inventory, MDM, and Cybersecurity modules.

- **Human URL:** [https://apidoc.factorialhr.com/reference](https://apidoc.factorialhr.com/reference)

#### Tags

- IT
- Asset Management
- MDM

#### Properties

- [Documentation](https://apidoc.factorialhr.com/reference)
- [Postman Collection](collections/factorial.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/factorial.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Factorial Procurement API

Purchase orders, purchase requests, and purchase types. Added in v2026-01-01.

- **Human URL:** [https://apidoc.factorialhr.com/reference](https://apidoc.factorialhr.com/reference)

#### Tags

- Procurement
- Purchase Orders

#### Properties

- [Documentation](https://apidoc.factorialhr.com/reference)
- [Postman Collection](collections/factorial.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/factorial.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Factorial Approvals API

Programmatically approve or reject pending steps of a materialized approval flow, either by id or by resource_id+resource_type. Added in v2026-04-01.

- **Human URL:** [https://apidoc.factorialhr.com/reference](https://apidoc.factorialhr.com/reference)

#### Tags

- Workflows
- Approvals

#### Properties

- [Documentation](https://apidoc.factorialhr.com/reference)
- [Postman Collection](collections/factorial.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/factorial.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Factorial Locations and Holidays API

Company locations, work areas, and company holidays.

- **Human URL:** [https://apidoc.factorialhr.com/reference](https://apidoc.factorialhr.com/reference)

#### Tags

- HR
- Locations
- Holidays

#### Properties

- [Documentation](https://apidoc.factorialhr.com/reference)
- [Postman Collection](collections/factorial.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/factorial.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Factorial Custom Fields API

Define custom fields, options, values, and schemas to extend Factorial resources with company-specific metadata.

- **Human URL:** [https://apidoc.factorialhr.com/reference](https://apidoc.factorialhr.com/reference)

#### Tags

- HR
- Custom Fields
- Extensibility

#### Properties

- [Documentation](https://apidoc.factorialhr.com/reference)
- [OpenAPI](openapi/factorial-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/factorial.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/factorial.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Factorial Posts and Communities API

Groups, posts, and comments backing the Communities V2 feature. Requires Communities V2 to be enabled on the company.

- **Human URL:** [https://apidoc.factorialhr.com/reference](https://apidoc.factorialhr.com/reference)

#### Tags

- Communities
- Posts
- Communication

#### Properties

- [Documentation](https://apidoc.factorialhr.com/reference)
- [Postman Collection](collections/factorial.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/factorial.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Factorial Marketplace and Integrations API

Integrations Framework and Marketplace endpoints used by partner integrations to register, surface, and operate within the Factorial app.

- **Human URL:** [https://apidoc.factorialhr.com/docs/integrations-framework](https://apidoc.factorialhr.com/docs/integrations-framework)

#### Tags

- Integrations
- Marketplace

#### Properties

- [Documentation](https://apidoc.factorialhr.com/docs/integrations-framework)
- [Postman Collection](collections/factorial.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/factorial.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Factorial Keys and OAuth API

Two authentication methods. OAuth2 (authorization code flow at /oauth/authorize and /oauth/token) is used to act on behalf of a user; Credentials/API Keys (x-api-key header) are used to act on behalf of the company with full admin access. API Keys overrule OAuth tokens when both are present on the same request.

- **Human URL:** [https://apidoc.factorialhr.com/docs/authentication](https://apidoc.factorialhr.com/docs/authentication)

#### Tags

- Authentication
- OAuth2
- API Keys

#### Properties

- [Documentation](https://apidoc.factorialhr.com/docs/api-keys)
- [Documentation](https://apidoc.factorialhr.com/docs/oauth-2)
- [Documentation](https://apidoc.factorialhr.com/docs/oauth-scopes)
- [Documentation](https://apidoc.factorialhr.com/docs/create-a-new-oauth-application)
- [Documentation](https://apidoc.factorialhr.com/docs/oauth2-partner-guide)
- [Postman Collection](collections/factorial.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/factorial.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Portal](https://factorialhr.com)
- [Documentation](https://apidoc.factorialhr.com/)
- [Documentation](https://apidoc.factorialhr.com/reference)
- [Getting Started](https://apidoc.factorialhr.com/docs/getting-started)
- [Documentation](https://apidoc.factorialhr.com/docs/first-steps)
- [Documentation](https://apidoc.factorialhr.com/docs/authentication)
- [Documentation](https://apidoc.factorialhr.com/docs/oauth-2)
- [Documentation](https://apidoc.factorialhr.com/docs/oauth-scopes)
- [Documentation](https://apidoc.factorialhr.com/docs/api-keys)
- [Documentation](https://apidoc.factorialhr.com/docs/api-versioning)
- [Documentation](https://apidoc.factorialhr.com/docs/production-and-demo)
- [Documentation](https://apidoc.factorialhr.com/docs/pagination)
- [Documentation](https://apidoc.factorialhr.com/docs/faqs)
- [Changelog](https://apidoc.factorialhr.com/changelog)
- [Webhooks](https://apidoc.factorialhr.com/docs/manage-webhooks)
- [Documentation](https://apidoc.factorialhr.com/docs/webhooks-policies)
- [Documentation](https://apidoc.factorialhr.com/docs/integrations-framework)
- [Documentation](https://apidoc.factorialhr.com/docs/payroll-integrations)
- [Documentation](https://apidoc.factorialhr.com/docs/finance-integrations)
- [Pricing](https://factorialhr.com/pricing)
- [Sign Up](https://factorialhr.com/signup)
- [Login](https://app.factorialhr.com/users/sign_in)
- [Status Page](https://factorial.statuspage.io/)
- [Blog](https://factorialhr.com/blog)
- [Customers](https://factorialhr.com/customers)
- [Support](https://apidoc.factorialhr.com/docs/contact-page)
- [GitHub Organization](https://github.com/factorialco)
- [SDK](https://github.com/factorialco/oas)
- [SDK](https://github.com/factorialco/oas/tree/main/sdk-ruby)
- [SDK](https://github.com/factorialco/oas/tree/main/sdk-python)
- [SDK](https://github.com/factorialco/oas/tree/main/sdk-java)
- [SDK](https://github.com/factorialco/oas/tree/main/sdk-php)
- [SDK](https://github.com/factorialco/oas/tree/main/sdk-typescript-axios)
- [SDK](https://github.com/factorialco/oas/tree/main/sdk-nodejs-server)
- [Tool](https://github.com/factorialco/f0)
- [Privacy Policy](https://factorialhr.com/privacy-policy)
- [Terms of Service](https://factorialhr.com/terms-and-conditions)
- [LinkedIn](https://www.linkedin.com/company/factorial-hr/)
- [Plans](plans/factorial-plans-pricing.yml)
- [Rate Limits](rate-limits/factorial-rate-limits.yml)
- [Fin Ops](finops/factorial-finops.yml)
- [Spectral Rules](rules/factorial-rules.yml)
- [Vocabulary](vocabulary/factorial-hr-vocabulary.yml)
- [Features](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** info@apievangelist.com
**URL:** https://apievangelist.com
