# amc-entertainment-holdings

Profile for **AMC Entertainment Holdings** in the API Evangelist network. Fortune 2024 (rank 659).

AMC Entertainment Holdings is the largest movie exhibition company in the United States and the world,
operating AMC Theatres, AMC Stubs loyalty programs, and related entertainment brands. AMC publishes a
public developer portal at [developers.amctheatres.com](https://developers.amctheatres.com) that exposes
a REST API for movies, showtimes, theatres, locations, seating, ticketing, concessions, AMC Stubs
loyalty, refunds, fee waivers, barcodes, and webhooks.

## Quick Facts

- **Developer Portal:** https://developers.amctheatres.com (the live portal blocks scrapers).
- **Base URL:** `https://api.amctheatres.com`
- **Authentication:** API key sent in the `X-AMC-Vendor-Key` header.
- **Versioning:** Resource families are independently versioned under `/v1`, `/v2`, `/v3`, `/v4`.
- **Response envelope:** HAL-style with `pageSize`, `pageNumber`, `count`, `_embedded`, `_links`.
- **GitHub:** [github.com/amctheatres](https://github.com/amctheatres) (organization exists; no public repos).

## APIs Profiled

| API | Description |
| --- | --- |
| [AMC Theatres API](openapi/amc-theatres-api-openapi.yml) | REST API for theatres, movies, showtimes, locations, markets, seating, orders, payments, concessions, AMC Stubs loyalty, refunds, fee waivers, barcodes, and webhooks. |

## Repository Layout

```
amc-entertainment-holdings/
├── apis.yml                                  Provider profile (apis.json 0.19)
├── README.md
├── openapi/
│   └── amc-theatres-api-openapi.yml          Reconstructed OpenAPI 3.0.3 spec (73 paths, 45 schemas)
├── rules/
│   └── amc-theatres-rules.yml                Spectral ruleset for AMC API conventions
├── capabilities/
│   ├── shared/
│   │   └── amc-theatres-api.yaml             Naftiko shared per-API consumed definition
│   ├── movie-discovery.yaml                  Movie/theatre/showtime discovery workflow
│   ├── ticket-purchase.yaml                  End-to-end ticket and concessions ordering workflow
│   └── loyalty-management.yaml               AMC Stubs loyalty management workflow
├── json-schema/
│   ├── amc-theatres-theatre-schema.json
│   ├── amc-theatres-movie-schema.json
│   ├── amc-theatres-showtime-schema.json
│   ├── amc-theatres-order-schema.json
│   ├── amc-theatres-loyalty-account-schema.json
│   └── amc-theatres-attribute-schema.json
├── json-structure/
│   ├── amc-theatres-theatre-structure.json
│   ├── amc-theatres-movie-structure.json
│   ├── amc-theatres-showtime-structure.json
│   ├── amc-theatres-order-structure.json
│   └── amc-theatres-loyalty-account-structure.json
├── json-ld/
│   └── amc-entertainment-holdings-context.jsonld
├── examples/
│   ├── amc-theatres-list-theatres-example.json
│   ├── amc-theatres-list-movies-now-playing-example.json
│   ├── amc-theatres-list-theatre-showtimes-example.json
│   ├── amc-theatres-create-order-example.json
│   └── amc-theatres-get-loyalty-account-example.json
└── vocabulary/
    └── amc-entertainment-holdings-vocabulary.yml
```

## Resource Families

The AMC Theatres API exposes the following resource families. Versions reflect the path prefix used in
the public developer documentation.

| Resource | Version | Description |
| --- | --- | --- |
| Theatres | v2 | Theatre locations, attributes, brands, and metadata. |
| Movies | v2 | Movies and views (`now-playing`, `advance`, `coming-soon`, `on-demand`). |
| Showtimes | v2 | Showtimes by theatre, date, embargo status, and proximity to a coordinate. |
| Locations | v2 | Locations by state, theatre name, and location-suggestion search. |
| Markets | v1 | AMC market areas. |
| States | v1 | U.S. states served. |
| Media | v2 | Movie, theatre, and attribute imagery and video. |
| Attributes | v1/v2 | Movie/showtime/theatre attribute taxonomy (IMAX, Atmos, Reserved Seating, etc.). |
| Seating Layouts | v2 | Seating layouts for performances and auditoriums. |
| Orders | v3 | Order creation, products, payments, fulfillment, and recording. |
| Concessions | v1 | Concessions, categories, delivery locations, pickup/delivery times. |
| Loyalty | v4 | AMC Stubs loyalty accounts, cards, redemptions, and registrations. |
| Refunds | v1 | Refund reasons, fee waivers, and refunds. |
| Barcodes | v3 | Ticket and loyalty QR codes and Code 128 barcodes. |
| Webhooks | v1 | Webhook event subscriptions and management. |
| Wallet | v4 | External wallet for use by external billers. |

## Naftiko Capabilities

Three workflow-oriented capabilities compose the AMC Theatres API into reusable building blocks:

- **[Movie Discovery](capabilities/movie-discovery.yaml)** — Surface movies, theatres, and showtimes for entertainment listings, voice assistants, and AI concierges.
- **[Ticket Purchase](capabilities/ticket-purchase.yaml)** — End-to-end orders: create order, add products, add payment, apply AMC Stubs rewards.
- **[AMC Stubs Loyalty Management](capabilities/loyalty-management.yaml)** — Look up loyalty accounts and redeem points for customer-care and loyalty partners.

Each workflow consumes the shared [`capabilities/shared/amc-theatres-api.yaml`](capabilities/shared/amc-theatres-api.yaml) definition, which binds the `AMC_VENDOR_KEY` environment variable to the `X-AMC-Vendor-Key` header.

## Notes on Source Material

The AMC developer portal at developers.amctheatres.com aggressively blocks automated retrieval, so the
OpenAPI spec, JSON Schemas, and examples in this repository were reconstructed from a combination of:

1. A community-maintained snapshot of the AMC Developer Portal HTML documentation captured by the
   open-source [ialexryan/amc-showtime-monitor](https://github.com/ialexryan/amc-showtime-monitor)
   project.
2. The [StateMachineJunkie/AMCAPI](https://github.com/StateMachineJunkie/AMCAPI) Swift client for
   schema cross-referencing.
3. Live request signatures observed in the open-source `amc-showtime-monitor` TypeScript client
   (auth header, base URL, HAL envelope conventions).

This is a best-effort reconstruction; consult the official developer portal for the canonical contract.
