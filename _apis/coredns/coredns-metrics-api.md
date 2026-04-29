---
aid: coredns:coredns-metrics-api
baseURL: http://localhost:9153
description: The CoreDNS prometheus plugin exposes a Prometheus-compatible metrics endpoint at /metrics on port 9153. It provides DNS request counters, response size histograms, latency distributions, and build information metrics for monitoring CoreDNS performance and behavior.
humanURL: https://coredns.io/plugins/metrics/
image: ''
layout: api
name: CoreDNS Metrics API
properties:
- type: Documentation
  url: https://coredns.io/plugins/metrics/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/coredns/refs/heads/main/openapi/coredns-metrics-openapi.yml
- type: Rules
  url: https://raw.githubusercontent.com/api-evangelist/coredns/refs/heads/main/rules/coredns-metrics-rules.yml
- type: Capabilities
  url: https://raw.githubusercontent.com/api-evangelist/coredns/refs/heads/main/capabilities/coredns-metrics-capabilities.yml
provider_name: CoreDNS
provider_slug: coredns
slug: coredns-metrics-api
source_filename: coredns-metrics-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: CoreDNS Metrics API\n  description: >-\n    The CoreDNS prometheus plugin exposes a Prometheus-compatible metrics\n    endpoint at /metrics on port 9153 by default. It provides DNS request\n    counters broken down by server, zone, type, and rcode; response size\n    histograms; cache hit and miss counters; forward request counters; latency\n    distributions; and build information. These metrics are scraped by\n    Prometheus or compatible monitoring systems for observability into CoreDNS\n    performance and DNS query patterns.\n  version: '2.x'\n  contact:\n    name: CoreDNS Community\n    url: https://coredns.io/community/\n  license:\n    name: Apache 2.0\n    url: https://www.apache.org/licenses/LICENSE-2.0\nexternalDocs:\n  description: CoreDNS Metrics Plugin Documentation\n  url: https://coredns.io/plugins/metrics/\nservers:\n  - url: http://localhost:9153\n    description: CoreDNS Prometheus metrics HTTP server (default port, configurable)\n\
  tags:\n  - name: Metrics\n    description: >-\n      Prometheus-compatible metrics endpoints exposing DNS query statistics,\n      cache performance, latency histograms, and build information.\npaths:\n  /metrics:\n    get:\n      operationId: getMetrics\n      summary: CoreDNS Get Prometheus metrics\n      description: >-\n        Returns all CoreDNS metrics in Prometheus text exposition format\n        (version 0.0.4). The response includes counters, gauges, histograms,\n        and summaries covering DNS request rates by server and zone,\n        response code distributions, DNS query type breakdowns, cache hit\n        rates, panics, and plugin-specific metrics such as forward latency and\n        health check state. Requires the prometheus plugin to be configured in\n        the Corefile.\n      tags:\n        - Metrics\n      responses:\n        '200':\n          description: Prometheus text format metrics.\n          content:\n            text/plain:\n              schema:\n   \
  \             type: string\n                description: >-\n                  Prometheus exposition format text, one metric per line with\n                  HELP and TYPE comments followed by sample lines. Key metrics\n                  include coredns_dns_requests_total, coredns_dns_responses_total,\n                  coredns_dns_request_duration_seconds,\n                  coredns_cache_hits_total, coredns_cache_misses_total,\n                  coredns_forward_requests_total, and\n                  coredns_build_info.\n              example: |\n                # HELP coredns_build_info A metric with a constant '1' value labeled by version, revision, and goversion from which CoreDNS was built.\n                # TYPE coredns_build_info gauge\n                coredns_build_info{goversion=\"go1.21.0\",revision=\"abcdef\",version=\"1.11.1\"} 1\n                # HELP coredns_dns_requests_total Counter of DNS requests made per zone, protocol and family.\n                # TYPE coredns_dns_requests_total\
  \ counter\n                coredns_dns_requests_total{family=\"1\",proto=\"udp\",server=\"dns://:53\",type=\"A\",zone=\".\"} 42\n                # HELP coredns_dns_request_duration_seconds Histogram of the time (in seconds) each request took per zone.\n                # TYPE coredns_dns_request_duration_seconds histogram\n                coredns_dns_request_duration_seconds_bucket{le=\"0.00025\",server=\"dns://:53\",type=\"A\",zone=\".\"} 10\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/coredns/refs/heads/main/openapi/coredns-metrics-openapi.yml
tags:
- Metrics
- Monitoring
- Observability
- Prometheus
---
