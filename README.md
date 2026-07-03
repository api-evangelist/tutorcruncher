# TutorCruncher (tutorcruncher)

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
