# Truework

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

Truework operates a unified income and employment verification platform for mortgage lenders, credit unions, and fintechs. The Truework API orchestrates six verification methods — Instant Data, Payroll Credentials, Bank Credentials, Tax Credentials, Smart Outreach, and Document Upload — behind a single REST surface (api.truework.com), asynchronous webhooks, and the Truework.js / Truework Direct widget for consumer-permissioned verifications. The platform claims coverage of more than 97% of U.S. workers and 75% completion rates versus a ~48% industry average. Core resources are Orders, Verification Requests, Reports, and Order Events, with beta surfaces for Qualification Checks and Tenant Properties.

**Areas:** Verification · Income Verification · Employment Verification · VOIE · Mortgage · Lending · Credit Union · Identity · KYC · Fintech

## Truework on APIs.io

Everything profiled for Truework is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/truework/](https://apis.io/providers/truework/)** — or go straight to one of the APIs or properties below.

### APIs (6)

- [Truework.js (Truework Direct)](https://apis.io/apis/truework/truework-js/) — Truework.js is the client-side JavaScript library that powers Truework Direct, the borrower-driven (consumer-permissioned) verification flow. The host page…
- [Truework Subpackage Orders API](https://apis.io/apis/truework/truework-subpackage-orders-api/) — The subpackage_orders API from Truework — 8 operation(s) for subpackage_orders.
- [Truework Subpackage Qualification Checks API](https://apis.io/apis/truework/truework-subpackage-qualificationchecks-api/) — The subpackage_qualificationChecks API from Truework — 3 operation(s) for subpackage_qualificationchecks.
- [Truework Subpackage Reports API](https://apis.io/apis/truework/truework-subpackage-reports-api/) — The subpackage_reports API from Truework — 1 operation(s) for subpackage_reports.
- [Truework Subpackage Tenant Properties API](https://apis.io/apis/truework/truework-subpackage-tenantproperties-api/) — The subpackage_tenantProperties API from Truework — 2 operation(s) for subpackage_tenantproperties.
- [Truework Webhooks API](https://apis.io/apis/truework/truework-truework-webhooks-api/) — The Truework Webhooks API from Truework — 0 operation(s) for truework webhooks.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Truework Agentic Access](https://apis.io/agentic-access/truework/truework-agentic-access/)

#### JSON Schema (2)

The data models the API reads and writes.

- [Truework Order](https://apis.io/schemas/truework/truework-order/)
- [Truework Verification Report](https://apis.io/schemas/truework/truework-report/)

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [Truework Context](https://apis.io/jsonld/truework/truework-context/)

#### Collections (11)

Postman and Open Collection request collections.

- [Truework Qualifications & Tenant Properties API (Beta)](https://apis.io/collections/truework/open-truework-beta/)
- [Truework Qualifications & Tenant Properties API (Beta) subpackage_orders API](https://apis.io/collections/truework/open-truework-subpackage-orders-api/)
- [Truework Qualifications & Tenant Properties API (Beta) subpackage_orders subpackage_qualificationChecks API](https://apis.io/collections/truework/open-truework-subpackage-qualificationchecks-api/)
- [Truework Qualifications & Tenant Properties API (Beta) subpackage_orders subpackage_reports API](https://apis.io/collections/truework/open-truework-subpackage-reports-api/)
- [Truework Qualifications & Tenant Properties API (Beta) subpackage_orders subpackage_tenantProperties API](https://apis.io/collections/truework/open-truework-subpackage-tenantproperties-api/)
- [Truework Verifications API](https://apis.io/collections/truework/open-truework-verifications-orders/)
- [Truework Webhooks](https://apis.io/collections/truework/open-truework-webhooks/)
- [Truework Qualifications & Tenant Properties API (Beta) subpackage_orders API](https://apis.io/collections/truework/postman-truework-subpackage-orders-api/)
- [Truework Qualifications & Tenant Properties API (Beta) subpackage_orders subpackage_qualificationChecks API](https://apis.io/collections/truework/postman-truework-subpackage-qualificationchecks-api/)
- [Truework Qualifications & Tenant Properties API (Beta) subpackage_orders subpackage_reports API](https://apis.io/collections/truework/postman-truework-subpackage-reports-api/)
- [Truework Qualifications & Tenant Properties API (Beta) subpackage_orders subpackage_tenantProperties API](https://apis.io/collections/truework/postman-truework-subpackage-tenantproperties-api/)

#### Governance rules (1)

Spectral rulesets for the provider's contracts.

- [Truework — jsonschema rules](https://apis.io/rules/truework/truework-jsonschema-spectral-rules/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Truework Authentication](https://apis.io/security/truework/truework-authentication/)
- [Truework Domain Security](https://apis.io/security/truework/truework-domain-security/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Truework Plans Pricing](https://apis.io/plans/truework/truework-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Truework Rate Limits](https://apis.io/rate-limits/truework/truework-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Truework Finops](https://apis.io/finops/truework/truework-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.truework.com/)
- [Documentation](https://www.truework.com/docs)
- [Getting started](https://www.truework.com/docs/guides/api/getting-started)
- [Support](https://help.truework.com)
- [Blog](https://www.truework.com/resource-center/blog)
- [Privacy policy](https://www.truework.com/legal/privacy)
- [GitHub](https://github.com/truework)
- [Status](https://truework.statuspage.io)

## API Evangelist rating

**Kin Score 46.7** — developing · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 71.4 |
| Contract quality | 64.4 |
| Contract governance | 9.8 |
| Operational transparency | 50.0 |
| Developer ergonomics | 65.5 |
| Access clarity | 22.4 |

**Agent readiness 36.5** — agent-ready

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | documented (partial credit) |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | documented (partial credit) |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | yes |
| Agent Skills | — |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | paginated |
| Operation Distinctiveness | distinct |

**Regulatory alignment 13.4** — Banking & Open Finance

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/truework/](https://apis.io/providers/truework/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Truework: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/truework/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
