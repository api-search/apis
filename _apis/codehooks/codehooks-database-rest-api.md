---
aid: codehooks:codehooks-database-rest-api
baseURL: https://{projectId}.api.codehooks.io/{space}
description: Auto-generated, secure REST API for Codehooks NoSQL collections, the built-in key-value store, and queue topics. Supports MongoDB-style query operators ($gt, $lt, $in, $nin, $exists, $regex, $or, $and), pagination, sorting, field selection, bulk update/delete by query, counts, and increment/decrement on key-value entries. Authenticated via API key.
humanURL: https://codehooks.io/docs/
image: ''
layout: api
name: Codehooks Database REST API
properties:
- type: Documentation
  url: https://codehooks.io/docs/
- type: APIReference
  url: https://codehooks.io/docs/restapi
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/codehooks/refs/heads/main/openapi/codehooks-database-rest-api-openapi.yml
provider_name: Codehooks
provider_slug: codehooks
slug: codehooks-database-rest-api
source_yaml: "aid: codehooks:codehooks-database-rest-api\nname: Codehooks Database REST API\ntags:\n- CRUD\n- Database\n- Documents\n- Key-Value\n- NoSQL\n- Queues\n- REST\nhumanURL: https://codehooks.io/docs/\nbaseURL: https://{projectId}.api.codehooks.io/{space}\nproperties:\n- url: https://codehooks.io/docs/\n  type: Documentation\n- url: https://codehooks.io/docs/restapi\n  type: APIReference\n- url: openapi/codehooks-database-rest-api-openapi.yml\n  type: OpenAPI\ndescription: Auto-generated, secure REST API for Codehooks NoSQL collections, the built-in key-value store,\n  and queue topics. Supports MongoDB-style query operators ($gt, $lt, $in, $nin, $exists, $regex, $or,\n  $and), pagination, sorting, field selection, bulk update/delete by query, counts, and increment/decrement\n  on key-value entries. Authenticated via API key.\nx-features:\n- Automatic CRUD REST API via app.crudlify()\n- MongoDB-like query language with $gt/$lt/$in/$exists/$regex/$or/$and\n- Pagination, sort, field\
  \ selection\n- Bulk updateByQuery and deleteByQuery\n- Key-value cache with TTL plus increment/decrement\n- Persistent queue API for asynchronous job processing\n- Auto-generated OpenAPI/Swagger from schema\n- Sub-5-second deploys via the codehooks CLI\nx-use-cases:\n- Internal CRUD apps and admin dashboards\n- Webhook receivers (Stripe, GitHub, Shopify) with persistent queues\n- Headless content backends for SPA/PWA hosting\n- AI agent state and memory backends\n- Lightweight microservices replacing custom Node.js + MongoDB stacks\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/codehooks/refs/heads/main/apis.yml
tags:
- CRUD
- Database
- Documents
- Key-Value
- NoSQL
- Queues
- REST
---
