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
source_yaml: "aid: car-api:vehicle-api\nname: CarAPI Vehicle API\ndescription: The CarAPI Vehicle API provides REST/JSON access to a vehicle database covering year/make/model\n  (1900-2026), sub-models, trims (1990-2026), bodies, engines, mileage, interior, and exterior attributes.\n  Authentication uses JWT tokens obtained from /api/auth/login with an api_token and api_secret. The API\n  supports pagination (up to 1000 per page), sorting, JSON filter queries with operators, and modified-since\n  caching. Responses are available as application/json, application/ld+json, and application/hal+json.\n  CORS is not supported; the API is intended for server-side integration.\nhumanURL: https://carapi.app/\nbaseURL: https://carapi.app/api\ntags:\n- Automobiles\n- Vehicle API\n- Vehicle Specifications\n- Vehicles\nproperties:\n- url: https://carapi.app/\n  type: Documentation\n- url: https://carapi.app/docs\n  type: Developer\n- url: https://carapi.app/api\n  type: API\n- url: openapi/car-api-openapi-original.yml\n\
  \  type: OpenAPI\nx-features:\n- REST/JSON vehicle database with OpenAPI documentation\n- Year/make/model coverage 1900-2026 (trims 1990-2026)\n- JWT authentication via /api/auth/login endpoint\n- Pagination, sorting, and JSON filter queries with in/>=/operators\n- JSON, JSON-LD (application/ld+json), and HAL (application/hal+json) responses\n- Modified-since timestamps for cache validation\n- Swagger UI, ReDoc, Postman, and GitHub docs\n- Public dataset available without account for prototyping\nx-use-cases:\n- Vehicle dropdowns and VIN-aware forms in auto-commerce apps\n- Automotive marketplaces and classifieds\n- Fleet management and telematics dashboards\n- Insurance quoting and underwriting vehicle lookups\n- Repair shop and service advisor applications\n- Vehicle research and comparison tools\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/car-api/refs/heads/main/apis.yml
tags:
- Automobiles
- Vehicle API
- Vehicle Specifications
- Vehicles
---
