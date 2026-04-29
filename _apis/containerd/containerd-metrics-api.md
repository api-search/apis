---
aid: containerd:containerd-metrics-api
baseURL: ''
description: The containerd metrics plugin exposes a Prometheus-compatible HTTP endpoint for scraping runtime metrics. When enabled via the metrics.address configuration option in config.toml, it serves Prometheus text format metrics covering gRPC request counts, latency histograms, snapshot usage, content store statistics, and task lifecycle events.
humanURL: https://containerd.io/docs/
image: ''
layout: api
name: Containerd Metrics API
properties:
- type: Documentation
  url: https://containerd.io/docs/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/containerd/refs/heads/main/openapi/containerd-metrics-openapi.yml
provider_name: Containerd
provider_slug: containerd
slug: containerd-metrics-api
source_filename: containerd-metrics-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Containerd Metrics API\n  description: >-\n    The containerd metrics plugin exposes a Prometheus-compatible HTTP endpoint\n    for scraping runtime metrics. When enabled via the metrics.address\n    configuration option in config.toml, it serves Prometheus text format\n    metrics covering gRPC request counts, latency histograms, snapshot usage,\n    content store statistics, and task lifecycle events. This endpoint enables\n    integration with Prometheus, Grafana, and other observability tooling for\n    monitoring the containerd container runtime.\n  version: '2.x'\n  contact:\n    name: Containerd Community\n    url: https://containerd.io/community/\n  license:\n    name: Apache 2.0\n    url: https://www.apache.org/licenses/LICENSE-2.0\nexternalDocs:\n  description: Containerd Documentation\n  url: https://containerd.io/docs/\nservers:\n  - url: http://localhost:1338\n    description: >-\n      Containerd metrics HTTP server. Address is\
  \ configured via\n      metrics.address in config.toml (e.g., \"127.0.0.1:1338\").\ntags:\n  - name: Metrics\n    description: >-\n      Prometheus-compatible metrics endpoints exposing containerd runtime\n      statistics including gRPC request rates, snapshot usage, and task\n      lifecycle counts.\npaths:\n  /v1/metrics:\n    get:\n      operationId: getMetrics\n      summary: Containerd Get Prometheus metrics\n      description: >-\n        Returns all containerd metrics in Prometheus text exposition format.\n        Metrics include gRPC server request counts and latency histograms\n        (when grpc_histogram is enabled), snapshotter usage statistics,\n        content store byte counts, task start and exit counters, and\n        container count gauges. Each metric is labeled by namespace,\n        snapshotter, or plugin type as appropriate. Requires the metrics\n        address to be configured in the containerd config.toml.\n      tags:\n        - Metrics\n      responses:\n  \
  \      '200':\n          description: Prometheus text format metrics.\n          content:\n            text/plain:\n              schema:\n                type: string\n                description: >-\n                  Prometheus exposition format text (version 0.0.4). Lines\n                  beginning with # HELP describe the metric, # TYPE lines\n                  declare metric type (counter, gauge, histogram, summary),\n                  and sample lines contain the metric name, optional labels,\n                  value, and optional timestamp. Key metrics include\n                  container_tasks_running, container_running_time_microseconds,\n                  grpc_server_handled_total, and snapshot_stats.\n              example: |\n                # HELP containerd_snapshotter_snapshot_inodes_usage Snapshot inodes usage in bytes.\n                # TYPE containerd_snapshotter_snapshot_inodes_usage gauge\n                containerd_snapshotter_snapshot_inodes_usage{snapshotter=\"\
  overlayfs\"} 1024\n                # HELP grpc_server_handled_total Total number of RPCs completed on the server.\n                # TYPE grpc_server_handled_total counter\n                grpc_server_handled_total{grpc_code=\"OK\",grpc_method=\"ListContainers\",grpc_service=\"containerd.services.containers.v1.Containers\",grpc_type=\"unary\"} 42\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/containerd/refs/heads/main/openapi/containerd-metrics-openapi.yml
tags:
- Metrics
- Observability
- Prometheus
---
