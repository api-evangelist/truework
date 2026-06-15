# Truework (truework)

Truework operates a unified income and employment verification platform for mortgage lenders, credit unions, and fintechs. The Truework API orchestrates six verification methods — Instant Data, Payroll Credentials, Bank Credentials, Tax Credentials, Smart Outreach, and Document Upload — behind a single REST surface (api.truework.com), asynchronous webhooks, and the Truework.js / Truework Direct widget for consumer-permissioned verifications. The platform claims coverage of more than 97% of U.S. workers and 75% completion rates versus a ~48% industry average. Core resources are Orders, Verification Requests, Reports, and Order Events, with beta surfaces for Qualification Checks and Tenant Properties.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/truework/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/truework/refs/heads/main/apis.yml)

## Scope

- **Position:** Consuming
- **Access:** 3rd-Party

## Tags

- Verifications
- Income Verification
- Employment Verification
- VOIE
- Mortgage
- Lending
- Credit Unions
- Identity
- KYC
- Fintech

## Timestamps

- **Created:** 2026-05-24T00:00:00.000Z
- **Modified:** 2026-05-24

## APIs

### Truework Verifications API

Truework Verifications API for orders, reports, and order events. Submit a verification of income and employment (VOIE) order against a known target employer, run a synchronous employer search, kick off a Truework Direct (Truework.js) borrower-driven verification, retrieve completed verification reports, list and cancel orders, and replay the order event log. Six verification methods are orchestrated automatically: Instant Data, Payroll Credentials, Bank Credentials, Tax Credentials, Smart Outreach, and Document Upload. Current API version is 2023-10-30; pinned per API key via the Accept header.

- **Human URL:** [https://www.truework.com/docs/api-reference](https://www.truework.com/docs/api-reference)
- **Base URL:** `https://api.truework.com`

#### Tags

- Verifications
- VOIE
- Orders
- Reports
- Mortgage

#### Properties

- [Documentation](https://www.truework.com/docs/api-reference)
- [Documentation](https://www.truework.com/docs/api-reference/versions/2023-10-30)
- [OpenAPI](openapi/truework-verifications-orders-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/truework-verifications-orders.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/truework-verifications-orders.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/truework-order-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/truework-report-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON-LD](json-ld/truework-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)

### Truework Qualifications API (Beta)

Public beta surface for running qualification checks against a borrower's verified employment and income data. Create a qualification check, retrieve a check result, and list the qualification check sets defined for a tenant. Useful for low-latency knockout decisions (e.g. "minimum gross monthly income") layered on top of full verification reports.

- **Human URL:** [https://www.truework.com/docs/api-reference](https://www.truework.com/docs/api-reference)
- **Base URL:** `https://api.truework.com`

#### Tags

- Qualifications
- Decisioning
- Beta
- VOIE

#### Properties

- [Documentation](https://www.truework.com/docs/api-reference)
- [OpenAPI](openapi/truework-beta-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/truework-beta.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/truework-beta.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Truework Tenant Properties API (Beta)

Public beta surface for programmatically managing tenant-scoped configuration properties on Truework. Create, list, retrieve, and update tenant properties that govern verification behavior (allowed methods, branding, callback expectations) across the account.

- **Human URL:** [https://www.truework.com/docs/api-reference](https://www.truework.com/docs/api-reference)
- **Base URL:** `https://api.truework.com`

#### Tags

- Configuration
- Tenant
- Beta

#### Properties

- [Documentation](https://www.truework.com/docs/api-reference)
- [OpenAPI](openapi/truework-beta-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/truework-beta.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/truework-beta.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Truework Webhooks

Truework emits two webhook event types — `order.completed` when every verification on an order is finished, and `verification_request.state.change` as individual verifications transition through pending-approval, processing, action-required, completed, canceled, and invalid. Each webhook destination is associated with a token delivered in the `X-Truework-Token` header so receivers can authenticate the call. Failed deliveries are retried periodically for up to 48 hours. Accounts may register up to 10 webhook destinations.

- **Human URL:** [https://www.truework.com/docs/api-reference/webhooks](https://www.truework.com/docs/api-reference/webhooks)

#### Tags

- Webhooks
- Events

#### Properties

- [Documentation](https://www.truework.com/docs/api-reference/webhooks)
- [Documentation](https://www.truework.com/docs/api-reference/webhooks/security)
- [OpenAPI](openapi/truework-webhooks-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/truework-webhooks.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/truework-webhooks.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Truework.js (Truework Direct)

Truework.js is the client-side JavaScript library that powers Truework Direct, the borrower-driven (consumer-permissioned) verification flow. The host page loads `https://js.truework.com/v1` and initializes the widget with a session token created server-side via POST /orders/truework-direct, then handles `onComplete`, `onClose`, and `onError` callbacks. Publishable keys (`tw_pk_*` / `tw_pk_test_*`) authenticate the client.

- **Human URL:** [https://www.truework.com/docs/guides/truework-direct/truework-js-reference](https://www.truework.com/docs/guides/truework-direct/truework-js-reference)
- **Base URL:** `https://js.truework.com/v1`

#### Tags

- JavaScript
- SDK
- Embedded

#### Properties

- [Documentation](https://www.truework.com/docs/guides/truework-direct/truework-js-reference)
- [Documentation](https://www.truework.com/docs/guides/truework-direct/getting-started)
- [Code Examples](https://github.com/truework/truework.js-examples)
- [Postman Collection](collections/truework-beta.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/truework-beta.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/truework-verifications-orders.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/truework-verifications-orders.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/truework-webhooks.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/truework-webhooks.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Portal](https://www.truework.com)
- [Documentation](https://www.truework.com/docs)
- [Documentation](https://www.truework.com/docs/api-reference)
- [Documentation](https://www.truework.com/docs/api-reference/versions/2023-10-30)
- [Documentation](https://www.truework.com/docs/api-reference/versions)
- [Versioning](https://www.truework.com/docs/api-reference/versions)
- [Authentication](https://www.truework.com/docs/api-reference/authentication)
- [Rate Limits](https://www.truework.com/docs/api-reference/limits)
- [Errors](https://www.truework.com/docs/api-reference/versions/2023-10-30)
- [Sandbox](https://www.truework.com/docs/api-reference/sandbox)
- [Documentation](https://www.truework.com/docs/api-reference/sandbox/test-cases)
- [Documentation](https://www.truework.com/docs/api-reference/monitoring)
- [Webhooks](https://www.truework.com/docs/api-reference/webhooks)
- [Documentation](https://www.truework.com/docs/api-reference/webhooks/security)
- [Documentation](https://www.truework.com/docs/guides)
- [Getting Started](https://www.truework.com/docs/guides/api/getting-started)
- [Documentation](https://www.truework.com/docs/guides/methods)
- [Documentation](https://www.truework.com/docs/guides/workflows)
- [Documentation](https://www.truework.com/docs/guides/truework-direct/getting-started)
- [Documentation](https://www.truework.com/docs/guides/truework-direct/truework-js-reference)
- [Documentation](https://www.truework.com/docs/guides/mortgage/mortgage-intro)
- [Documentation](https://www.truework.com/docs/guides/mortgage/mortgage-los)
- [Documentation](https://www.truework.com/docs/guides/mortgage/mortgage-pos)
- [Portal](https://www.truework.com/products/api)
- [Portal](https://www.truework.com/products)
- [Sign Up](https://app.truework.com/requester/signup)
- [Login](https://app.truework.com/requester/login)
- [Sandbox](https://api.truework-sandbox.com)
- [Status Page](https://truework.statuspage.io)
- [Support](https://help.truework.com)
- [Documentation](https://www.truework.com/legal/terms)
- [Privacy Policy](https://www.truework.com/legal/privacy)
- [GitHub Organization](https://github.com/truework)
- [SDK](https://github.com/truework/truework.js-examples)
- [Tool](https://github.com/truework/gretchen)
- [Tool](https://github.com/truework/mounty)
- [LinkedIn](https://www.linkedin.com/company/truework)
- [Blog](https://www.truework.com/resource-center/blog)
- [Plans](plans/truework-plans-pricing.yml)
- [Rate Limits](rate-limits/truework-rate-limits.yml)
- [Fin Ops](finops/truework-finops.yml)
- [Features](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** info@apievangelist.com
**URL:** https://apievangelist.com
