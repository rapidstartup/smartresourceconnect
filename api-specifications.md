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