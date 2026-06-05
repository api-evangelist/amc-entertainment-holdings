# AMC Entertainment Holdings (amc-entertainment-holdings)

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
