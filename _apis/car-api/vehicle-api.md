---
aid: car-api:vehicle-api
baseURL: https://carapi.app/api
description: The CarAPI Vehicle API provides REST/JSON access to a vehicle database covering year/make/model (1900-2026), sub-models, trims (1990-2026), bodies, engines, mileage, interior, and exterior attributes. Authentication uses JWT tokens obtained from /api/auth/login with an api_token and api_secret. The API supports pagination (up to 1000 per page), sorting, JSON filter queries with operators, and modified-since caching. Responses are available as application/json, application/ld+json, and application/hal+json. CORS is not supported; the API is intended for server-side integration.
humanURL: https://carapi.app/
image: ''
layout: api
name: CarAPI Vehicle API
properties:
- type: Documentation
  url: https://carapi.app/
- type: Developer
  url: https://carapi.app/docs
- type: API
  url: https://carapi.app/api
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/car-api/refs/heads/main/openapi/car-api-openapi-original.yml
provider_name: Car API (carapi.app)
provider_slug: car-api
slug: vehicle-api
tags:
- Automobiles
- Vehicle API
- Vehicle Specifications
- Vehicles
---
