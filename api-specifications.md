# API Specifications

Smart Resource Connect provides a REST API for third-party integrations, enabling external systems to submit surplus listings, post resource needs, and query for matches.

## Authentication and Security

- Bearer Token Authentication (JWT)
- HTTPS required for all API calls

## Core API Endpoints

- `GET /v1/surplus`: List surplus resources
- `GET /v1/demand`: List resource demands
- `POST /v1/surplus`: Create surplus listing
- `POST /v1/demand`: Create demand listing
- `GET /v1/surplus/{id}`: Get surplus details
- `GET /v1/demand/{id}`: Get demand details
- `GET /v1/match`: Matchmaking endpoint
- `PUT/PATCH /v1/surplus/{id}`: Update surplus listings
- `PUT/PATCH /v1/demand/{id}`: Update demand listings

## Updated API Endpoints

- `GET /api/surplus` & `GET /api/demand`: List items with optional filters (category, location, status), pagination enforced.
- `POST /api/surplus` & `POST /api/demand`: Create new entries, validate required fields, auto-set `posted_at` and default status.
- `PUT/PATCH /api/surplus/{id}` & `PUT/PATCH /api/demand/{id}`: Update records or mark status as fulfilled/closed, ownership checks enforced.

## Matching Endpoint

- `GET /api/match?surplusId={id}` or `GET /api/match?demandId={id}`: Returns potential matches with scoring.

### Matching Algorithm Scoring

- **Category match**: +0.4
- **Location match**: +0.3
- **Sufficient quantity**: +0.2
- **Valid timeframe**: +0.1

Final score ranges from 0 to 1, sorted by highest score. 