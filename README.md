# Truework (truework)

Truework operates a unified income and employment verification platform for mortgage lenders, credit unions, and fintechs. The Truework API orchestrates six verification methods — Instant Data, Payroll Credentials, Bank Credentials, Tax Credentials, Smart Outreach, and Document Upload — behind a single REST surface (`api.truework.com`), asynchronous webhooks, and the Truework.js / Truework Direct widget for consumer-permissioned verifications. The platform claims coverage of more than 97% of U.S. workers and 75% completion rates versus a ~48% industry average.

**URL:** [Visit APIs.json](https://raw.githubusercontent.com/api-evangelist/truework/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags

- Verifications, Income Verification, Employment Verification, VOIE, Mortgage, Lending, Credit Unions, Identity, KYC, Fintech

## Timestamps

- **Created:** 2026-05-24
- **Modified:** 2026-05-24

## Environments

| Environment | Base URL | Key Prefix |
|---|---|---|
| Production | `https://api.truework.com` | `tw_sk_` |
| Sandbox | `https://api.truework-sandbox.com` | `tw_sk_test_` |
| Truework.js | `https://js.truework.com/v1` | `tw_pk_` / `tw_pk_test_` |

## APIs

### Truework Verifications API

Orders, reports, and order events. Submit a VOIE order against a known target employer, run a synchronous employer search, kick off a Truework Direct borrower-driven verification, retrieve reports, list and cancel orders, and replay order event logs.

**Human URL:** [https://www.truework.com/docs/api-reference](https://www.truework.com/docs/api-reference)

- [Documentation](https://www.truework.com/docs/api-reference)
- [API Version 2023-10-30](https://www.truework.com/docs/api-reference/versions/2023-10-30)
- [OpenAPI](openapi/truework-verifications-orders-openapi.yml)
- [JSON Schema — Order](json-schema/truework-order-schema.json)
- [JSON Schema — Report](json-schema/truework-report-schema.json)
- [JSON-LD](json-ld/truework-context.jsonld)
- [Naftiko Capability — Orders](capabilities/verifications-orders.yaml)
- [Naftiko Capability — Reports](capabilities/verifications-reports.yaml)

### Truework Qualifications API (Beta)

Public beta surface for low-latency knockout decisioning against a borrower's verified income and employment.

- [Documentation](https://www.truework.com/docs/api-reference)
- [OpenAPI](openapi/truework-beta-openapi.yml)
- [Naftiko Capability — Qualification Checks](capabilities/qualifications-checks.yaml)

### Truework Tenant Properties API (Beta)

Public beta surface for managing tenant-scoped configuration properties that govern verification behavior across the account.

- [OpenAPI](openapi/truework-beta-openapi.yml)
- [Naftiko Capability — Tenant Properties](capabilities/tenant-properties.yaml)

### Truework Webhooks

`order.completed` and `verification_request.state.change` events authenticated via the `X-Truework-Token` header. Up to 10 destinations per account; 48-hour retry on failure.

- [Documentation](https://www.truework.com/docs/api-reference/webhooks)
- [Webhook Security](https://www.truework.com/docs/api-reference/webhooks/security)
- [OpenAPI](openapi/truework-webhooks-openapi.yml)
- [Naftiko Capability — Webhook Receiver](capabilities/webhooks-events.yaml)

### Truework.js (Truework Direct)

Client-side JavaScript library loaded from `https://js.truework.com/v1` that powers the Truework Direct borrower-driven verification widget.

- [Truework.js Reference](https://www.truework.com/docs/guides/truework-direct/truework-js-reference)
- [Getting Started](https://www.truework.com/docs/guides/truework-direct/getting-started)
- [Examples on GitHub](https://github.com/truework/truework.js-examples)

## Authentication

Bearer-token API keys generated in the [developer settings](https://app.truework.com/requester/developer-settings):

- Production secret keys are prefixed `tw_sk_`.
- Sandbox secret keys are prefixed `tw_sk_test_`.
- Publishable keys for Truework.js use `tw_pk_` / `tw_pk_test_`.

Version selection uses the standard HTTP `Accept` header (`Accept: application/json; version=2023-10-30`). Downgrading below an API key's pinned version returns HTTP 406.

## Rate Limits

- 10 requests per second per source IP
- 10 requests per second per account
- HTTP 429 on overage; exponential backoff recommended
- 10 webhook destinations per account
- Custom limits via `implementations@truework.com`

See [rate-limits/truework-rate-limits.yml](rate-limits/truework-rate-limits.yml).

## Plans & Pricing

Truework sells through Sales/Demo motions; per-unit verification pricing is contract-driven and not published publicly. The captured commercial surface is in [plans/truework-plans-pricing.yml](plans/truework-plans-pricing.yml) and the FOCUS-aligned billing surface in [finops/truework-finops.yml](finops/truework-finops.yml).

## Status & Support

- [Status Page](https://truework.statuspage.io)
- [Help Center](https://help.truework.com)
- Implementations: `implementations@truework.com`

## Maintainers

- [Kin Lane](https://apievangelist.com) — `info@apievangelist.com`
