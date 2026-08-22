# TutorCruncher (tutorcruncher)

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

TutorCruncher is tutoring business management software for agencies, companies, and independent tutors - handling clients, students, tutors, lesson scheduling, invoicing, and payments. Its documented REST API (base `https://app.tutorcruncher.com/api/`, token-authenticated) exposes clients, recipients (students), contractors (tutors), agents, services (jobs), appointments (lessons), invoices, payment orders, proforma invoices, ad hoc charges, and reference data, with HTTP webhooks for event notifications. Its "Socket" product is a JavaScript embed for publishing public tutor and lesson listings on a provider's own website - not a WebSocket API.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/tutorcruncher/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/tutorcruncher/refs/heads/main/apis.yml)

## Authentication & Conventions

- **Base URL:** `https://app.tutorcruncher.com/api/`
- **Auth:** private API key (from Integrations) in the `Authorization` header as `token <API KEY>`
- **Rate limit:** 100 requests per minute
- **Pagination:** list endpoints return up to 100 objects per page (`count`, `next`, `previous`, `results`)
- **Version:** API v2 (v1 deprecated 2025-07-03); users are updated by ID via POST

## Tags

- Tutoring
- Education
- Business Management
- Scheduling
- Invoicing
- Payments
- EdTech

## Timestamps

- **Created:** 2026-07-03
- **Modified:** 2026-07-03

## APIs

### TutorCruncher Clients API

Create, list, retrieve, update, and delete clients - the paying customers (parents or organizations) in a TutorCruncher account.

- **Human URL:** [https://api.tutorcruncher.com/](https://api.tutorcruncher.com/)
- **Base URL:** `https://app.tutorcruncher.com/api`

#### Tags

- Clients
- CRM
- Users

#### Properties

- [Documentation](https://api.tutorcruncher.com/)
- [API Reference](https://api.tutorcruncher.com/)
- [OpenAPI](openapi/tutorcruncher-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/tutorcruncher.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/tutorcruncher.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### TutorCruncher Recipients (Students) API

Manage recipients - the students who receive tutoring - linked to a paying client and enrolled onto services and appointments.

- **Human URL:** [https://api.tutorcruncher.com/](https://api.tutorcruncher.com/)
- **Base URL:** `https://app.tutorcruncher.com/api`

#### Tags

- Recipients
- Students
- Users

#### Properties

- [API Reference](https://api.tutorcruncher.com/)
- [OpenAPI](openapi/tutorcruncher-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/tutorcruncher.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/tutorcruncher.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### TutorCruncher Contractors (Tutors) API

Manage contractors - the tutors delivering lessons - including availability, skills, subjects, and qualification levels. Public contractor profiles are exposed read-only for website listings.

- **Human URL:** [https://api.tutorcruncher.com/](https://api.tutorcruncher.com/)
- **Base URL:** `https://app.tutorcruncher.com/api`

#### Tags

- Contractors
- Tutors
- Availability

#### Properties

- [API Reference](https://api.tutorcruncher.com/)
- [OpenAPI](openapi/tutorcruncher-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/tutorcruncher.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/tutorcruncher.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### TutorCruncher Services (Jobs) API

Manage services (jobs) that tie recipients and contractors together with a rate and subject; add or remove contractors and recipients from a service.

- **Human URL:** [https://api.tutorcruncher.com/](https://api.tutorcruncher.com/)
- **Base URL:** `https://app.tutorcruncher.com/api`

#### Tags

- Services
- Jobs
- Enrollment

#### Properties

- [API Reference](https://api.tutorcruncher.com/)
- [OpenAPI](openapi/tutorcruncher-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/tutorcruncher.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/tutorcruncher.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### TutorCruncher Appointments (Lessons) API

Schedule and manage appointments - the individual lessons or sessions delivered under a service - and manage their recipients and contractors.

- **Human URL:** [https://api.tutorcruncher.com/](https://api.tutorcruncher.com/)
- **Base URL:** `https://app.tutorcruncher.com/api`

#### Tags

- Appointments
- Lessons
- Scheduling

#### Properties

- [API Reference](https://api.tutorcruncher.com/)
- [OpenAPI](openapi/tutorcruncher-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/tutorcruncher.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/tutorcruncher.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### TutorCruncher Invoices API

List, retrieve, and create client invoices and take payment against them.

- **Human URL:** [https://api.tutorcruncher.com/](https://api.tutorcruncher.com/)
- **Base URL:** `https://app.tutorcruncher.com/api`

#### Tags

- Invoices
- Billing
- Finance

#### Properties

- [API Reference](https://api.tutorcruncher.com/)
- [OpenAPI](openapi/tutorcruncher-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/tutorcruncher.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/tutorcruncher.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### TutorCruncher Payments API

Manage payment orders (contractor payouts), proforma invoices (client credit requests) with take-payment, and ad hoc charges and their categories.

- **Human URL:** [https://api.tutorcruncher.com/](https://api.tutorcruncher.com/)
- **Base URL:** `https://app.tutorcruncher.com/api`

#### Tags

- Payments
- Payouts
- Charges

#### Properties

- [API Reference](https://api.tutorcruncher.com/)
- [OpenAPI](openapi/tutorcruncher-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/tutorcruncher.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/tutorcruncher.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### TutorCruncher Webhooks and Action Types API

Discover the 150+ action types that can fire, then receive HTTP webhook POSTs (HMAC-SHA256 signed, retried with exponential backoff) at a URL configured in System > Settings > Integrations. This is HTTP push, not a WebSocket.

- **Human URL:** [https://api.tutorcruncher.com/](https://api.tutorcruncher.com/)
- **Base URL:** `https://app.tutorcruncher.com/api`

#### Tags

- Webhooks
- Events
- Integrations

#### Properties

- [Documentation](https://api.tutorcruncher.com/)
- [Documentation](https://help.tutorcruncher.com/en/articles/4843207-tutorcruncher-sockets)
- [OpenAPI](openapi/tutorcruncher-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/tutorcruncher.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/tutorcruncher.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [GitHub Organization](https://github.com/tutorcruncher)
- [LinkedIn](https://www.linkedin.com/company/tutorcruncher)
- [Website](https://tutorcruncher.com)
- [Documentation](https://api.tutorcruncher.com/)
- [Plans](plans/tutorcruncher-plans-pricing.yml)
- [Rate Limits](rate-limits/tutorcruncher-rate-limits.yml)
- [Fin Ops](finops/tutorcruncher-finops.yml)

## WebSocket Review

**Does TutorCruncher expose a documented public WebSocket API?** No. The public API is request/response REST, and asynchronous events are delivered via HTTP webhooks (server-to-endpoint push), not a WebSocket or SSE stream. TutorCruncher's "Socket" product is a JavaScript embed (`cdn.tutorcruncher.com/socket/latest/socket.js`) for public tutor/lesson listings on a website - a front-end widget, not a network socket. See [review.yml](review.yml).

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
