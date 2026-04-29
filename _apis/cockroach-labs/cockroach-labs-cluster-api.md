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
source_yaml: "aid: cockroach-labs:cockroach-labs-cluster-api\nname: CockroachDB Cluster API\ntags:\n- Cluster\n- Database\n- Monitoring\n- Nodes\n- Observability\nhumanURL: https://www.cockroachlabs.com/docs/stable/cluster-api\nbaseURL: https://localhost:8080\nproperties:\n- url: https://www.cockroachlabs.com/docs/stable/cluster-api\n  type: Documentation\n- url: https://www.cockroachlabs.com/docs/api/cluster/v2\n  type: APIReference\n- url: openapi/cockroach-labs-cluster-api-openapi.yml\n  type: OpenAPI\ndescription: REST API hosted by every CockroachDB node under the /api/v2 base path, exposed on the same\n  HTTP port as the DB Console (default 8080). Provides health checks, node detail, hot range info, session\n  and query introspection, database and table metadata, and event log retrieval. Authentication uses session\n  tokens obtained via /api/v2/login/ and passed in the X-Cockroach-API-Session header. Self-hosted operators\n  typically front the cluster API with a load balancer or\
  \ service mesh.\nx-features:\n- Available on every CockroachDB node\n- Session-token authentication via /api/v2/login/\n- Health, node, range, session, and database introspection\n- JSON responses suitable for monitoring and alerting integrations\nx-use-cases:\n- Custom dashboards and observability pipelines\n- Programmatic health/readiness checks\n- Hot-range and session troubleshooting\n- Liveness probes for self-hosted CockroachDB\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cockroach-labs/refs/heads/main/apis.yml
tags:
- Cluster
- Database
- Monitoring
- Nodes
- Observability
---
