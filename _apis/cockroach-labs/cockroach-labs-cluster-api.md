---
aid: cockroach-labs:cockroach-labs-cluster-api
baseURL: https://localhost:8080
description: REST API hosted by every CockroachDB node under the /api/v2 base path, exposed on the same HTTP port as the DB Console (default 8080). Provides health checks, node detail, hot range info, session and query introspection, database and table metadata, and event log retrieval. Authentication uses session tokens obtained via /api/v2/login/ and passed in the X-Cockroach-API-Session header. Self-hosted operators typically front the cluster API with a load balancer or service mesh.
humanURL: https://www.cockroachlabs.com/docs/stable/cluster-api
image: ''
layout: api
name: CockroachDB Cluster API
properties:
- type: Documentation
  url: https://www.cockroachlabs.com/docs/stable/cluster-api
- type: APIReference
  url: https://www.cockroachlabs.com/docs/api/cluster/v2
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cockroach-labs/refs/heads/main/openapi/cockroach-labs-cluster-api-openapi.yml
provider_name: Cockroach Labs
provider_slug: cockroach-labs
slug: cockroach-labs-cluster-api
tags:
- Cluster
- Database
- Monitoring
- Nodes
- Observability
---
