---
aid: cockroachdb:cluster-api
baseURL: https://localhost:8080/api/v2
description: REST API hosted by every CockroachDB node under the /api/v2 base path, exposed on the same HTTP port as the DB Console (default 8080). Provides health checks, node detail, hot range info, session and query introspection, database and table metadata, and event log retrieval. Authentication uses session tokens obtained via /api/v2/login/ and passed in the X-Cockroach-API-Session header.
humanURL: https://www.cockroachlabs.com/docs/stable/cluster-api
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: CockroachDB Cluster API
properties:
- type: Documentation
  url: https://www.cockroachlabs.com/docs/stable/cluster-api
- type: APIReference
  url: https://www.cockroachlabs.com/docs/api/cluster/v2
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cockroachdb/refs/heads/main/openapi/cockroachdb-cluster-api-openapi.yml
provider_name: CockroachDB
provider_slug: cockroachdb
slug: cluster-api
tags:
- Cluster
- Database
- Monitoring
- Nodes
- Observability
---
