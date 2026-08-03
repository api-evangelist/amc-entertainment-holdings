# AMC Entertainment Holdings (amc-entertainment-holdings)

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
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

AMC Entertainment Holdings is the largest movie exhibition company in the United States and the world, operating AMC Theatres, AMC Stubs loyalty programs, and related entertainment brands. AMC publishes a public developer portal at developers.amctheatres.com that exposes a REST API for movies, showtimes, theatres, locations, seating, ticketing, concessions, AMC Stubs loyalty, refunds, fee waivers, barcodes, and webhooks. The API is the primary integration surface for distributors, partners, and third-party developers building movie discovery, ticket sales, and AMC Stubs co-marketing experiences.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/amc-entertainment-holdings/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/amc-entertainment-holdings/refs/heads/main/apis.yml)

## Scope

- **Type:** Index

## Tags

- Entertainment
- Movies
- Theatres
- Showtimes
- Ticketing
- Concessions
- Loyalty
- Fortune 500

## Timestamps

- **Created:** 2026-05-04
- **Modified:** 2026-05-19

## APIs

### AMC Theatres API

The AMC Theatres API is a public REST API providing programmatic access to AMC Theatres data including theatres, locations, showtimes, movies, seating, ticketing, concessions, and AMC Stubs loyalty. The API is intended for partner integrations such as movie discovery, ticketing, and entertainment listings. Authentication is performed via a vendor API key issued through the AMC developer portal and supplied in the X-AMC-Vendor-Key header. Resource families are versioned independently under /v1, /v2, /v3, and /v4 path prefixes, and collection responses use a HAL-style envelope.

- **Human URL:** [https://developers.amctheatres.com](https://developers.amctheatres.com)
- **Base URL:** `https://api.amctheatres.com`

#### Tags

- Theatres
- Showtimes
- Movies
- Ticketing
- Concessions
- Loyalty
- Webhooks

#### Properties

- [Developer Portal](https://developers.amctheatres.com)
- [Documentation](https://developers.amctheatres.com)
- [Authentication](https://developers.amctheatres.com/GettingStarted/Authentication)
- [Sandbox](https://developers.amctheatres.com/GettingStarted/Sandbox)
- [OpenAPI](openapi/amc-theatres-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/amc-theatres-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/amc-theatres-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Spectral Rules](rules/amc-theatres-rules.yml)
- [Naftiko Shared Capability](capabilities/shared/amc-theatres-api.yaml)
- [JSON Schema](json-schema/amc-theatres-theatre-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/amc-theatres-movie-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/amc-theatres-showtime-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/amc-theatres-order-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/amc-theatres-loyalty-account-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/amc-theatres-attribute-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/amc-theatres-theatre-structure.json)
- [JSON Structure](json-structure/amc-theatres-movie-structure.json)
- [JSON Structure](json-structure/amc-theatres-showtime-structure.json)
- [JSON Structure](json-structure/amc-theatres-order-structure.json)
- [JSON Structure](json-structure/amc-theatres-loyalty-account-structure.json)
- [JSON-LD](json-ld/amc-entertainment-holdings-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Vocabulary](vocabulary/amc-entertainment-holdings-vocabulary.yml)
- [Example](examples/amc-theatres-list-theatres-example.json)
- [Example](examples/amc-theatres-list-movies-now-playing-example.json)
- [Example](examples/amc-theatres-list-theatre-showtimes-example.json)
- [Example](examples/amc-theatres-create-order-example.json)
- [Example](examples/amc-theatres-get-loyalty-account-example.json)

## Common Properties

- [Website](https://www.amctheatres.com)
- [Developer Portal](https://developers.amctheatres.com)
- [Customers](https://www.amctheatres.com/amcstubs)
- [Terms of Service](https://www.amctheatres.com/legal/terms-of-use)
- [Privacy Policy](https://www.amctheatres.com/legal/privacy-policy)
- [LinkedIn](https://www.linkedin.com/company/amc-theatres)
- [Git Hub](https://github.com/amctheatres)

## Maintainers

**FN:** API Evangelist
**URL:** https://apievangelist.com
