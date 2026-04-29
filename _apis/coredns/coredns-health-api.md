---
aid: coredns:coredns-health-api
baseURL: http://localhost:8080
description: The CoreDNS health plugin exposes HTTP /health and /ready endpoints on port 8080 by default. It reports the overall health and readiness of the CoreDNS process and is used by Kubernetes liveness and readiness probes to determine if the DNS server is operational.
humanURL: https://coredns.io/plugins/health/
image: ''
layout: api
name: CoreDNS Health API
properties:
- type: Documentation
  url: https://coredns.io/plugins/health/
- type: ReadyDocumentation
  url: https://coredns.io/plugins/ready/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/coredns/refs/heads/main/openapi/coredns-health-openapi.yml
- type: Rules
  url: https://raw.githubusercontent.com/api-evangelist/coredns/refs/heads/main/rules/coredns-health-rules.yml
- type: Capabilities
  url: https://raw.githubusercontent.com/api-evangelist/coredns/refs/heads/main/capabilities/coredns-health-capabilities.yml
provider_name: CoreDNS
provider_slug: coredns
slug: coredns-health-api
source_filename: coredns-health-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: CoreDNS Health API\n  description: >-\n    The CoreDNS health plugin exposes an HTTP health check endpoint at /health\n    on port 8080 by default. It reports the overall health of the CoreDNS\n    process and is used by Kubernetes liveness and readiness probes to determine\n    if the DNS server is operational. When lameduck mode is enabled, the health\n    endpoint returns HTTP 503 for a configurable duration before shutdown to\n    allow graceful traffic draining.\n  version: '2.x'\n  contact:\n    name: CoreDNS Community\n    url: https://coredns.io/community/\n  license:\n    name: Apache 2.0\n    url: https://www.apache.org/licenses/LICENSE-2.0\nexternalDocs:\n  description: CoreDNS Health Plugin Documentation\n  url: https://coredns.io/plugins/health/\nservers:\n  - url: http://localhost:8080\n    description: CoreDNS Health HTTP server (default port, configurable)\ntags:\n  - name: Health\n    description: >-\n      Health check endpoints\
  \ used by Kubernetes liveness and readiness probes\n      to assess the operational state of the CoreDNS process.\n  - name: Ready\n    description: >-\n      Readiness check endpoints that indicate whether CoreDNS plugins have\n      finished initializing and are ready to serve DNS queries.\npaths:\n  /health:\n    get:\n      operationId: getHealth\n      summary: CoreDNS liveness health check\n      description: >-\n        Returns the overall health status of the CoreDNS process. Returns HTTP\n        200 with body \"OK\" when CoreDNS is alive and healthy. Returns HTTP 503\n        during the lameduck shutdown period to signal that the instance is\n        draining and should not receive new traffic. This endpoint is typically\n        used as the Kubernetes liveness probe target.\n      tags:\n        - Health\n      responses:\n        '200':\n          description: CoreDNS is healthy and alive.\n          content:\n            text/plain:\n              schema:\n               \
  \ type: string\n                example: OK\n        '503':\n          description: >-\n            CoreDNS is in lameduck mode (shutting down gracefully). The process\n            is still running but draining connections before exit.\n          content:\n            text/plain:\n              schema:\n                type: string\n                example: lameduck\n  /ready:\n    get:\n      operationId: getReadiness\n      summary: CoreDNS readiness check\n      description: >-\n        Returns the readiness status of all CoreDNS plugins. Returns HTTP 200\n        with body \"OK\" when all plugins that implement the Readiness interface\n        report they are ready to serve traffic. Returns HTTP 503 if any plugin\n        is not yet ready. This endpoint is typically used as the Kubernetes\n        readiness probe target and requires the ready plugin to be enabled in\n        the Corefile.\n      tags:\n        - Ready\n      responses:\n        '200':\n          description: All CoreDNS\
  \ plugins are ready to serve traffic.\n          content:\n            text/plain:\n              schema:\n                type: string\n                example: OK\n        '503':\n          description: >-\n            One or more CoreDNS plugins are not yet ready. The server is still\n            initializing.\n          content:\n            text/plain:\n              schema:\n                type: string\n                example: not ready\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/coredns/refs/heads/main/openapi/coredns-health-openapi.yml
tags:
- Health Check
- Kubernetes
- Observability
- Readiness
---
