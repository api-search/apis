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
source_yaml: "aid: cockroachdb:cluster-api\nname: CockroachDB Cluster API\ntags:\n- Cluster\n- Database\n- Monitoring\n- Nodes\n- Observability\nimage: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg\nbaseURL: https://localhost:8080/api/v2\nhumanURL: https://www.cockroachlabs.com/docs/stable/cluster-api\nproperties:\n- url: https://www.cockroachlabs.com/docs/stable/cluster-api\n  type: Documentation\n- url: https://www.cockroachlabs.com/docs/api/cluster/v2\n  type: APIReference\n- url: openapi/cockroachdb-cluster-api-openapi.yml\n  type: OpenAPI\ndescription: REST API hosted by every CockroachDB node under the /api/v2 base path, exposed on the same\n  HTTP port as the DB Console (default 8080). Provides health checks, node detail, hot range info, session\n  and query introspection, database and table metadata, and event log retrieval. Authentication uses session\n  tokens obtained via /api/v2/login/ and passed in the X-Cockroach-API-Session header.\nx-features:\n\
  - Available on every CockroachDB node\n- Session-token auth via /api/v2/login/\n- Health, node, range, and database introspection\n- JSON responses suitable for monitoring pipelines\nx-use-cases:\n- Custom dashboards and alerting\n- Liveness probes and readiness checks\n- Hot-range and session troubleshooting\n- Self-hosted observability integrations\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cockroachdb/refs/heads/main/apis.yml
tags:
- Cluster
- Database
- Monitoring
- Nodes
- Observability
---
