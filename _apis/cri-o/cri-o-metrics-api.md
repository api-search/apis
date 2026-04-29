---
aid: cri-o:cri-o-metrics-api
baseURL: http://localhost:9090
description: The CRI-O metrics endpoint exposes Prometheus-compatible metrics for operation counts, container lifecycle, image pulls, and errors. It is enabled with the --enable-metrics flag and served on the configured port (default 9090) at the /metrics path. The endpoint can also be served over a Unix socket and secured with TLS for cluster-grade observability.
humanURL: https://github.com/cri-o/cri-o/blob/main/docs/metrics.md
image: ''
layout: api
name: CRI-O Metrics API
properties:
- type: Documentation
  url: https://github.com/cri-o/cri-o/blob/main/docs/metrics.md
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cri-o/refs/heads/main/openapi/cri-o-metrics-openapi.yml
- type: Rules
  url: https://raw.githubusercontent.com/api-evangelist/cri-o/refs/heads/main/rules/cri-o-metrics-rules.yml
- type: Capabilities
  url: https://raw.githubusercontent.com/api-evangelist/cri-o/refs/heads/main/capabilities/cri-o-metrics-capabilities.yml
provider_name: CRI-O
provider_slug: cri-o
slug: cri-o-metrics-api
source_filename: cri-o-metrics-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: CRI-O Metrics API\n  description: >-\n    The CRI-O metrics endpoint exposes Prometheus-compatible metrics for\n    operations, image pulls, container lifecycle, and runtime errors. Metrics\n    are enabled with the --enable-metrics daemon flag and served on the port\n    configured by --metrics-port (default 9090) at the /metrics path. The\n    endpoint can also be served over a Unix socket via --metrics-socket and\n    secured using --metrics-cert and --metrics-key for TLS.\n  version: '1.0'\n  contact:\n    name: CRI-O Project\n    url: https://cri-o.io/\n  license:\n    name: Apache 2.0\n    url: https://github.com/cri-o/cri-o/blob/main/LICENSE\nexternalDocs:\n  description: CRI-O Metrics Documentation\n  url: https://github.com/cri-o/cri-o/blob/main/docs/metrics.md\nservers:\n  - url: http://localhost:9090\n    description: Default CRI-O metrics endpoint\ntags:\n  - name: Metrics\n    description: Prometheus metrics scraping endpoint.\n\
  paths:\n  /metrics:\n    get:\n      tags:\n        - Metrics\n      operationId: getMetrics\n      summary: Scrape Prometheus metrics\n      description: >-\n        Returns the current CRI-O metrics in the Prometheus text exposition\n        format, including operation counters, latency histograms, image pull\n        statistics, and error counters.\n      responses:\n        '200':\n          description: Prometheus metrics in text exposition format.\n          content:\n            text/plain:\n              schema:\n                type: string\n              example: |\n                # HELP container_runtime_crio_operations_total Cumulative number of CRI-O operations by operation type.\n                # TYPE container_runtime_crio_operations_total counter\n                container_runtime_crio_operations_total{operation_type=\"create_container\"} 42\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cri-o/refs/heads/main/openapi/cri-o-metrics-openapi.yml
tags:
- Metrics
- Monitoring
- Observability
- Prometheus
---
